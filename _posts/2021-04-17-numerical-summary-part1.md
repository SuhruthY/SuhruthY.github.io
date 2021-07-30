---
title: "Numerical Summary Part-&#8544;: Understanding Measures of Central Tendency"
layout: post
post-image: https://blog.masterofproject.com/wp-content/uploads/2017/08/3.9-f-750x410.jpg
description: In descriptive statistics, summary statistics are used to summarize a set of observations, in order to communicate the largest amount of information as simply as possible. 
tags:
- mean
- median
- mode
---

>"If your boss asks you a report on this quarter's sales numbers and is rushing to a meeting and has time to listen to one piece of information about that data, that piece of information you give her should probably be a *measure of central tendency*" states Adriene Hill, crash course statistics.

&nbsp;&nbsp;&nbsp;&nbsp;A **measure of central tendency** is a single value that describes the way in which a group of data cluster around a central value. To put in other words, it is a way to describe the center of a data set.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- It condenses the data set down to one representative value.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- It also allows you to compare one data set to another or a piece of data to entire dataset.  

&nbsp;&nbsp;&nbsp;&nbsp;There are three measures of central tendency namely *mean*, *medain* and *mode*.  

&nbsp;&nbsp;&nbsp;&nbsp;Upnext we are going to talk about them in greater level of detail.  

## Working with samples
&nbsp;&nbsp;&nbsp;&nbsp;A sample is set of data points taken out from the given population which represents the population as a whole.   
  
&nbsp;&nbsp;&nbsp;&nbsp;Let's say you wanna study Advertisements for IT jobs in the Netherlands and found the data of top 50 search results for Ads for IT jobs in the Netherlands on May 1, 2020. This isn't the whole population, instead a small sample that represents it.


## Mean: The average value 
&nbsp;&nbsp;&nbsp;&nbsp;As commonly known mean or the average is simply *the sum of all data points divided by the number of data points in the sample*.
  
&nbsp;&nbsp;&nbsp;&nbsp;For example, A cricketer's scores in five ODI matches are as follows: 12, 34, 45, 50, 24. The *arithmetic mean* of data is given by

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{200}\textbf{Mean},&space;\bar{x}&space;=&space;\frac{sum\;of\;all\;observations}{total\;no\;of\;observations}&space;=&space;\frac{\sum_{i=1}^{n}x_{i}}{n}&space;=&space;\frac{x_{1}&plus;x_{2}\cdots&plus;x_{n}&space;}{n}" title="\dpi{200}\textbf{Mean},&space;\bar{x}&space;=&space;\frac{sum\;of\;all\;observations}{total\;no\;of\;observations}&space;=&space;\frac{\sum_{i=1}^{n}x_{i}}{n}&space;=&space;\frac{x_{1}&plus;x_{2}\cdots&plus;x_{n}&space;}{n}" /></p>
&nbsp;&nbsp;&nbsp;&nbsp;In this case,
<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{200}\bar{x}&space;=&space;\frac{12&plus;34&plus;45&plus;50&plus;24}{5}&space;=&space;\frac{165}{5}&space;=&space;33" title="\dpi{200}\bar{x} = \frac{12+34+45+50+24}{5} = \frac{165}{5} = 33" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;So on an average the cricketer scores **33**.  
&nbsp;  
&nbsp;&nbsp;&nbsp;&nbsp;Wait a minute...

&nbsp;&nbsp;&nbsp;&nbsp;Did you noticed that I said **arthmetic mean**...that mean there are other ones.

&nbsp;&nbsp;&nbsp;&nbsp;Yes, there are other ones which we won't use that much. But let's take a look at them.

