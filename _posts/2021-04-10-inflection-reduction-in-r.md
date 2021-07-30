---
title: 2 Ways to Reduce Inflection in Text Data
layout: post
post-image: https://miro.medium.com/max/1200/1*h0mO4PdZaQKtbwWJW40FKQ.jpeg
description: Text normalization is the process of transforming text into a single canonical form that it might not have had before. Normalizing text before storing or processing it allows for separation of concerns, since input is guaranteed to be consistent before operations are performed on it.
tags:
- textdata
- stemming
- lemma
---

According to Wikipedia,  
&nbsp;&nbsp;&nbsp;&nbsp;*In linguistic morphology, inflection (or inflexion) is a process of word formation, in which a word is modified to express different grammatical categories such as tense, case, voice, aspect, person, number, gender, mood, animacy, and definiteness*.

&nbsp;&nbsp;&nbsp;&nbsp;These are formed either by the addition of -s or -es to nouns, -ed and -ing to verbs, and -er and -est to adjectives and adverbs or changing the spelling of the root word or a doubling of a final letter.

&nbsp;&nbsp;&nbsp;&nbsp;The goal of both **stemming** and **lemmatization** is to reduce inflectional forms and sometimes derivationally related forms of a word to a common base form. For instance:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;am, are, is ⇒ be  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;car, cars, car’s, cars’ ⇒ car

&nbsp;&nbsp;&nbsp;&nbsp;In this page we are going to talk about these two techniques in great detail.

```
# loading packages
library(textstem)
library(SnowballC)
library(hunspell)

library(tidytext)
library(textclean)
library(tidyverse)
library(dplyr)

library(hcandersenr)
library(tokenizers)
library(sentimentr)
```


## Stemming
&nbsp;&nbsp;&nbsp;&nbsp;Stemming is the act of removing inflections from a word not necessarily “*identical to the morphological root of the word*”.  
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;Consider as an example searching over a corpus of documents. More specifically, we might prepare a bunch of documents to be searchable in some kind of search term. Let’s say we wanna search indexers, indexing and indexable    
&nbsp;   
&nbsp;&nbsp;&nbsp;&nbsp;Instead of checking for all of the three seperately in the document, one can search for the word *index* and get the same results.  
&nbsp;  
The way we can do this using r would be something like this
```{r}
wordVec <- c('driver', 'drive', 'drove', 'driven', 'drives', 'driving')
stem_words(wordVec)
```
---
    ## [1] "driver" "drive"  "drove"  "driven" "drive"  "drive"   
    
&nbsp;  
```{r}
sentVec <- c(
    'the dirtier dog has eaten the pies',
    'that shameful pooch is tricky and sneaky',
    "He opened and then reopened the food bag",
    'There are skies of blue and red roses too!',
    NA,
    "The doggies, well they aren't joyfully running.",
     "The daddies are coming over...",
    "This is 34.546 above")   

stem_strings(sentVec)
```
---
    ## [1] "the dirtier dog ha eaten the pi"          
    ## [2] "that shame pooch i tricki and sneaki"     
    ## [3] "He open and then reopen the food bag"     
    ## [4] "There ar ski of blue and red rose too!"   
    ## [5] NA                                         
    ## [6] "The doggi, well thei aren't joyfulli run."
    ## [7] "The daddi ar come over..."                
    ## [8] "Thi i 34. 546 abov"    
  
&nbsp;       
But this was not so accurate, So let’s first understand some stemming algorithms which might be helpful.

### Porter Stemmer
&nbsp;&nbsp;&nbsp;&nbsp;The Porter stemmer makes a use of a measure, m, of the length of a word or word part. If C is a sequence of one or more consonants, and V a sequence of one or more vowels, any word part has the form  
<p align="center" style="font-weight:bold">[C](VC)m[V]</p>  
  
Let’s go with a practical approach
```{r}
sentVec <- hca_fairytales() %>%
            filter(book == "The fir tree",
                   language == "English") %>%
                select(text)

wordsVec <- unnest_tokens(sentVec, word, text) %>%
                anti_join(get_stopwords())
                
wordsVec %>%
    count(word, sort = TRUE) %>%
        filter(str_detect(word, "^tree"))
```
---
    ## # A tibble: 3 x 2
    ##   word       n
    ##   <chr>  <int>
    ## 1 tree      76
    ## 2 trees     12
    ## 3 tree's     1  

&nbsp;  
As you can see above, there are lots of words in this text like this. Let’s try to reduce the inflection.
```
# stemming using SnowballC
wordsVec %>%
  mutate(stem = wordStem(word)) %>%
    count(stem, sort = TRUE)
```
---
    ## # A tibble: 570 x 2
    ##    stem        n
    ##    <chr>   <int>
    ##  1 tree       88
    ##  2 fir        34
    ##  3 littl      23
    ##  4 said       22
    ##  5 stori      16
    ##  6 thought    16
    ##  7 branch     15
    ##  8 on         15
    ##  9 came       14
    ## 10 know       14
    ## # ... with 560 more rows  

