---
title: Getting access to Social Media APIs
layout: post
post-image: https://cdn.searchenginejournal.com/wp-content/uploads/2014/10/API-economy_720-720x400.jpg
description: Application Programming Interface(API) is an intermidiary which enables data exchange between a service and it's user. In order to access the data from API one needs to authenticate which is the topic of this markdown.
tags:
- API
- data science
- social media
---

If you are a noob to API's I recommend to watch one of this first : [Getting started with APIs] [1]

## Social Media and API
&nbsp;&nbsp;&nbsp;&nbsp;Social media are interactive Web 2.0 Internet-based applications. User-generated content such as text posts or comments,
digital photos or videos, and data generated through all online interactions is the lifeblood of social media.
Social media also started creating APIs to share their data with third-party application developers and became source for data mining. 

&nbsp;&nbsp;&nbsp;&nbsp;There are mainly two types of APIs:   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**RESTful API:**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- REST Stands for Representational State Transfer which relies on HTTP protocol for data transfer.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Services Provided are    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*GET*: recieve data from server     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*POST*: write data to the server  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Stream API:**   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Used to collect data in real time.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Data is similar to REST APIs  

## Authentication and Authorization 
&nbsp;&nbsp;&nbsp;&nbsp;Let's say you were alone in your home, suddenly the doorbell rang. You opened the door and found that its was your friend.
As it was your friend, you felt happy and invited him into your home. Now think about what are the things he can use? can he enter you bedroom or 
eat something in your kitchen that is made for you? Will you allow him to do so? What if it's not your friend and some stranger?  
Here your home is an API and the visitor is an user.

![Authenticate_vs_Authorize][2]

&nbsp;&nbsp;&nbsp;&nbsp;*Authentication* is an act of validating the user. Usernames, Passwords, One-time pins(OTP), 
Authentication apps, Biometrics, etc are some authentication factors.  
&nbsp;&nbsp;&nbsp;&nbsp;*Authorization* is a process of giving the user permission to access a specific resource. In 
order to authorize one must be authenticated.

Now let's see some practical implementations


#### Necessary Libraries
```python
import os
import json
import requests
import webbrowser

import tweepy

from requests_oauthlib import OAuth1
```  
&nbsp;

In a situation when you want your variables to be kept secret to the other users, the python library [*dotenv*][5] is very useful.
  
#### Global Variables
```python
# loading  environmental vars
from dotenv import load_dotenv

folder_path = os.path.expanduser('../data/')  
load_dotenv(os.path.join(folder_path, '.env'))
```
---
    True  
  
&nbsp;  
  
#### AUTHENTICATION
&nbsp;&nbsp;&nbsp;&nbsp;Tweepy makes it easier to use the twitter streaming api by handling authentication, connection, creating and destroying the session, reading incoming messages, and partially routing messages.  

```python
consumer_key = os.getenv("TWITTER_API_KEY")
consumer_secret = os.getenv("TWITTER_API_SECRET")

callback_URL = "oob"

oauth = tweepy.OAuthHandler(consumer_key, consumer_secret, callback_URL)

redirect_URL = oauth.get_authorization_url()

webbrowser.open(redirect_URL)
```
---
    True  
    
&nbsp;  

&nbsp;&nbsp;&nbsp;&nbsp;After running the above code you will be redirected to this page as shown below  

![tweepy authorize][3]

click the authorize button and then you will be provided with a pin as shown below

![tweepy authorize2][4]

saving the pin for future use 

```python
PIN = input("Enter the PIN: ")
```
---
    Enter the PIN: 9210359
    
&nbsp;  
 
Using  the pin above we can get the access token and the access secret as shown below      
```python
access_token, access_secret = oauth.get_access_token(PIN)
```

#### Extracting  data
&nbsp;&nbsp;&nbsp;&nbsp;Let's collect some tweets from our API  

```python
# url's
url = "https://api.Twitter.com/1.1/search/tweets.json"

# parameters
qry = "premier league -filter:retweets AND -filter:replies"
pms = {"q" : qry, "count" : 100, "lang" : "en", 
       "result_type": "recent"}

auth = OAuth1(consumer_key, consumer_secret, access_token, access_secret)

res = requests.get(url, params = pms, auth=auth)

tweets = res.json()

for status in tweets["statuses"][:10]:
    print(status["text"])
    print("--------------------------------")
```
---
    Man city will win again,looking for partners, new premier league champion medals. https://t.co/02d8FzEtZ9
    --------------------------------
    #Terry and #Carvalho be the greatest CB partnership for the Premier League history.
    
    •Dem concede only15 goals in 3… https://t.co/Y9Yyw9XEUv
    --------------------------------
    There’s no Premier League this weekend so instead we’ve previewed three international games, with odds from… https://t.co/p0zUdT7PGQ
    --------------------------------
    How hard is it for every premier league player to put 1% of their wages forward to a group who will work on feeding… https://t.co/V2pGOcb40f
    --------------------------------
    LIVE: Nile Special Stout Rugby Premier League Matchday Four #NileStoutRugby 
    https://t.co/bIhZP8HnLl
    --------------------------------
    GOAL! Blackburn U18 in England Premier League U18
    Middlesbrough U18 0-1 Blackburn U18
    --------------------------------
    Weekend without premier league everything become difficult am even falling in love just 14 hours am in love 🙄🤸‍♂️🤸‍♂️🤸‍♂️
    --------------------------------
    There is no Premier League this weekend and I hate it.
    --------------------------------
    Never Miss The Action With https://t.co/Z4GIY7IONU
    Catch The Indian Premier League - Starting Starting 07 April 202… https://t.co/X8FISJYuW4
    --------------------------------
    Man Utd legend Sir Alex Ferguson admits some of his transfers ‘weren  👨 #cristianoronaldo #siralexferguson https://t.co/n23i26VMdl
    --------------------------------

&nbsp;  
Various APIs have various ways to authenticate. They may differ in their endpoint url's, parameters, queries provided, etc.
But the process is same as follows.    

[1]: https://www.youtube.com/results?search_query=getting+started+with+api
[2]: https://nordicapis.com/wp-content/uploads/What-is-the-Difference-Between-Authorization-and-Authentication-.png
[3]: ../assets/images/Social_APIs/tweepy.png
[4]: ../assets/images/Social_APIs/tweepy2.png
[5]: https://stackoverflow.com/questions/41546883/what-is-the-use-of-python-dotenv