#### Geometric Mean: 
&nbsp;&nbsp;&nbsp;&nbsp;The Geometric Mean is a special type of average where we multiply the numbers together and then take a square root (for two numbers), cube root (for three numbers) etc. It is given by  

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{300}GM=&space;\left&space;(&space;\prod_{i=1}^{n}x_{i}&space;\right&space;)^\frac{1}{n}&space;=&space;\sqrt[n]{x_1&space;x_2&space;\cdots&space;x_n}" title="\dpi{300}\bar{x}&space;=&space;\left&space;(&space;\prod_{i=1}^{n}x_{i}&space;\right&space;)^\frac{1}{n}&space;=&space;\sqrt[n]{x_1&space;x_2&space;\cdots&space;x_n}" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;The Geometric Mean is useful when we want to compare things with very different properties.

&nbsp;&nbsp;&nbsp;&nbsp;Consider a stock that grows by 10% in year one, declines by 20% in year two, and then grows by 30% in year three. The geometric mean of the growth rate is calculated as follows:

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{200}GM=&space;\sqrt[3]{(1&plus;0.1)(1-0.2)(1&plus;0.3)}&space;=&space;\sqrt[3]{10.1}&space;=&space;1.0458&space;" title="\dpi{200}\bar{x}= \sqrt[3]{(1+0.1)(1-0.2)(1+0.3)} = \sqrt[3]{10.1} = 1.0458 " /></p>

&nbsp;&nbsp;&nbsp;&nbsp;This implies the growth rate is **46%**.

#### Harmonic Mean:
&nbsp;&nbsp;&nbsp;&nbsp;The Harmonic mean is simply reciprocal of the average of the reciprocals.

&nbsp;&nbsp;&nbsp;&nbsp;It is used for calculating mean data is obtained by combining two scales.   

&nbsp;&nbsp;&nbsp;&nbsp;In particular cases, especially those involving rates and ratios, the harmonic mean gives the most correct value of the mean. It is given by 

<p align="center"><img src="https://latex.codecogs.com/svg.image?HM&space;=&space;\frac{n}{\sum_{i=1}^{n}\frac{1}{x_{i}}}&space;=&space;\frac{n}{&space;\frac{1}{x_{1}}&plus;\frac{1}{x_{2}}&plus;\cdots&space;&plus;\frac{1}{x_{n}}&space;&space;}" title="HM = \frac{n}{\sum_{i=1}^{n}\frac{1}{x_{i}}} = \frac{n}{ \frac{1}{x_{1}}+\frac{1}{x_{2}}+\cdots +\frac{1}{x_{n}} }" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;Let's say I travel 10 km at 60 km/h, than another 10 km at 20 km/h, what is my average speed?  

<p align="center"><img src="https://latex.codecogs.com/svg.image?HM&space;=&space;\frac{2}{\frac{1}{60}&plus;\frac{1}{20}}&space;=&space;\frac{2}{\frac{1}{15}}&space;=&space;&space;2&space;\cdot&space;15&space;=&space;30\;km/hr" title="HM = \frac{2}{\frac{1}{60}+\frac{1}{20}} = \frac{2}{\frac{1}{15}} = 2 \cdot 15 = 30\;km/hr" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;Yes! you got it right. It was 30 Kilometers per Hour.   

#### Outliers and its effect:
&nbsp;&nbsp;&nbsp;&nbsp;Some electric utilities companies allow homeowners to pay their electric bills by setting up budget billing. This budget billing figure is derived by the average electric bill over acertain period, usually the prior 12 months. 

&nbsp;&nbsp;&nbsp;&nbsp;The electric company, like PPL electric, will take twelve months of bills (Jan-Dec) of the prior year, add the total, and divide by 12. For example, the usage for the prior 12 months is shown below:

<table><thead><tr><th>Month</th><th>Jan</th><th>Feb</th><th>Mar</th><th>Apr</th><th>May</th><th>Jun</th><th>Jul</th><th>Aug</th><th>Sep</th><th>Oct</th><th>Nov</th><th>Dec</th></tr></thead><tbody><tr><td>Amount</td><td>$135</td><td>$145</td><td>$112</td><td>$101</td><td>$98</td><td>$87</td><td>$116</td><td>$121</td><td>$113</td><td>$107</td><td>$126</td><td>$131</td></tr></tbody></table>