&nbsp;  
You can also perform the same stuff above using a single function called *tokenize_word_stems* from the pakage *tokenizers* as shown below
```
hca_fairytales() %>%
    filter(book == "The fir tree",
           language == "English") %>%
        select(text) %>%
            paste0() %>%
                tokenize_word_stems(stopwords = stopwords::stopwords("en")) %>%
                    as.data.frame(col.names="stem") %>%
                        as_tibble() %>% count(stem, sort=TRUE)
```
---
    ## # A tibble: 566 x 2
    ##    stem        n
    ##    <chr>   <int>
    ##  1 tree       89
    ##  2 fir        34
    ##  3 littl      23
    ##  4 said       22
    ##  5 stori      16
    ##  6 thought    16
    ##  7 branch     15
    ##  8 one        15
    ##  9 came       14
    ## 10 know       14
    ## # ... with 556 more rows

### Hungspell Stemmer
&nbsp;&nbsp;&nbsp;&nbsp;Hunspell Stemmer is a dictionary-based stemmer meaning uses a predefined dictionary for stemming.   
&nbsp;    
&nbsp;&nbsp;&nbsp;&nbsp;*Hun* in Hunspell stands for *Hungarian*; this set of NLP algorithms was originally written to handle Hungarian but has since been extended to handle many languages with compound words and complicated morphology.   
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;The Hunspell library is used mostly as a spell checker, but as part of identifying correct spellings, this library identifies word stems as well. You can use the Hunspell library from R via the *hunspell* package.  
```
words <- c("love", "loving", "lovingly", "loved", "lover", "lovely", "love")
hunspell_stem(words)
```
---
    ## [[1]]
    ## [1] "love"
    ## 
    ## [[2]]
    ## [1] "loving" "love"  
    ## 
    ## [[3]]
    ## [1] "loving"
    ## 
    ## [[4]]
    ## [1] "loved" "love" 
    ## 
    ## [[5]]
    ## [1] "lover" "love" 
    ## 
    ## [[6]]
    ## [1] "lovely" "love"  
    ## 
    ## [[7]]
    ## [1] "love"  

&nbsp;  
Hunspell uses a special dictionary format that defines which characters, words and conjugations are valid in a given language.

Let’s use the hungspell dictionary on the words vector now
```
wordsVec %>%
    mutate(stem=hunspell_stem(word)) %>%
    unnest(stem) %>% count(stem, sort = TRUE)
```
---
    ## # A tibble: 595 x 2
    ##    stem       n
    ##    <chr>  <int>
    ##  1 tree      89
    ##  2 fir       34
    ##  3 little    23
    ##  4 said      22
    ##  5 story     16
    ##  6 branch    15
    ##  7 one       15
    ##  8 came      14
    ##  9 know      14
    ## 10 now       14
    ## # ... with 585 more rows

## Lemmatization
&nbsp;&nbsp;&nbsp;&nbsp;Lemmatizing works by “*grouping together the inflected forms of a word so they can be analysed as a single item*”.    
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;Lemmatization considers the context and converts the word to its meaningful base form, whereas *stemming* just removes the last few characters, often leading to incorrect meanings and spelling errors.  
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;For example,   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Caring* -&gt; Lemmatization -&gt; *Care*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Caring* -&gt; Stemming -&gt; *Car*

Let’s see the same using the *lemmatize_words* function in *text_stem*
```
bforms <- c('are', 'am', 'being', 'been', 'be')
stem_words(bforms)
```
---
    ## [1] "ar"   "am"   "be"   "been" "be"   
    
 &nbsp;     
```
lemmatize_words(bforms)
``` 
---
    ## [1] "be" "be" "be" "be" "be"  
  
&nbsp;    
&nbsp;  
It also provide with the function *lemmatize_strings* as follows  
```
crowdflower_self_driving_cars$text %>% head()
```
---
    ## [1] "Two places I'd invest all my money if I could: 3D printing and Self-driving cars!!!"                                   
    ## [2] "Awesome! Google driverless cars will help the blind travel more often; https://t.co/QWuXR0FrBpv"                       
    ## [3] "If Google maps can't keep up with road construction, how am I supposed to trust a driverless car to get around here?"  
    ## [4] "Autonomous cars seem way overhyped given the technology challenges; pilotless planes seem much more doable and needed."
    ## [5] "Just saw Google self-driving car on I-34. It was painted green and blue."
    ## [6] "Will driverless cars eventually replace taxi drivers in cities?"    
    
