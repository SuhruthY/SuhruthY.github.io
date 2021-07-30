---
title: Extracting data from GitHub search API
layout: post
post-image: https://pbs.twimg.com/profile_images/1978599420/electrocat.png
description: The Search API is an XQuery library that combines searching, search parsing, search grammar, faceting, snippeting, search term completion, and other search application features into a single API. You can interact with the Search API through XQuery, REST, Node.
tags:
- GitHub
- repository
- social media
---

    I’m assuming you are familiar with some R-programming. If not please go through some [Getting Started With R][1]

    Let’s load some required packages

    library(gh)
    library(httr)
    library(jsonlite)
    library(dplyr)

## GitHub Search API

    The GithHub’s Search API helps you search for the specific item you
want to find. Just like searching on Google, you sometimes want to see a
few pages of search results so that you can find the item that best
meets your needs. To satisfy that need, the GitHub Search API provides
up to *1,000* results for each search.

    The Search API has a custom rate limit.  
        - For requests using Basic
Authentication, OAuth, or client ID and secret, you can make up to *30*
requests per minute.  
        - For unauthenticated requests, the rate limit
allows you to make up to *10* requests per minute.

In the next few minutes we are going to retrieve trending repositories
which were created over the last years i.e.*2020* data

> The definition of trending repositories in our case will be only those repositories which have at least 500 stars or more.

## Utility Functions

    Let’s define some fucntions that are useful to retrieve the data.

    DataFramefromCall <- function(x) {
        x <- URLencode(x)
        data <- jsonlite::fromJSON(x)
        items <- data$items
        req_names <- c("id", "name", "full_name", "size", "open_issues",
                       'fork', 'stargazers_count', 'watchers', 'forks',
                       "language", "has_issues", "has_downloads", "has_wiki",
                       "has_page", "created_at", "updated_at", "pushed_at", 
                       "url", "description")
        
        mynames <- c()
        for (name in req_names){
            if (name %in% colnames(items)){
                mynames <- c(mynames, name)
            }
        }
        
        items <- items[,mynames]
        
        Sys.sleep(5)
        return(data.frame(items))
    } 

    get.trending.repositories <- function(timeline.dates, auth.id, auth.pwd){
        # set parameters
        base_url <- "https://api.github.com/search/repositories?"
        
        api_id_param <- paste0("client_id=", auth.id)
        api_pwd_param <- paste0("client_secret=", auth.pwd)
        arg_sep = '&'
        per_page <- 100
        
        top.repos.df <- data.frame(stringsAsFactors=FALSE)
        pb <- txtProgressBar(min = 0, max = length(timeline.dates), style = 3)
        
        # for each pair of dates in list get all trending repos
        for (i in seq(1, length(timeline.dates), by = 2)){ 
            start_date <- timeline.dates[i]
            end_date <- timeline.dates[i+1]
            query <- paste0("q=created:%22", start_date, "%20..%20", end_date, 
                            "%22%20stars:%3E=500")
            url <- paste0(base_url, query, arg_sep, api_id_param, arg_sep, api_pwd_param)
     
            firstCall <- GET(paste(url)) %>% content()
            total_repos <- min(firstCall$total_count, 1000)
            number_calls <- ceiling(total_repos/per_page)
            
            query2 <- "&per_page=100&page="
            api_calls <- paste(url, query2, as.character(c(1:number_calls)), sep = "")
            
            for (i in 1:number_calls) {
                top.repos.df <- rbind(top.repos.df, DataFramefromCall(api_calls[i]))
                Sys.sleep(2)
            
            }
            Sys.sleep(3)
            setTxtProgressBar(pb, i+1)
        }
        print("---- FINISHED ---")
        return(top.repos.df)
    }

    loop_to_get_repo_data <- function(){
        i <- 0
        v <- 1
        for (date in dates){
            if(i%%2 == 0){
                req_dates <- c(date, dates[v+1])
                tmp_repos <- get.trending.repositories(timeline.dates = req_dates,
                                                       auth.id = auth.id, auth.pwd = auth.pwd)
                Sys.sleep(5)
                
                tmp <- dim(tmp_repos)

                print(paste("Temporarily downloaded", paste(tmp[1], "x", tmp[2])))

                trending_repos <- rbind(trending_repos, tmp_repos)
                
                tmp <- dim(trending_repos)

                print(paste("Final data dimensions", paste(tmp[1], "x", tmp[2])))
                
                Sys.sleep(5)
            }
            i = i + 1
            v = v + 1
        }
        return(trending_repos)
    }

   
  
    To keep the auth variables secret you can use the R console as below

    Now we can load these vars into r script and also the dates required