&nbsp;&nbsp;&nbsp;&nbsp;What is the average of this homeowner’s electric bill for this given year? 

<p align="center"><img src="https://latex.codecogs.com/svg.image?Average\;Bill&space;=&space;\frac{135&plus;145&plus;112&plus;101&plus;98&plus;87&plus;116&plus;121&plus;113&plus;107&plus;126&plus;131}{12}" title="Average\;Bill = \frac{135+145+112+101+98+87+116+121+113+107+126+131}{12}" /></p> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://latex.codecogs.com/svg.image?=&space;116" title="= 116" />

&nbsp;&nbsp;&nbsp;&nbsp;The average electric bill for this house is **$116**.

&nbsp;&nbsp;&nbsp;&nbsp;What would happen if a heat wave hit in August and the family’s electrical bill for the month increased to $449? By how much would this affect their budgeted amount?

&nbsp;&nbsp;&nbsp;&nbsp;Now the calculation would be

<p align="center"><img src="https://latex.codecogs.com/svg.image?Average\;Bill&space;=&space;\frac{135&plus;145&plus;112&plus;101&plus;98&plus;87&plus;116&plus;\textbf{449}&plus;113&plus;107&plus;126&plus;131}{12}" title="Average\;Bill&space;=&space;\frac{135+145+112+101+98+87+116+\textbf{449}+113+107+126+131}{12}" /></p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://latex.codecogs.com/svg.image?=&space;143" title="= 143" />

&nbsp;&nbsp;&nbsp;&nbsp;With a heat wave the average electrical bill for this house will increase to $143.

&nbsp;&nbsp;&nbsp;&nbsp;Here the abnormal bill value is called an *outlier*.

> In statistics, an **outlier** is a data point that differs significantly from other observations. An outlier may be due to variability in the measurement or it may indicate experimental error.

&nbsp;&nbsp;&nbsp;&nbsp;Mean is robust to ouliers.

&nbsp;&nbsp;&nbsp;&nbsp;Hence we use another measure called *Median*  


## Median: The middle value of the data
&nbsp;&nbsp;&nbsp;&nbsp;In statistics and probability theory,    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;the median is the value separating the higher half from the lower half of a data sample.