&nbsp;      
```
crowdflower_self_driving_cars$text %>% lemmatize_strings() %>% head() 
```
---
    ## [1] "Two place I'd invest all my money if I can: 3D print and Self - drive car!!!"                                      
    ## [2] "Awesome! Google driverless car will help the blind travel much often; https: / / t. co / QWuXR0FrBpv"              
    ## [3] "If Google map can't keep up with road construction, how be I suppose to trust a driverless car to get around here?"
    ## [4] "Autonomous car seem way overhyped give the technology challenge; pilotless plane seem much much doable and need."  
    ## [5] "Just see Google self - drive car on I - 34. It be paint green and blue."
    ## [6] "Will driverless car eventually replace taxi driver in city?"

&nbsp;  
### Lemma Dictionary
&nbsp;&nbsp;&nbsp;&nbsp;There are many lemma dictionary available such as hunspell, treetagger, etc. Here I’m using the *`lexicon's`: hash lemmas dictionary*.   
```
sentVec <- get_sentences(hotel_reviews$text[1])[[1]]
sentVec <- strip(sentVec)
sentVec
```
---
    ## [1] "this hotel is in the perfect location"           
    ## [2] "it's within walking distance to many sites and just a tram ride away from everything else"                                            
    ## [3] "the staff in this hotel is exceptional"          
    ## [4] "very friendly and helpful"                                          
    ## [5] "we enjoyed the beautiful rooftop terrace with views of the marmara sea" 
    ## [6] "breakfast here was a very nice way to start each day"            

&nbsp;  
```
sentVec %>% lemmatize_strings(dictionary = lexicon::hash_lemmas)
```
---
    ## [1] "this hotel be in the perfect location"                                                                                            
    ## [2] "it's within walk distance to many site and just a tram ride away from everything else"                                            
    ## [3] "the staff in this hotel be exceptional"                                                                                           
    ## [4] "very friendly and helpful"                                                                                                        
    ## [5] "we enjoy the beautiful rooftop terrace with view of the marmara sea"                                                              
    ## [6] "breakfast here be a very nice way to start each day"    
    
&nbsp;  
For a given a set of text strings, the *make\_lemma\_dictionary* function generates a dictionary of lemmas corresponding to words that are not in base form.
```
hs_dict <- hotel_reviews$text[1] %>% make_lemma_dictionary(engine = 'hunspell')
sentVec %>% lemmatize_strings(dictionary = hs_dict)
```
---
    ## [1] "this hotel i in the perfect locate"                                                                                                
    ## [2] "it within walk distance to many site and just a tram ride away from everything else"                                               
    ## [3] "the staff in this hotel i exceptional"                                                                                             
    ## [4] "very friend and helpful"                                                                                                           
    ## [5] "we enjoy the beautiful rooftop terrace with view of the marmara sea"                                                               
    ## [6] "breakfast here was a very nice way to start each day"   
    
&nbsp;  
As you can see this wa more effective

## Stem vs Lemma
&nbsp;&nbsp;&nbsp;&nbsp;Below you can see that *stemming* the debate data took less time than *lemmatizing* the same and also more accurate.
```
stic <- Sys.time()

presidential_debates_2012$dialogue %>%
    stem_strings() %>%
    head()
```
---
    ## [1] "We'll talk about specif about health care in a moment."                             
    ## [2] "But what do you support the voucher system, Governor?"                              
    ## [3] "What I support i no chang for current retire and near retire to Medicar."           
    ## [4] "And the presid support take dollar seven hundr sixteen billion out of that program."
    ## [5] "And what about the voucher?"                                                        
    ## [6] "So that' that' number on."  

&nbsp;  
```
(stoc <- Sys.time() - stic)
```
---
    ## Time difference of 0.125922 secs  

&nbsp;   
&nbsp;  
```
    ltic <- Sys.time()

    presidential_debates_2012$dialogue %>%
        lemmatize_strings() %>%
        head()
```
---
    ## [1] "We'll talk about specifically about health care in a moment."                            
    ## [2] "But what do you support the voucher system, Governor?"                                   
    ## [3] "What I support be no change for current retiree and near retiree to Medicare."           
    ## [4] "And the president support take dollar seven hundred sixteen billion out of that program."
    ## [5] "And what about the voucher?"                                                             
    ## [6] "So that's that's numb one."    
    
&nbsp;  
```
(ltoc <- Sys.time() - ltic)
```
---
    ## Time difference of 0.1309261 secs  
    
&nbsp;  
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;In general, lemmatization offers better precision than stemming, but at the expense of recall.

&nbsp;&nbsp;&nbsp;&nbsp;If speed is focused then stemming should be used since lemmatizers scan a corpus which consumed time and processing. It depends on the application you are working on that decides if stemmers should be used or lemmatizers.
