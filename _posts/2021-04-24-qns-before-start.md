---
title: 21 Questions you should ask before starting a DataDriven Project
layout: post
post-image: https://images.pexels.com/photos/2726370/pexels-photo-2726370.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940
description: A data-driven approach enables companies to examine and organise their data with the goal of better serving their customers and consumers. By using data to drive its actions, an organisation can contextualise and/or personalise its messaging to its prospects and customers for a more customer-centric approach.
tags:
- problem statement
- data science
- Over The Top
---
&nbsp;&nbsp;&nbsp;&nbsp;Let's say there are two OTT platforms such as *Netflix* and *Amazon* namely A and B. Company-A uses an advanced AI powered technology to retained its customers, recommend shows and movies, analyze user demographics, etc and is one of the top streaming platforms now a days.

&nbsp;&nbsp;&nbsp;&nbsp;Where as company-B is having a tough time figuring ways to increase its annual revenue and provide best experience to their users. Assume you are a data scientist or an analyst and are given this task to complete...

&nbsp;&nbsp;&nbsp;&nbsp;In this post we are going to explore how we are going to tackle a business problem and turn it into a data science task. 

## Understanding the Problem
&nbsp;&nbsp;&nbsp;&nbsp;First and the foremost thing that we should do is to know the goals of the business inorder to have a solution.

&nbsp;&nbsp;&nbsp;&nbsp;As the information provided to you will be the basis for your analysis. So take your time and make sure to get all the information you need from the domain expert.

>&nbsp;&nbsp;&nbsp;&nbsp;"It’s necessary to accurately define the data problem that is to be solved. _The problem should be **clear**, **concise**, and **measurable**_. Many companies are too vague when defining data problems, which makes it difficult or even impossible for data scientists to translate them into machine code" - Brainhub

&nbsp;&nbsp;&nbsp;&nbsp;The things that we have to focus is the main problems that a client(in this case a company) is facing, resources that are given to us, benefits of solving the issue, and risks may occur.

&nbsp;&nbsp;&nbsp;&nbsp;Going back to the problem that we were solving, It states that company-B needs to improve their income by using big data and AI. There also mentioned that another company-A uses data analytics for their betterment.

&nbsp;&nbsp;&nbsp;&nbsp;Below is a video showing you how *Netfilx* uses data  

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/sAQmj8a_aI8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

&nbsp;&nbsp;&nbsp;&nbsp;With this you may understood what we are trying to do...Yes! a _**RECOMMENDATION SYSTEM**_.

&nbsp;&nbsp;&nbsp;&nbsp;I do agree there are many more thing that we can do to improve a company revenue. But in this case this is one of the most feasible option.

## Converting to a data science task
>&nbsp;&nbsp;&nbsp;&nbsp;A problem statement generally follows the format:  
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“*The problem P, has the impact I, which affects B, so a good starting point would be S*.” 

&nbsp;&nbsp;&nbsp;&nbsp;After you thoroughly understood the goals of the company-B then you have to make your own data driven statements that will lead to insights.

&nbsp;&nbsp;&nbsp;&nbsp;I believe this task is completely an individual task, nevertheless I will help you in doing so.

<p align="center"><img width="300" src="https://latex.codecogs.com/svg.image?\\\textbf{Business&space;Goals}&space;\Rightarrow&space;\textbf{Data&space;Goals}" title="\\\textbf{Business Goals} \Rightarrow \textbf{Data Goals}" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;I think of this as narrowing the big problem statement into smaller statements that include some data science jargon such as cleaning, models, classification, etc.

&nbsp;&nbsp;&nbsp;&nbsp;In our case we can determine the features that can determine user niche such as time stamp of pausing and watching a video, date, time and place(zip code) of watch, rating provided, searhes, browsing and scrolling behavior, etc and then recommend them accordingly.

<p align="center">or</p>

&nbsp;&nbsp;&nbsp;&nbsp;Classification of each user into which genre does he/she is mostly likely to be interested in watching at an instance. And then recommend those genres at the top of the list to the user.

#### Data Scarcity:
&nbsp;&nbsp;&nbsp;&nbsp;Yeah, I agree there isn't low amounts of data anymore in this **BIG DATA** age.

&nbsp;&nbsp;&nbsp;&nbsp;But I'm  taking about the scarcity that occurs while choosing data suitable to the problem.

&nbsp;&nbsp;&nbsp;&nbsp;I recommend starting with small datasets and then increase its volume further with the requirements.

### Exploring the data goals
&nbsp;&nbsp;&nbsp;&nbsp;After successfully defining your data goals you will still able to ask questions at various stages of your workflow.

&nbsp;&nbsp;&nbsp;&nbsp;One such stage is *Exploratory Data Anlaysis(EDA)*.

&nbsp;&nbsp;&nbsp;&nbsp;Data visualization tools like *Qlik* or *Tableau* typically have capabilities to directly access several kinds of structured and unstructured data sources, so they can be applied on top of raw data and are extremely effective in identifying trends, anomalies, outliers in analyzed data with a productivity level not comparable to a classical tabular approach.

&nbsp;&nbsp;&nbsp;&nbsp;You will find never before insights about data while performing EDA and which will further helpful in the model building or inference process.

&nbsp;&nbsp;&nbsp;&nbsp;In the view of company-B, it could be narrowing down our analysis to a specific group of users or TV shows. Or it may also lead us to change the whole data goals that we decided before.

With this we came to the end... wait!

What about the 

<p align="left" style="font-size:40px;font-weight:bold">21 questions</p>

Questions are not specific they vary from one problem to other. It is you who need to figure them out. 

But I told you I will help you... Here you go

<div style="background:#F5F5F5;padding:.5em .5em .5em .5em;">

<p align="center" style="font-size:21px;font-weight:bold">Recommendation System</p>

<h3 id="business-goals">Business Goals</h3>
<ol>
<li>What is the main objectives or goals that <em>company-B</em> wants to achieve?</li>
<li>What are the expectations of the <em>company-B</em>?</li>
<li>What are the positive and negative impacts of solving the task?</li>
<li>What are the potential and personal risks that may occur?</li>
<li>Are the goals fall into the short term or can long term?</li>
<li>What is the point of view or perspective of the <em>subscribers</em>?</li>
<li>Do I have perfect domain knowledge? If not who is the domain expert?</li>
</ol>
<p>converting to data terms...</p>
<ol>
<li>What are the popular <em>TV shows or Movies</em> streaming in both <em>B</em> and <em>A</em>?</li>
<li>What does <em>company-B</em> lacks in terms of <em>A</em>?  </li>
<li>What are the similarities and differences between <em>B</em> and <em>A</em>?</li>
<li>What are the peak hours of streaming in <em>B</em>? Do they converge with <em>A</em>?</li>
<li>What is the average subscriber stats of the <em>company-B</em>?</li>
<li>Can we create some clusters based on subscriber stats?</li>
<li>Is our data sufficient to solve the individual goals?</li>
</ol>
<p><strong>Problem Statement</strong>: The lack of customer recommendation in <em>company-B</em>, has an impact on their annual revenue, which affects the company growth, so a good starting point would be comparing with its competitor <em>company-A</em>.</p>
<p>While EDA...</p>
<ol>
<li>Which age bins of subscribers will need more attention?</li>
<li>Who are the top-n user based on categories?</li>
<li>What are the important features?</li>
<li>Which algorithm is best for training?</li>
<li>What are some trends in the features?</li>
<li>Is a feature correlated with the other?</li>
<li>Do null values should be imputed or left ignored?</li>
</ol>

</div>  

&nbsp;  
Nevertheless questions may vary... but who makes them do not and I say "you are the one"