&nbsp;&nbsp;&nbsp;&nbsp;So the median value is given by

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{200}Median,\;M&space;=&space;\left\{\begin{matrix}&space;&space;X(\frac{n&plus;1}{2})\;\;if\;n\;is\;odd&space;&space;\\&space;&space;\\\frac{X(\frac{n}{2})&plus;X(\frac{n}{2}&plus;1)}{2}\;\;if\;n\;is\;even\end{matrix}\right." title="\dpi{200}Median,\;M = \left\{\begin{matrix} X(\frac{n+1}{2})\;\;if\;n\;is\;odd \\ \\\frac{X(\frac{n}{2})+X(\frac{n}{2}+1)}{2}\;\;if\;n\;is\;even\end{matrix}\right." /></p>
<p align="right" style="margin-right:2em;font-style:italic">where <span style="font-weight:bold">n</span> is the number of observations</p>

&nbsp;&nbsp;&nbsp;&nbsp;Let's say the number of slices of pizza that each person at Thorton's birthday party ate were 4, 5, 3, 2, 13, 1, 3.

&nbsp;&nbsp;&nbsp;&nbsp;What does the middlemost value interpret?

&nbsp;&nbsp;&nbsp;&nbsp;In order to calcuate the median, first let's sort the numbers as follows: 1, 2, 3, *3*, 4, 5, 13

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{300}Median&space;=&space;X(\frac{7&plus;1}{2})&space;=&space;X(4)=&space;3" title="\dpi{300}Median = X(\frac{7+1}{2}) = X(4)= 3" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;So it seems like half of the people ate less than *3* slices and other more than *3*.

&nbsp;&nbsp;&nbsp;&nbsp;That's it! Wait a minute...

&nbsp;&nbsp;&nbsp;&nbsp;After sometime Thorton was checking his birthday stats and He was suprised...4, 5, 3, 2, **13**, 1, 3.

<p align="center" style="font-size:42px">Who ate 13 slices?</p>

&nbsp;&nbsp;&nbsp;&nbsp;Then we found that there were two people of same name recorded as a single person and they ate each of 6 and 7 slices.

&nbsp;&nbsp;&nbsp;&nbsp;Now if we arrange the data points again: 1, 2, 3, 3, 4, 5, 6, 7  and median is given by

<p align="center"><img src="https://latex.codecogs.com/svg.image?\dpi{200}Median&space;=&space;\frac{X(\frac{8}{2})&plus;&space;X(\frac{8}{2}&plus;1)}{2}&space;=&space;\frac{X(4)&plus;X(5)}{2}=&space;\frac{3&plus;4}{2}&space;=&space;3.5" title="\dpi{200}Median = \frac{X(\frac{8}{2})+ X(\frac{8}{2}+1)}{2} = \frac{X(4)+X(5)}{2}= \frac{3+4}{2} = 3.5" /></p>

&nbsp;&nbsp;&nbsp;&nbsp;So we now know the central value is 3.5(although no one ate 3.5 slices).

&nbsp;&nbsp;&nbsp;&nbsp;This is where *mode comes* into picture.

## Mode: The most frequent value
&nbsp;&nbsp;&nbsp;&nbsp;A mode, in statistics, is defined as the value that has higher frequency in a given set of values. It is the value that appears the most number of times.

&nbsp;&nbsp;&nbsp;&nbsp;Below your seeing 200 children favorite flavor of ice cream amoung vanilla, chocolate or strawberry encodes as 1, 2, and 3 respectively.

1, 3, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 1, 1, 3, 3, 3, 1, 1, 3, 1, 1, 2, 1, 3, 1, 2, 1, 2, 1, 2, 1, 3, 2, 3, 1, 2, 3, 3, 1, 1, 2, 3, 1, 1, 3, 3, 1, 3, 1, 2, 1, 3, 2, 3, 3, 1, 1, 2, 2, 1, 1, 2, 2, 1, 3, 2, 1, 3, 1, 2, 1, 3, 3, 1, 2, 1, 1, 2, 1, 3, 2, 2, 2, 1, 1, 3, 2, 1, 1, 3, 2, 1, 1, 1, 1, 1, 3, 3, 1, 1, 1, 3, 1, 1, 2, 3, 2, 3, 1, 1, 1, 1, 1, 3, 3, 1, 1, 2, 2, 3, 1, 3, 3, 2, 2, 1, 3, 1, 1, 1, 2, 1, 3, 2, 2, 3, 3, 2, 3, 3, 1, 1, 1, 1, 3, 2, 1, 2, 2, 1, 2, 3, 1, 1, 3, 1, 1, 3, 1, 3, 3, 1, 1, 3, 1, 1, 3, 3, 3, 3, 1, 3, 3, 2, 1, 2, 2, 1, 3, 3, 1, 2, 3, 1, 2, 2, 1, 2, 1, 2, 3, 3, 1, 2, 1, 1, 1, 2

&nbsp;&nbsp;&nbsp;&nbsp;What is the most liked flavor?

&nbsp;&nbsp;&nbsp;&nbsp;Yes! you were right. But how to calculate the mode.

&nbsp;&nbsp;&nbsp;&nbsp;Unlike mean and median there isn't any standard formula for mode. 

&nbsp;&nbsp;&nbsp;&nbsp;So lets create a simple frequency table:


| Flavor    | Vanilla | Chocolate | Straberry |
|-----------|---------|-----------|-----------|
| Frequency |      95 |        58 |        47 |

&nbsp;&nbsp;&nbsp;&nbsp;Hence most of the children likes **Vanilla**

&nbsp;&nbsp;&nbsp;&nbsp;Normally, the mode is used for categorical data.

With this we come to the end of the topic. In the next part we are going to see about *Variablity* in a sample.
