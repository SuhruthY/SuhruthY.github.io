---
title: Sampling from a Population and its influence on its Estimates
layout: post
post-image: https://images.pexels.com/photos/2833373/pexels-photo-2833373.png?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940
description: A data distribution is a function or a listing which shows all the possible values (or intervals) of the data. It also (and this is important) tells you how often each value occurs. Often, the data in a distribution will be ordered from smallest to largest, and graphs and charts allow you to easily see both the values and the frequency with which they appear.
tags:
- sample
- probability
- center
---

&nbsp;&nbsp;&nbsp;&nbsp;Let's say you are one of the researchers at *WhY Stats High School* and were assigned the task to study the selection behavior of its students.

&nbsp;&nbsp;&nbsp;&nbsp;So you conducted an experiment in which each individual will pick n no of balls from a bowl full of 50 colored balls.

&nbsp;&nbsp;&nbsp;&nbsp;Does this experiment correct? If not why? How can we improve it? 

&nbsp;&nbsp;&nbsp;&nbsp;In the next few minutes we are going to answer these questions.

## Population Parameter vs Statistic Sample
&nbsp;&nbsp;&nbsp;&nbsp;The field of inferential statistics enables you to make educated guesses about the numerical characteristics of large groups. The logic of sampling gives you a way to test conclusions about such groups using only a small portion of its members.

&nbsp;&nbsp;&nbsp;&nbsp;These large groups are called *Population of Interest* and the small protions are the *Sample of Study*.

&nbsp;&nbsp;&nbsp;&nbsp;The following table illustrated the idea of taking a sample from a population.

<table><thead><tr><th>Population</th><th>Sample</th></tr></thead><tbody><tr><td>Advertisement for IT jobs in Hyderabad</td><td>The top 50 google searches for Advertisements for IT jobs in Hyderabad in past decade </td></tr><tr><td>Songs from the a popular Indian Song Contest</td><td>Song list of all of the winning songs from the Shankar Mahadev Contest every year</td></tr><tr><td>Undergraduate Students in Delhi</td><td>330 undergraduate students from the University of Delhi who volunteer for the study</td></tr><tr><td>All the Countries over the world</td><td>Recently updated data of all the countries listed in the official Government website</td></tr></tbody></table>

&nbsp;&nbsp;&nbsp;&nbsp;we can determine the various measures such as mean, median, standard deviation, etc of the population using the sample we have in our hands.

<div  style="background:#F5F5F5;padding:.5em .5em .5em .5em;text-align:center">
<p style="font-size:21px;font-weight:bold">Terminology Alert!</p>
<p>A <strong>Parameter</strong> is any measured quantity of a statistical population that summarises or describes an aspect of the population  </p>
<p>Whereas</p>
<p>A <strong>Statistic</strong> is an estimate of the population parameter using a small sample drawn out of the population.</p>
</div>

&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;In other words we can estimate population parameters using the sample statistic. 

&nbsp;&nbsp;&nbsp;&nbsp;But how confident we are that the statistic is a true estimate of the parameter.

<div style="background:#F5F5F5;padding:.5em .5em .5em .5em;">
<p align="center" style="font-size:18px;font-weight:bold">Story Time: Mom and Chicken</p>
<p>Your mom is cooking something in the kitchen and you can smell it far from your room.</p>
<p>You ran towards the kitchen, saw Juicy, Tender Roasted Chicken almost finished, and felt like eating.</p>
<p>Suddenly your mom takes a piece of it and asks you &quot;Do you wanna taste?&quot;</p>
<p>No more second thoughts, you grabbed the piece and ate it...felt like...<strong>DELICIOUS</strong></p>
</div>

&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;As we saw in the story *tasting a single piece of chicken*(statistic) made you believe/estimate the *overall taste of the roasting chicken*.

&nbsp;&nbsp;&nbsp;&nbsp;But what made it true estimate?

&nbsp;&nbsp;&nbsp;&nbsp;Yup! randomly sampling a single piece from the whole made it accurate to infer about.

&nbsp;&nbsp;&nbsp;&nbsp;There are many methods of sampling such as simple random sampling, stratified sampling, cluster sampling, systematic sampling, etc... etc...etc... which is out of the scope of this post.

&nbsp;&nbsp;&nbsp;&nbsp;What ever the type of sample it should be a representative of the required population that we are about to study.  

### Experiment: Pick 21 Balls
&nbsp;&nbsp;&nbsp;&nbsp;Now let's get back to our example... did you remember it!

&nbsp;&nbsp;&nbsp;&nbsp;So to ensure that the sample is a random one you placed the bowl in an empty room and make sure only one person a time enters the room.

<p align="center" style="font-size:21px;font-weight:bold">Wait!</p>

&nbsp;&nbsp;&nbsp;&nbsp;Soon you found that most of the people picked up green balls more than red ones.

&nbsp;&nbsp;&nbsp;&nbsp;Why is the bias happening? Are we doing anything wrong? 

<div style="background:#F5F5F5;padding:.5em .5em .5em .5em;">
<p align="center" style="font-size:18px;font-weight:bold">Story Time: Sample Bias</p>
<p>The time is World War-&#8545; in England. In a dimly lit Quonset hut, the Royal Air Force crews gather having just returned from a bombing run over Germany.</p>
<p>The debriefing begins with a moment of silence for the flight crews who did not return, then the lieutenant asks the returning flight crews, from which direction did the fatal attacks come? </p>
<p>The pilots respond to the man &quot;We were attacked from above and behind&quot;. It&#39;s unanimous. The lieutenant scribbles this on a piece of paper and hands it to one of them and instructs &quot;Take this information to our department flight crew. This may save lives&quot;.</p>
<p>But as he is leaving the dimly lit Quonset hut, a hand reaches from the inky shadows and says...<strong>"STOP!</strong></p>
<p align="center" style="font-weight:bold">No, that info may cost lives"</p>
</div>

&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;So what is wrong with it?

&nbsp;&nbsp;&nbsp;&nbsp;All we know is that those who *survived* were attacked from above and behind. Those who died may have been attacked from a different direction.

### Experiment Continues: Randomly Picking Balls
&nbsp;&nbsp;&nbsp;&nbsp;To ensure that people pick the balls randomly you will blindfold the people before entering the room and give instructions on where the bowl is.

&nbsp;&nbsp;&nbsp;&nbsp;This way you found that the sample picked had much less bias compared to the previous case.

&nbsp;&nbsp;&nbsp;&nbsp;But, how will you estimate this is true for the population?
&nbsp;   

| Population Mean | Sample Mean |
|:---------------:|:------------|
|     <img src="https://latex.codecogs.com/svg.image?\dpi{200}\mu&space;=&space;\frac{\sum_{i=1}^{N}x_{i}}{N}" title="\dpi{200}\mu = \frac{\sum_{i=1}^{N}x_{i}}{N}" />    |    <img src="https://latex.codecogs.com/svg.image?\dpi{200}\bar{X}&space;=&space;\frac{\sum_{i=1}^{n}x_{i}}{n}" title="\dpi{200}\bar{X} = \frac{\sum_{i=1}^{n}x_{i}}{n}" />         |

&nbsp;  

Lets say there were 12 red balls, 8 green balls, 14 blue balls and 16 pink balls in our bowl.

Hence on an average the average ratio of all categories picked by a person is in the range of 6.25 - 12.25 then it is probably the true estimate.

> Note: Any 