in chunks as a list(to overcome the rate limit).

    auth.id <- GITHUB_CLIENT_ID
    auth.pwd <- GITHUB_CLIENT_SECRET

    dates <- c('2020-01-01', '2020-03-31',
               '2020-04-01', '2020-06-30',
               '2020-07-01', '2020-09-30',
               '2020-10-01', '2020-12-31')

    trending_repos <- data.frame(stringsAsFactors = F)

    trending_repos <- loop_to_get_repo_data()

---
    ##   |                                               |                                            |   0%[1] "---- FINISHED ---"
    ## [1] "Temporarily downloaded 761 x 18"
    ## [1] "Final data dimensions 761 x 18"
    ##   |                                               |                                            |   0%[1] "---- FINISHED ---"
    ## [1] "Temporarily downloaded 714 x 18"
    ## [1] "Final data dimensions 1475 x 18"
    ##   |                                               |                                            |   0%[1] "---- FINISHED ---"
    ## [1] "Temporarily downloaded 507 x 18"
    ## [1] "Final data dimensions 1982 x 18"        
    ##   |                                               |                                            |   0%[1] "---- FINISHED ---"
    ## [1] "Temporarily downloaded 306 x 18"
    ## [1] "Final data dimensions 2288 x 18"

<br>

    typeof(trending_repos)  
     
---
    ## [1] "list"
    
    
    As we can see the recieved data is in the form of a list. So let's convert it to a data frame.
     

    trending_repos_df <- data.frame(trending_repos)
    trending_repos_df <- as_tibble(trending_repos_df)
    trending_repos_df  
    
----
    ## # A tibble: 2,288 x 18
    ##        id name  full_name   size open_issues fork  stargazers_count watchers
    ##     <int> <chr> <chr>      <int>       <int> <lgl>            <int>    <int>
    ##  1 2.42e8 fuck~ labulado~ 109612          33 FALSE            86633    86633
    ##  2 2.38e8 COVI~ CSSEGISa~ 988047        1673 FALSE            25938    25938
    ##  3 2.31e8 exca~ excalidr~  24629         302 FALSE            18945    18945
    ##  4 2.42e8 tools rome/too~  92295          98 FALSE            14919    14919
    ##  5 2.51e8 CnC_~ electron~   7916          80 FALSE            14823    14823
    ##  6 2.46e8 Vent~ ventoy/V~ 154039         313 FALSE            14426    14426
    ##  7 2.38e8 diag~ mingramm~  26595         181 FALSE            13111    13111
    ##  8 2.34e8 fiber gofiber/~  25790          18 FALSE            12433    12433
    ##  9 2.44e8 fast~ fastai/f~  76662          54 FALSE            12022    12022
    ## 10 2.43e8 hero~ tailwind~   1043         158 FALSE            11644    11644
    ## # ... with 2,278 more rows, and 10 more variables: forks <int>, language <chr>,
    ## #   has_issues <lgl>, has_downloads <lgl>, has_wiki <lgl>, created_at <chr>,
    ## #   updated_at <chr>, pushed_at <chr>, url <chr>, description <chr>


[1]:https://www.youtube.com/results?search_query=getting+started+with+R
