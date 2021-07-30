---
title: "Numerical Summary Part-&#8545;: Familiarizing Measures of Spread" 
layout: post
post-image: https://exploringyourmind.com/wp-content/uploads/2019/04/person-analyzing-statistics.jpg
description: In statistics, dispersion is the extent to which a distribution is stretched or squeezed. Common examples of measures of statistical dispersion are the variance, standard deviation, and interquartile range.
tags:
- Range
- IQR
- Standard Deviation
---

&emsp;In my previous post [Understanding Measures of Central Tendency][1], we talked about the center of a data sample.

&emsp;Now we will be going through how *spread* the data points are around its respective central measure.

&emsp;In general, there are three *measures of dispersion* or *spread* namely   
&emsp;&emsp;- *Range*   
&emsp;&emsp;- *IQR* and   
&emsp;&emsp;- *Standard Deviation*  

## Range: difference between the extremes
&emsp;In statistics *Range* is simply the difference between the highest data point the lowest data point in the sample.

&emsp;Steps to find out range   
&emsp;&emsp;- Arrange the given data points in ascending order  
&emsp;&emsp;- Identify the largest and the smallest data point in the sample.  
&emsp;&emsp;- Then the range of the sample is given by **Range** = **Maximum** - **Minumum**  
  
<div align="center" style="background:#f5f5f5;text-align:left;padding:.5em .5em;">
<h4 id="note-" align="center">Note!</h4>
<p>&emsp;The <em>range</em> function used in programming and the <em>Range</em> measure used in statistics are quite different. One defined a sequence of numbers and the other says about the spread amoung data values.  </p>
</div>

&nbsp;  
**_Eg-1 :_** The ages of 7 participants in a lemon and spoon competition conducted at the University of WhY stats in 2021 are as follows. Figure out the how much spread apart the ages are?  

| Participant | 1  | 2  | 3  | 4  | 5  | 6  | 7  |
|-------------|----|----|----|----|----|----|----|
| Age         | 37 | 19 | 31 | 29 | 26 | 33 | 21 |  

**sol:**    
&emsp;To find out the range let's arrange the ages in order

&emsp;| Age         | 19 | 21 | 26 | 29 | 31 | 33 | 37 |

&emsp;Here the highest age is *37* years and the lowest is *19* years and range is given by

<p align="center"><img src="https://latex.codecogs.com/svg.image?Range&space;=&space;\mathrm{37}&space;-&space;\mathrm{19}&space;=&space;\textbf{18}&space;" title="Range = \mathrm{37} - \mathrm{19} = \textbf{18} " /></p>

&nbsp;  
**_Eg-2 :_** Martin scores 67, 100, 93, 81, 96 in 5 different math test respectively. Find out the range of his overall math scores?  
**sol:**    
&emsp;Arranging martin scores,

&emsp;&emsp;&emsp;*67*&emsp;&emsp;81&emsp;&emsp;93&emsp;&emsp;96&emsp;&emsp;*100*   

&emsp;Here *100* and *67* are the maximum and minimum marks scored. Then the Range is   

<p align="center"><img src="https://latex.codecogs.com/svg.image?Range&space;=&space;\mathrm{100}&space;-&space;\mathrm{67}&space;=&space;\textbf{33}&space;" title="Range = \mathrm{100} - \mathrm{67} = \textbf{33} " /></p>

## Quartiles: divides into 4 parts
&emsp;In statistics, the quartiles are data points that divide the given sample into 4 equal parts. 

&emsp;Steps to find out the quartile:   
&emsp;&emsp;- Arrange the data points in ascending order.   
&emsp;&emsp;- Calculate the median of the data set which is the 2<sup>nd</sup> quartile.    
&emsp;&emsp;- Split the data into 2 parts such that they are left side and right side of the median.    
&emsp;&emsp;- Calculate median of the individual parts which are nothing but the quartiles.       
    
<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#0000ff&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-20T05:05:37.723Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;bXyKuSNJ_j16RZrGureE\&quot; version=\&quot;14.6.13\&quot;&gt;&lt;diagram id=\&quot;mbiEi7woB1OH0UeVKUZ0\&quot; name=\&quot;Page-1\&quot;&gt;7Vxdc6I6GP41vdwOJBDgsrXd9mI7s05nz8652kkhaHYjcRC/zq8/QYjyZY2KEnXtReUlBMj7PM+bNx/ewd5o8RLj8fCNB4TdASNY3MGnOwBMaEDxL7UsM4sDnMwwiGmQF9oY3ul/JDcauXVKAzIpFUw4Zwkdl40+jyLiJyUbjmM+LxcLOSvfdYwHpGZ49zGrW3/SIBnmVmAYmxOvhA6G8tYeyM+MsCydGyZDHPB5wQSf72Av5jzJvo0WPcLS1pMNk133dcvZ9ZPFJEpULvjz4+e/xq/ftP8wi+jvBScPMfpiGm5Wzwyzaf7O+eMmS9kIJAoe0rYURxGPhPFxmIyYODLF10mC46RyOqSM9Tjj8ep6GNrp36pszP+Qwhm0+qRX8Ch5z+/Y8Ga5acKnsU8+ex3TzkqSoOTXvEVeCB+RJF6KAvONN+3cQcOCH6UtJgwndFZGA85BNVhXt77Dd07FMwNDEsDJ68nhb0ncyCqyN8qvKjqvUhEyyxVBz7v3ip9ytcInA5LUqhVfCo2wMa2Qsg9q5NMcjJr9EdKIs7ZQ42qNmh3OVsWQQN/nYNyCGtHoeFkoNk4LTLY//rb7bECY1dgyJE0FSDImAkeKnPmQJuR9jFe4mIvYVYYnnoyzaBLSBQlaULTsuFAu+wj7VtjOSJyQxadwlA3uVfGSHxfgChrgCir+LyKzJBn7OwNcUFTJYK+CLU30YV3PsVHF9g5ThPZIi85I2gATN/QbAeO75CNsIG0L5IS2duR0LoicCsFbncZIKxpDcDU09q4KUcDSCic73auKE9OAWmUREv832GVzavlc11EBqPSfLyelA55qVJBNqinbW0r+atw/VfaHUBfZnwTrLUpJbbSgcymB19UdMJSlBGglJagsHbbXVjdiV/558o6DfbNs97RLJ8E5c3i9nGEa+nXjVJL7yx5RcWtZTOeNfl2TaPLpFQKeo1XAc9zWMuWuQ5zE+Il4XNXICtZCgvxGXgeO9yGaohUe1zOdrnkMz58DtzVFIfGiCRNPlMU6xl7V7p3Stt9TVRkZvc7OEdKupwqPzUv1GuKSlFcI055W4oBM497YfFzrc05bJ9KKSr3di4V5u2mtrV2fHlpHioVefXrPURULzZbQQSejre06wicmBHVSOyZAluUiy7aRfZhYtLO+bt+xcmtLvnLisXIVZF+nzLj6pRwqmn85MgOUZUazSXbXWhEemTZwXQuiBpkx01KGgyzTAYepzM4JeBcq6Ux7PQ6VgavrlIL6ItvOpeDYUcQOF0j+XUCtRwoBb3e8AWiXQnjnnIvRyxmWdurqXdccjdSw3drs6TVHA3dp84HDPTYo1SMj0sUM/ni3q9yWbrPo6+2dVyIWcuG7gljoNVJ8KrGw0KWIxRvu/fMyc+bL/tPYCF/j6Wxqf1GYpsxAJfcsgwo6h3iclhstBum27fuQ8bk/FIi9x1HEE+ExHv1Kr8GMDiJRkJFQOPaR4Q/CvvMJTQsIc5w5/HH1piR+npH0hbN7BDQWEpSVE25JH+NxizA0oFo9bbPqWgHdBkRaLYhFozNUlj9tpMJneDKhftkfjZxTapUzTdhUp1LcSmMqD7NWK6p6pb0Bj0Zf1TvkbySgOBI2Ib7A6Nd9J6CaVLW9qNcN4p6bJHl8kpJDGFLgUx+zh/zEiAYB2xbNYz6NgjR2PxnNkeAoGtmVVdrQrNOoiUVthNxmSVMYlL5WTUOWbprWMBP5lcaTlMmvmIUXQBLQgl+qG/S6J0k91nzDt+YVtxpDOvfKfvtpL7IHAG3vXk5OyNHPaoOqdgKa6kLn7Qc0zHv0zZrT9ONPG6G/tu0Ydc2f/XYPXyR/XCgwD2ozEMdSaUe1Z2ZVw37ePrwRVlWj0glZJQ43vxqW+W7z42vw+X8=&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
<p align="center">Figure-1 : 3 quartiles of 15 unknown data points</p>
</div>  

&nbsp;   
**_Eg-3 :_** The following were the hourly collections from a Salvation Army kettle at a local store one day in December: $19, $26, $25, $37, $32, $28, $22, $23, $29, $34, $39, and $31. Determine the first quartile and third quartile for the amount collected.    
**sol:**      
&emsp;First let's arrange the data points

&emsp;&emsp;&emsp;19&emsp;&emsp;22&emsp;&emsp;23&emsp;&emsp;24&emsp;&emsp;25&emsp;&emsp;*26*&emsp;&emsp;*28*&emsp;&emsp;31&emsp;&emsp;33&emsp;&emsp;34&emsp;&emsp;37&emsp;&emsp;39  
 
&emsp;Here there are even no of data points(i.e. n=12). So median is given by

&emsp;&emsp;&emsp;<img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(12/2)&plus;X(12/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(6)&plus;X(7)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{26&plus;28}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;27" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(12/2)+X(12/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(6)+X(7)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{26+28}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 27" />

&emsp;Now that over data is of 2 parts as shown

&emsp;&emsp;&emsp;19&emsp;&emsp;22&emsp;&emsp;23&emsp;&emsp;24&emsp;&emsp;25&emsp;&emsp;26&emsp;&emsp;&emsp;**27**&emsp;&emsp;&emsp;28&emsp;&emsp;31&emsp;&emsp;33&emsp;&emsp;34&emsp;&emsp;37&emsp;&emsp;39  

&emsp;Computing median for the 2 parts separately

|19&emsp;&emsp;22&emsp;&emsp;*23*&emsp;&emsp;*24*&emsp;&emsp;25&emsp;&emsp;26|28&emsp;&emsp;31&emsp;&emsp;*33*&emsp;&emsp;*34*&emsp;&emsp;37&emsp;&emsp;39| 

|<img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(6/2)&plus;X(6/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(3)&plus;X(4)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{23&plus;24}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;23.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(6/2)+X(6/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(3)+X(4)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{23+24}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 23.5" />|<img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(6/2)&plus;X(6/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(3)&plus;X(4)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{33&plus;34}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;33.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(6/2)+X(6/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(3)+X(4)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{33+34}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 33.5" />|                                                                              

&emsp;Therefore our new sequence with the quartiles would be 

&emsp;&emsp;&emsp;19&emsp;&emsp;22&emsp;&emsp;23&emsp;&emsp;&emsp;**23.5**&emsp;&emsp;&emsp;24&emsp;&emsp;25&emsp;&emsp;26&emsp;&emsp;&emsp;**_27_**&emsp;&emsp;&emsp;28&emsp;&emsp;31&emsp;&emsp;33&emsp;&emsp;&emsp;**33.5**&emsp;&emsp;&emsp;34&emsp;&emsp;37&emsp;&emsp;39  

&emsp;Hence $23.5 and $33.5 are the 1<sup>st</sup> and the 3<sup>rd</sup> quartiles respectively.

<div align="center" style="background:#f5f5f5;padding:.5em.5em;text-align:left;">
<h3 id="quartiles-as-percentile" align="center">Quartiles as Percentile</h3>
<p>&emsp;A percentile is a measure at which that percentage of the total values are the same as or below that measure.</p>
<p>&emsp;They divide the data into 100 equal parts.</p>
<p>&emsp;So we can say that quartiles divide the data into 25%, 50%, 75% and 100%.</p>
<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#0000ff&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-20T06:20:03.681Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;x_HEn_BK10E7UKP7UYM3\&quot; version=\&quot;14.6.13\&quot;&gt;&lt;diagram id=\&quot;prpuUI8UF7onrhmtAaKJ\&quot; name=\&quot;Page-1\&quot;&gt;5Vhdb9sgFP01flzlj+Amj23SrZu0aVM1tX0khtho2FgYx05//cDGX8FR2khZIi+JIjjABc6511xsecu4/MJhGn1nCFPLtVFpeSvLdX3gyn8F7GrA870aCDlBNeR0wBN5wxq0NZoThLNBR8EYFSQdggFLEhyIAQY5Z8Ww24bR4awpDLEBPAWQmugzQSLSqGvbXcMjJmHUTL1wdUsMm94ayCKIWNGDvAfLW3LGRF2KyyWmiryGmHrc5wOt7co4TsR7Buxewi345j9uyNeVeH7Lf/8o+CdtZQtprnfsAkv9qhWLXcODXHyqiriUc90jlq+rFkdWOMsThNUktqwVERH4KYWBai6kT0gsEjHVnTeE0iWjjFdmvQ1QX4WzRPTw+iPxTHD2p6VeWdALxlzg8iATTsuvdEzMYiz4TnbRA2ZzLYl2SsfxNVB0Gs80FPXUbTCovSpsTXe8y4Km/gMyuIYMwJ68DMC9Nhk8Q4bb6UcD8K9Nhpkhg2NPPxx8+9p0AIYOhgI4QXfqmJW1gMIsI8GQ2XoARsYpe5SV3qbByKYbjGMKBdkOzY8xoWf4yYic+PAzyGAzYzkPsB7WP16PWnL2LAnIQywMS5U07cZPV8sfOcolg5JsLDeQCCI125dP1JHTE6x27cbpE5bgvfjQEKQkTJTq0jKW+L3yfSITpzvdEBOE1DSjsTeMznMc6a2D9PxoPuJH7rmC53b6wWM8sU4OHtPSPw6e+cjJ/98Ej5EBXDx4FoYckj7Xp4rvtSqFqvTLmbAmRkTM35cNeOfSxDEvKaOieBMWxThlLi6KeWUBtvHgskeFkuN8GCuiknWWtgxNUjhvTzh7JLf2R4Tzzyacecn5cH6ASyJeFEk3QNdeey2rUvNXVXYDMo/nFHIh1dl91PculrmDxU3zdrG9MYFTk3fjDrxv6eT8Q1a7d3x19+5NqffwFw==&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
<p align="center">Figure-2 : Expressing quartiles as percentiles</p>
</div>

&nbsp;  
<p>&emsp;Note: Median is the 2<sup>nd</sup> quartile and also the 50<sup>th</sup> percentile.</p>
</div>

### Interquartile Range(IQR): Q3-Q1
&emsp;In statistics the *Interquartile Range* is the difference between the 3<sup>rd</sup> quartile and the 1<sup>st</sup> od the given data sample.
  
&emsp;Steps to find IQR:  
&emsp;&emsp;- As usual arrange the data in ascending order.  
&emsp;&emsp;- Find out the 3 quartiles of the data points.  
&emsp;&emsp;- Then the IQR for the data pointd is given by **IQR** = **Q3** - **Q1**  
  
**_Eg-4 :_** The marks scored by each students at WhY stats of two different tests are as follows. Compare them.   
  
&emsp;&emsp;&emsp;&ensp;Test Scores for *Test A*: 69, 96, 81, 79, 65, 76, 83, 99, 89, 67, 90, 77, 85, 98, 66, 91, 77, 69, 80, 94   
   
&emsp;&emsp;&emsp;&ensp;Test Scores for *Test B*: 90, 72, 80, 92, 90, 97, 92, 75, 79, 68, 70, 80, 99, 95, 78, 73, 71, 68, 95, 100  
**sol:**  
&emsp;To compare two samples with same characteristics we need to find some statistics. So let's find out the median.

&emsp;Arranging the two samples in order

| Test A| Test B|
| :---: | :---: |
| 65, 66, 67, 69, 69, 76, 77, 77, 79, *80*, *81*, 83, 85, 89, 90, 91, 94, 96, 98, 99<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(20/2)&plus;X(20/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10)&plus;X(11)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{80&plus;81}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;80.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(20/2)+X(20/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10)+X(11)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{80+81}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 80.5" />      | 68, 68, 70, 71, 72, 73, 75, 78, 79, *80*, *80*, 90, 90, 92, 92, 95, 95, 97, 99, 100<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(20/2)&plus;X(20/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10)&plus;X(11)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{80&plus;80}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;80" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(20/2)+X(20/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10)+X(11)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{80+80}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 80" />     |

&emsp;So median value of Test A scores is 0.5 more than Test B

&emsp;Does this mean  that students performed even worse in the 2<sup>nd</sup> test.

&emsp;Let's conform this mathematically using the IQR

&emsp;In test A

|  1<sup>st</sup> quartile(Test A) |  3<sup>rd</sup> quartile(Test A) | 
|:---:|:---:|
|65&emsp;&emsp;66&emsp;&emsp;67&emsp;&emsp;69&emsp;&emsp;*69*&emsp;&emsp;*76*&emsp;&emsp;77&emsp;&emsp;77&emsp;&emsp;79&emsp;&emsp;80<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10/2)&plus;X(10/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(5)&plus;X(6)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{69&plus;76}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;72.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10/2)+X(10/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(5)+X(6)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{69+76}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 72.5" /> |81&emsp;&emsp;83&emsp;&emsp;85&emsp;&emsp;89&emsp;&emsp;*90*&emsp;&emsp;*91*&emsp;&emsp;94&emsp;&emsp;96&emsp;&emsp;98&emsp;&emsp;99<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10/2)&plus;X(10/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(5)&plus;X(6)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{90&plus;91}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;90.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10/2)+X(10/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(5)+X(6)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{90+91}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 90.5" /> |                            
   
&emsp;So, the Interquartile Range is given by **IQR** = **90.5** - **72.5** = **18**   
    
&emsp;In test B

|  1<sup>st</sup> quartile(Test B) |  3<sup>rd</sup> quartile(Test B) | 
|:---:|:---:|
|68&emsp;&emsp;68&emsp;&emsp;70&emsp;&emsp;71&emsp;&emsp;*72*&emsp;&emsp;*73*&emsp;&emsp;75&emsp;&emsp;78&emsp;&emsp;79&emsp;&emsp;80<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10/2)&plus;X(10/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(5)&plus;X(6)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{69&plus;76}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;72.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10/2)+X(10/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(5)+X(6)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{69+76}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 72.5" /> |80&emsp;&emsp;90&emsp;&emsp;90&emsp;&emsp;92&emsp;&emsp;*92*&emsp;&emsp;*95*&emsp;&emsp;95&emsp;&emsp;97&emsp;&emsp;99&emsp;&emsp;100<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;\frac{X(n/2)&plus;X(n/2&plus;1)}{2}&space;\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(10/2)&plus;X(10/2&plus;1)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{X(5)&plus;X(6)}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;\frac{90&plus;91}{2}\\\\&space;\frac{}{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;=&space;90.5" title="Median = \frac{X(n/2)+X(n/2+1)}{2} \\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(10/2)+X(10/2+1)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{X(5)+X(6)}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = \frac{90+91}{2}\\\\ \frac{}{} \quad \quad \quad \quad \quad = 90.5" /> |                            
 
 &emsp;So, the Interquartile Range is given by **IQR** = **93.5** - **72.5** = **21**     

With this mathematical knowledge we can infer that students performed well in **2<sup>nd</sup>**. Hence they improved.


### The 5 Point Summary
&emsp;The Minimum, the First Quartile, the Median, the Third Quartile and the Maximum are the five numbers often used to summarise a given data sample. 

&emsp;These data points are also known as The Five Point Summary.  

<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#FFFFFF&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-21T06:31:12.804Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;JHhZEkbsiOZtU8Hxmh1T\&quot; version=\&quot;14.6.13\&quot;&gt;&lt;diagram id=\&quot;XM4BjzlWB54q8TmcV5Dv\&quot; name=\&quot;Page-2\&quot;&gt;7Vzfc5s4EP5rPHP3kAxIIMRjk7SXuzZ37aXTu9xLh4Bs64LBg3Hs5K+vMML8dBE2RgTbeQgsYgHtft9qV4IRvJ6tfwus+fTOd4g7AoqzHsGbEQAqVCD7F0leYokBjFgwCajDG6WCe/pKuFDh0iV1yCLXMPR9N6TzvND2PY/YYU5mBYG/yjcb+27+qnNrQkqCe9tyy9J/qBNOuRQoSnrgltDJNLm0CfiRmZW05oLF1HL8VUYE34/gdeD7Ybw1W18TN+q9pGMevt5d3Fp/vd6+Bqs7c3Lx6XPw+0Ws7EOTU7bPEBAv3Fs10b/9//EBff/457en4NPfz3BMTH6K8my5S95h/FnDl6QHiee8iwzB9jzfY8KraThz2Z7KNhehFYSFw2Pqute+6web8+FYj/42bQP/iWSOoM0vOsP3wnt+Rf6wxCnZtebpebuFvwxs8pNHVs2t7ZjXE39GwuCFnbhK3UPn3TLNOEYiC4hrhfQ5f3MW99LJVt32Cp99ym4bKAmiDK6H40lLHDFREd8/PytrzoIipOYVQdO8NLO/vFpmpwkJS2rZRqYTUtHGdxr4kXqgHzX3mUrP69KPAOyTH9WYX9SrmD+24FXMLNZLptk8arDY/TDFqyagSJ001tiqywIBl3VdFqciz1pNaUju59bGI1YsVObd11rM4+A1pmvitMCB8X6mXfxjcn7XJAjJeg/HLvtrYgOzaHm+n/FnUOHPoMBfWdfNsUxT+8DBhaYYLXUuKYtRtnraZRTdrAl4R45MWocwd3SCHa3KnzB4hJUwPxacYcmakuGsDw7O9SMEQdhrMmEPQUsDUtlARyfoYDs4oBvPqTW4qOeoCuxTLmN0GDHewMDQKCWakiMJPhDobzDXVA3BUGL0iRBaGkGW6EE0sjRNQxGSkIaaZ7bJsU2priGZbRL2O6VxhSjbSK2kojy76GZbgxFd7jhWFamlnhAjmH3LZFXQpYGwTWy7ykCPWNdY13RXUlCVvo0EVZEa4QCLO7iUL8k2hEiVbWBB0hQMkqrUeSIDt5aky46LIhXE/cFejHIF8FsEjytpGNmYPI6PCPZyViUb7IdW2no+CxM72sCSaENppLZxRt062s9VuBwLoN6Ngk+xDKeLUojUOhxSlUsl/WHt58jXjsQoBb3yKeVcassPLPqWRSSKTymLAEiUUqQW26ARg1vHhgo1FYIy9A0VIE3DSNN1pO9HKe2saWxa9td2pEjHXX12rvLlSxp9y3ISe5wSGSX1tPqFalIXHmBtQwtI1QHGGkQVZKRGrRQDaaoB9uOi2kUJGAqxUWuE0WWts09V575NCIJDa509L3+cxLr2w5cQtI7v45Y339yAAPQuOxEpe56QgbTeEbNIyXBgIzaARVkdyWR1WMfqe9agdJDTk9Qk30pFCojUUE+JUvq2wACIlAwHRimaKKPgITKKht40o8BmL+LarrVYUDvvswc5mLQ5j+JshNFK3lBSC2W+mZCUXTPWvSMOtbxRxIDIZV169RiwrUm05QdlGfAc1vbLkrESZf4gdI6uMPsx+xPWY158WsGjWBgIi7yX5bIK4uMiy6UTL3JEppkw+VUUVKhtue/4gRl1HHdX9Av8pedEse6mXJE4UojSC69LgYoQpaIuYxRsthxjOJCHunmJQQmLSYZf7HBRyNeoRWKFg9YgX05qPtBgEWZQ/MsX9dcdSLZmEUy8x8V8Y+QSG+hnZKcFh+I0EJaO7GZLLIaDbMyiLIbpCgbQDrJr1HaM7KQimbHu1ykNnByywZ7INs7ITu1uFN/r6hLZF6/fJ8HtvT19Wl8o4I8n7z/ttvLbI9yEiQXvqEdny1kiZ5fZHuqpLY825KovChhdGq/Zh0kqWZmsafhvZvsh6sJLne/drHmPbnZect3bSt6/2yelTfvUveIpPG274x3OI7B6ZS9WTQ4WkW2tz8iOtSi4Z9hu9pWS4Yy4SpY44D2RPada6xHIdtOvLcbN049Wwvc/AA==&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
<p align="center">Figure 3: 5 point summary for a 15 point unknown data sample</p>
</div>  

&nbsp;   
**_Eg-5 :_** A year ago, Angela began working at a computer store. Her supervisor asked her to keep a record of the number of sales she made each month.  

&emsp;The following data set is a list of her sales for the last 12 months:  

&emsp;34, 47, 1, 15, 57, 24, 20, 11, 19, 50, 28, 37 

**sol:**  
&emsp;Arranging the values in ascending order  

|1|11|15|19|20|24|28|34|37|47|50|57| 

&emsp;W csn say that the maximum sales were **57** and the minimum were **1**

<p align="center"><img src="https://latex.codecogs.com/svg.image?Median&space;=\frac{X(\frac{n}{2})&plus;X(\frac{n}{2}&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(12/2)&plus;X(12/2&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(6)&plus;X(7)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{24&plus;28}{2}&space;\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;26" title="Median =\frac{X(\frac{n}{2})+X(\frac{n}{2}+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(12/2)+X(12/2+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(6)+X(7)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{24+28}{2} \\\\ {} \quad \quad \quad \quad \quad = 26" /></p>

|     |     |
|:---:|:---:|
|1&emsp;&emsp;11&emsp;&emsp;15&emsp;&emsp;19&emsp;&emsp;20&emsp;&emsp;24<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=\frac{X(\frac{n}{2})&plus;X(\frac{n}{2}&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(6/2)&plus;X(6/2&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(3)&plus;X(4)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{15&plus;19}{2}&space;\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;17" title="Median =\frac{X(\frac{n}{2})+X(\frac{n}{2}+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(6/2)+X(6/2+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(3)+X(4)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{15+19}{2} \\\\ {} \quad \quad \quad \quad \quad = 17" />|28&emsp;&emsp;34&emsp;&emsp;37&emsp;&emsp;47&emsp;&emsp;50&emsp;&emsp;57<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=\frac{X(\frac{n}{2})&plus;X(\frac{n}{2}&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(6/2)&plus;X(6/2&plus;1)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{X(3)&plus;X(4)}{2}\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;\frac{37&plus;47}{2}&space;\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;42" title="Median =\frac{X(\frac{n}{2})+X(\frac{n}{2}+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(6/2)+X(6/2+1)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{X(3)+X(4)}{2}\\\\ {} \quad \quad \quad \quad \quad = \frac{37+47}{2} \\\\ {} \quad \quad \quad \quad \quad = 42" />|  

Hence the 5 point summary is 

|Minimum|1<sup>st</sup> Quartile|Median|3<sup>rd</sup> Quartile|Maximum|
|:---:|:---:|:---:|:---:|:---:|
|1|17|26|42|57|

#### The Anatomy of a Box-Plot
&emsp;A boxplot is a standardized way of displaying the dataset based on a five-number summary.

&emsp;They were introduced by the American statistician John Tukey around 1970 and became widely known after the publication of his book Exploratory Data Analysis in 1977.

&emsp;They are widely used while comparing two or more categories, samples or even populations.

<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#FFFFFF&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-21T07:51:11.143Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;UBqNiKfp8mwlR3t9rm7-\&quot; version=\&quot;14.6.13\&quot;&gt;&lt;diagram id=\&quot;bAe-oB_lqUXJ17f_VAu5\&quot; name=\&quot;Page-3\&quot;&gt;7Zptb9o6FMc/DdLulYqCTcJ4WVpuN+lWa9dNt92byUvcxJsTI8eUsE8/m9h5cLIBKU3vRvuiio8dh/x/xz7HBwbwLM4uOFpElyzAdACcIBvA8wEAngvkf2VY5wbowdwQchLkplFpuCHfsTY62rokAU5rAwVjVJBF3eizJMG+qNkQ52xVH3bPaP2pCxTihuHGR7Rp/Y8EItJW4DhlxxtMwsg8egp0T4zMaG1IIxSwVcUE5wN4xhkT+VWcnWGqxDPC3KAYf3hgH98t/OX157lYORk4ySf7Z59binfgOBGHndro84DoUiumX1asjYScLZMAq1mcAZytIiLwzQL5qnclfUbaIhFT2RrJy3tC6RmjjG/uhXgUuHgi7Tu+gvk4mAucVQjqV7rALMaCr+UQ3TseazrGPw2tVY12bosqoM19SDtYWExdaigvtIz7SAq2S4qT4FQ5t2wlLMF1CaVCfH2r5d407lRj6JrmeVbtPF/r1n4S46C2cJoCVwR0W/QzNo4pEuShvtzaRNVPuGJEfryCH/QsfjaXlC25j/VdVfe2Jmo4gj2RQDzEojHRhnHx2o/ADh+J/bfE59r44HQ4mVb+3G40veemOT5Gmo3F6HZcjI2JYM/43GPE11g0XfE1Juobn/fYEJoRcVsGTdm6q/SU8VM1TPgsw24Zae9qgfYQYTdHsENGlku8w8D/ifPZ8RdMuwbyqTVR31v/6xbn86hUa/ZFXoTq4hIHBCXGLB9T9DT8VOaxou6cqeDsGzZJsnbeat6sTYiSMJFNXzoWlvaZyoqJPNqc6o6YBIF6TGtOXs/a93PSPdLvibVTmHNVxem8FqcDzs/963HZ93Q7vevRCzkwBtvJjfskZ2LML8nBwsRLbkfP0rXj9bOz3KGskAMwRZmRRSdCCzUuzkJVlhreU7byI8TFECUJEzJQseQzqOCh+F4BpugLplcsJWqANPP8ZWcLFS0wnz9I5VP9jIBw7OtxMjipj9FbmQJMmoRayxR25nU4RG1lCmu5vb1+L0dsOh219JwTdfGye0qersXTbeHp9Lrk2o48dtpCEhIv43Z+9r76SoHeEB8N3b+lK/x1ZIyhHSG9JuPXT4T447/hp6/wa3AxZrd0ROb40/vTkx1W7CXK9iGs1vQAzH4Xxg12u2L/eeScbmf8ZOu4FXKnMmKA0mijlRVGlf0KCSl/srEABxYATeQdF/JaJ8nu4vZUrRpZ7LqWjrfWoA934mxF3qnWeJTIPXu5dkXeY325FfkO9UmTAvtLTtczjvxvqhy07fu3ctvcfBtHyeLNL9LdNP++Nq94PdUe29C65XTS5jNPtsXuUF38Y8RvbJLPLf5kexLzbikowTz9A876hwcKppOhW0NaJKEVpBO3R6TGxV6Ydt0hQY9MZbP8zUoez8pf/sD5Dw==&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
<p>Figure-4: Visualizing the various parts of a Boxplot</p>
</div>
 
&nbsp;    
&emsp;Box plots are made of 5 key components  
&emsp;&emsp;- Median  
&emsp;&emsp;- Hinges: two hinges located at the lower and the upper quartiles denoted by Q1 and Q3, respectively.  
&emsp;&emsp;- Fences: two fences determined as the data values which are adjacent to the extremes:  
&emsp;&emsp;&emsp;&emsp;Lower Extreme = Q1 – 1.5(IQR),  
  
&emsp;&emsp;&emsp;&emsp;Upper  Extreme = Q3 + 1.5(IQR),  
  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;where IQR denotes the inter quartile range, IQR = Q3 – Q1.  
  
&emsp;&emsp;- Whiskers: two lines that connect the hinges with the fences.  
&emsp;&emsp;- Outliers: all individual points further away from the lower and upper extremes are represented as dots.  

**_Eg-6 :_** The School of WhYrus conducted an experiment on amount of time people spent exercising every day. Here is a sample of 15 values. Interpret them. 

&emsp;0 minutes, 40 minutes, 60 minutes, 30 minutes, 60 minutes, 10 minutes, 45 minutes, 30 minutes, 300 minutes, 90 minutes, 30 minutes, 120 minutes, 60 minutes, 0 minutes, 20 minutes   
**sol:**      
&emsp;First let's arrange the data into order

|*0*|0|10|20|30|30|30|40|45|60|60|60|90|120|*300*| 

&emsp;Now find out the median   

<p align="center"><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;X(\frac{n&plus;1}{2})=&space;X(\frac{15&plus;1}{2})=&space;X(8)&space;=&space;40" title="Median = X(\frac{n+1}{2})= X(\frac{15+1}{2})= X(8) = 40" /></p>

&emsp;Then we will find out the middle point of each individual groups separated by the median.   
 
|  Q1   |  Q3   |
|:---:|:---:|
|0&emsp;&emsp;0&emsp;&emsp;10&emsp;&emsp;*20*&emsp;&emsp;30&emsp;&emsp;30&emsp;&emsp;30<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;X(\frac{n&plus;1}{2})\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;X(\frac{7&plus;1}{2})\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;X(4)&space;\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;20" title="Median = X(\frac{n+1}{2})\\\\ {} \quad \quad \quad \quad \quad = X(\frac{7+1}{2})\\\\ {} \quad \quad \quad \quad \quad = X(4) \\\\ {} \quad \quad \quad \quad \quad = 20" /> | 45&emsp;&emsp;60&emsp;&emsp;60&emsp;&emsp;*60*&emsp;&emsp;90&emsp;&emsp;120&emsp;&emsp;300<br><br><img src="https://latex.codecogs.com/svg.image?Median&space;=&space;X(\frac{n&plus;1}{2})\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;X(\frac{7&plus;1}{2})\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;X(4)&space;\\\\&space;{}&space;\quad&space;\quad&space;\quad&space;\quad&space;\quad&space;&space;=&space;60" title="Median = X(\frac{n+1}{2})\\\\ {} \quad \quad \quad \quad \quad = X(\frac{7+1}{2})\\\\ {} \quad \quad \quad \quad \quad = X(4) \\\\ {} \quad \quad \quad \quad \quad = 60" />|

&emsp;So Interquartile range is IQR = Q3- Q1 = 60 - 20 = *40*

&emsp;Then calculate the extreme values as follows

&emsp;&emsp;Lower Extreme = Q1 – 1.5(IQR) = 20 - 1.5*40 = 20 -60 = -40

&emsp;&emsp;Upper  Extreme = Q3 + 1.5(IQR) = 60 + 1.5*40 = 60 + 60 = 120  

&emsp;So we have one potential outlier(i.e.300)

&emsp;&emsp;Now summing up all of this information into a boxplot give us

<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#FFFFFF&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-21T08:30:44.163Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;hbIeYHdjDIeKwhe04SrC\&quot; version=\&quot;14.6.13\&quot;&gt;&lt;diagram id=\&quot;ACEENY4e2prZLJeGvaWZ\&quot; name=\&quot;Page-4\&quot;&gt;7Zxbc5s4FMc/jR+dQdxsP8ZJ2k233Uknu9uZfcnIINvayIhg+ZL99CtA2ALhQFpunaoPtTngIzi//4GjA2Fk3WyOHyMYrr9QH5GRafjHkXU7Mk0AwIR/xJbX1OKaVmpYRdgXG50Nj/g/JIyGsO6wj7a5DRmlhOEwb/RoECCP5Wwwiughv9mSkvyoIVwhxfDoQaJav2GfrYXVNIzzit8QXq2zoWemWLOB2dbCsF1Dnx4kk3U3sm4iSln6bXO8QSSOXhaY68cjnHz+9vfDh39enqynzf3XRzZOnX14z09OxxChgDXrWsDcQ7ITARPHyl6zCKLAv45B8CWPwO0WeyNrvmYbwg2Afz2FxYgXWESfT5HmIZovacCELEC8nPpHvoKt4uDAKeJcq4huEIte+e8OZ6iO4LSWcGa2CBHI8D4/JhTaWp3cnUZ4oJjvjWmIPDAnwo/IAifTROZiS3eRh8SvZAgFR7MqRwxGK8QUR/yLdNhnU8K4nPen39G/cPpkfprdH1/CuUU/Lu7G5rt4BzRAb8Auos3DBz8rbMssMLK+E7biqGPY70vuXxS22xTsoqOOYdsadiVs2zCuDOkfaAZ9hduOheBoIVQLwW5HCG+77VgIrhZCtRCmDZ3+FUcdw55o2JWwnaYKO8VRx7CnGnY1bLeVU3yF246FMNNCqBSCazSU9YqjjmEDnfY1aNtN0S466pq2zu0atJsq3xRHXfflDE27kvbEbOWSXuG2ayUArYRqJbRT3FW47VoJplZCpRKmTVV3iqOuaetufQ3aTVV3iqOuaet2fQ3a01bO8hVuu1aC7tdXK2FWbLh9L3vFUde01ab86fGSM2+GjqwAOeF4QwmNziJYYkIKJkjwKuCLHoeJuH2+RxHDHiTXYsUG+348zPywxgw9htCLxzxEMOS2iO4CH/lCS28KSxwG946OjQgpu4166XouCc0uEVqRo6ypHMR3E1M767YmJhO7dE3ujZjaJ3M1MZnYpa5Jb8TUXtdUE5OI2Zeuf30Ry8aXiAFDI5ORuRfK1d6QqY0loGsPGZkztNrDUjtAQBcfOWRDKz4stY0DdPWRQza06sNSezFAlx8yMndw5YfaNDF1+ZFDdum55t6QlXQ+gEYmIZsMrvxQWx+6W5VH1mP5MR8T/9kaL8je/+vO2N9vj08PY3VaprtVeWI9Vh+lxNRZme5W5YhNeyw+SompkzLdrcoT67H2KCWmzsksXS3KxGY9lh6lxPRN0Rp/lNzUw4+Ko/ZuipbCVmcGOjml5DSHdjqt8Rx6Pmxlgf3RZG3htlih0LBtNc7TkjjbbcW5xhPgBCcaV4MkhTdEEeY7FGv/dgG95wXPi4ezbR7GeZ3suzMfObfcQncsdnxzeidHf9ovnJpsx6mlfdAWE1Dj8dyhQPFxxLfEND7J8WtBvBvtgZo4lckDukweoJbpgwXVFhTbqM6e0z3AbtKnxlOuQ6HSZfo4YGjpU+MB1V8RlOUMDVSNqRKPXpiUXvA1iXcc0GfEvHUW3TSYbsYDRXd7lGIBpYxKyuwIcS9wkQxpJIUzg0xaloWQluKyDLYBDP+k6QxjUEVhcWZcxrusAGmPd9lrHVzCRJRy4N2XHc1WjFPI13wDYITH80r+bRV/fgWZH75fqat0hSKngc/F2pQD10NeDqYqB7fLuRgoe/FDinEbwuAH5GBJckhdaTkoV4PJ0ORQNjdv4uzwBfk40UDiaxGd1aDPGVUisQYmkjp/apYF+TNcIPJAt1jUVwvKGN2UUGBU7eokRcfmuIpfLXq1JPTgrWHErmgwjl+7+RShJeKR9VCRDIkHnfNqcZXgK2qkwE0tBkpU1Fp9AIpTLBVu2QyrPbhqPfgH5ct0yf/b4GDH0DZGHaLAjz8JQiEOVj9DwtaXhSmWOxLBCXrWoXVVEVgNqYAvnl85m3bgz2/ute7+Bw==&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
<p>Figure-5 : Five point summary of individuals and their sleeping time</p>
</div>

## Standard Deviation
&emsp;In statistics, the standard deviation is a measure of the amount of variation or dispersion of a set of values. A low standard deviation indicates that the values tend to be close to the mean of the set, while a high standard deviation indicates that the values are spread out over a wider range. 

&emsp;It is nothing but the square root of variance.

|Population Std|Sample Std|
|:---:|:---:|
|<img src="https://latex.codecogs.com/svg.image?\dpi{200}\sigma&space;=&space;\sqrt{\frac{\sum_{i=1}^{N}&space;(x_{i}&space;-&space;\mu)^{2}}{N}}" title="\dpi{200}\sigma = \sqrt{\frac{\sum_{i=1}^{N} (x_{i} - \mu)^{2}}{N}}" /> |<img src="https://latex.codecogs.com/svg.image?\dpi{200}s&space;=&space;\sqrt{\frac{\sum_{i=1}^{n}&space;(x_{i}&space;-&space;\bar{x})^{2}}{n-1}}&space;" title="\dpi{200}s = \sqrt{\frac{\sum_{i=1}^{n} (x_{i} - \bar{x})^{2}}{n-1}} " />|

&emsp;Steps to calculate the Standard Deviation  
&emsp;&emsp;- First figure out the mean value of the data points.  
&emsp;&emsp;- Calculate the sum of the squares of the difference from each data point to the mean value.  
&emsp;&emsp;- Now divide this whole sum with the one less than the no of data points(i.e. n-1)  
&emsp;&emsp;- And finally take the square root of this to find out the standard deviation of the data points.   

**Eg-7 :** The reporter compares a week of high temperatures (in Fahrenheit) in two different seasons. The data looks like this:  

|           | City A Forecast | City B Forecast |
|-----------|:---------------:|:---------------:|
| Monday    | 95              | 91              |
| Tuesday   | 93              | 81              |
| Wednesday | 95              | 95              |
| Thursday  | 94              | 91              |
| Friday    | 96              | 86              |
| Saturday  | 94              | 82              |
| Sunday    | 95              | 78              |

**sol:**  
&emsp;At first he figures out the mean temperature in city-A is **94.6 F** and the mean temperature in the city-B is **86.1 F**.  

|||
|:---:|:---:|
|<img src="https://latex.codecogs.com/svg.image?\dpi{200}\bar{x}&space;=&space;\frac{95&plus;93&plus;95&plus;94&plus;96&plus;94&plus;95}{7}&space;\\&space;\\&space;^{}\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;=&space;94.6&space;F&space;" title="\dpi{200}\bar{x} = \frac{95+93+95+94+96+94+95}{7} \\ \\ ^{}\; \; \; \; \; \; \; = 94.6 F " />|<img src="https://latex.codecogs.com/svg.image?\dpi{200}\bar{x}&space;=&space;\frac{91&plus;81&plus;95&plus;91&plus;86&plus;82&plus;78}{7}&space;\\&space;\\&space;^{}\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;=&space;86.1&space;F" title="\dpi{200}\bar{x} = \frac{91+81+95+91+86+82+78}{7} \\ \\ ^{}\; \; \; \; \; \; \; = 86.1 F" />|  

&emsp;To infer this he considered calculating the amount of spread between each city individually.

&emsp;That is

&emsp;**For city-A**
<p align="center">
<img src="https://latex.codecogs.com/svg.image?\dpi{100}s&space;=&space;\sqrt{\frac{\sum_{i=1}^{7}&space;(x_{i}&space;-&space;96.4)^{2}}{7-1}}\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{\frac{(95-94.6)^2&plus;(93-94.6)^2&plus;(95-94.6)^2&plus;(94-94.6)^2&plus;(96-94.6)^2&plus;(94-94.6)^2&plus;(95-94.6)^2}{6}}\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{\frac{0.16&plus;2.56&plus;0.16&plus;0.36&plus;1.96&plus;0.36&plus;0.16}{6}}&space;\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{0.953}\\&space;\\&space;^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;0.976" title="\dpi{100}s = \sqrt{\frac{\sum_{i=1}^{7} (x_{i} - 96.4)^{2}}{7-1}}\\ \\^{} \; \; \; \; \; \; \;= \sqrt{\frac{(95-94.6)^2+(93-94.6)^2+(95-94.6)^2+(94-94.6)^2+(96-94.6)^2+(94-94.6)^2+(95-94.6)^2}{6}}\\ \\^{} \; \; \; \; \; \; \;= \sqrt{\frac{0.16+2.56+0.16+0.36+1.96+0.36+0.16}{6}} \\ \\^{} \; \; \; \; \; \; \;= \sqrt{0.953}\\ \\ ^{} \; \; \; \; \; \; \;= 0.976" />
</p>

&emsp;**For city-B**
<p align="center">
<img src="https://latex.codecogs.com/svg.image?\dpi{100}s&space;=&space;\sqrt{\frac{\sum_{i=1}^{7}&space;(x_{i}&space;-&space;86.1)^{2}}{7-1}}\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{\frac{(90-86.1)^2&plus;(81-96.1)^2&plus;(95-86.1)^2&plus;(91-86.1)^2&plus;(86-86.1)^2&plus;(82-86.1)^2&plus;(78-86.1)^2}{6}}\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{\frac{15.21&plus;26.01&plus;79.21&plus;24.01&plus;0.01&plus;16.81&plus;65.61}{6}}&space;\\&space;\\^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;\sqrt{37.81}\\\\&space;^{}&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;&space;\;=&space;6.15" title="\dpi{100}s = \sqrt{\frac{\sum_{i=1}^{7} (x_{i} - 86.1)^{2}}{7-1}}\\ \\^{} \; \; \; \; \; \; \;= \sqrt{\frac{(90-86.1)^2+(81-96.1)^2+(95-86.1)^2+(91-86.1)^2+(86-86.1)^2+(82-86.1)^2+(78-86.1)^2}{6}}\\ \\^{} \; \; \; \; \; \; \;= \sqrt{\frac{15.21+26.01+79.21+24.01+0.01+16.81+65.61}{6}} \\ \\^{} \; \; \; \; \; \; \;= \sqrt{37.81}\\\\ ^{} \; \; \; \; \; \; \;= 6.15" />
</p>

This confirms the fact that city A’s forecasts are more reliable than City B’s forecasts.

### Why we divide by n-1?
&emsp;As the sample size tends to reduce while compared to the population. The sample statistic will become an biased estimate of the population parameter.

&emsp;Hence by using n-1 degrees of freedom we can achieve a statistic which is close to the true to the population.

<div style="background:#f5f5f5;padding:.5em .5em .5em .5em;">
<h4 id="summarizing-khan-academy-review" align="center">Summarizing Reasons</h4>
<p>&emsp;As the population size reduces there is a huge chance of underestimating the true population mean.</p>
<div align="center">
<div class="mxgraph" style="max-width:100%;" data-mxgraph="{&quot;highlight&quot;:&quot;#FFFFFF&quot;,&quot;lightbox&quot;:false,&quot;nav&quot;:true,&quot;edit&quot;:&quot;_blank&quot;,&quot;xml&quot;:&quot;&lt;mxfile host=\&quot;app.diagrams.net\&quot; modified=\&quot;2021-05-24T06:24:52.930Z\&quot; agent=\&quot;5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.212 Safari/537.36\&quot; etag=\&quot;HLkwYBM2AP7xQkk720mT\&quot; version=\&quot;14.7.0\&quot;&gt;&lt;diagram id=\&quot;_sR00FdCNcYVVuygdo2n\&quot; name=\&quot;Page-5\&quot;&gt;7Vtdk5s2FP01zLQP2QGBbPZxbcdNM5NOZtxpn7UgAxOBXIHXdn59JSS+Sc3uls92ZzeBK/kizrlHuhcZzdyG118YOvlfqIuJBnT3qpk7DYBHoPN/heEmDdAwpcFjgStNRmE4BN+xMqrPeefAxXGlY0IpSYJT1ejQKMJOUrEhxuil2u1ISfWqJ+ThhuHgINK0/hm4ia+sQNeLhk848Pzs0vkdhyjrrQyxj1x6KZnMj5q5ZZQm8ii8bjER4GXAOJHPot8+79ln/B1vb+RX8kfwQTrbv+Yj+T0wHCX/rmsgXb8gclaAqXtNbhmCOHKfBBH8LKIRN278JCT8zOCHcYJYUmuWHrDbIObO8FW/mJ6Zg/9pzCAHn0ctpiFO2I1/8FLwCxVlfonZzMYwQUnwUh0cUmHm5e7yK3ylAR820JUizCwclCDMlV51IcevPlXmo+bIhncccWg9nDQc8YPSbRemlO5XUG91oJ4QrlPB6cUPEnw4oZSYC58pqmGA4pMU7zG4Yn7RzTEgZEsJZfWweMEswdc3BEaT74wQs4ZjhmspHkBLPAD9x9RXsH4tsPCdmnqnfmTY3CN+/vKxx5XPaij5aMDU059eNQRrGoINDRktQWH0paH1otB9rM9QI6Nrz3DVf+w4u61Hnd2g/qCXfoxlzHWPi1LjamJqzBzPSo5WRzk+LlCOfD4vu10Z1qjqNIw+5RknjH7DJYGuHBs/HwfO8WE9Pxk5xze6FM4zx9yeGubmkpYhq76mj74MLaqigcbU4F1USQOtqcE7x5pGhcTdJMoYtaix9DvVx1zKGGNRdQyc2gICutQxs4HXqj+eHx3eXtP8weFtPLUfG95eM/qh4V1NLf0BXZL3qa3PRtcFWt7MWAs0vLeTOJcFGgy2JzmIBqeWI4MuO5PzgXc9NXgXVUCvJ7eCLKqAXk9ucuhSQM8H3qltuYJF1Z721CaHrJoowXtA4YkEkScux/++0tNZZFk0auDOwUnqyWb5AbzKNluevSMSeBE/dTiYmNs3AurAQeRJNYSB65IfMcroOXIFfzvB1ZFGyUENyuiLOFh/lpPppExcW6ra21N9s0vd1SgMXBT7KXJGlbiaEI62gx2nbUfl2Yaiwn9nDTHaxmY997HfmPE3HFnDZvxmr3s609hHm9r3E80OiVTso5M4dM6M3DYMOd9E/XuPgGJCS7XIafvUostMwgHjbIn52NzxcBVQDMcBaHJgD8pBM9tK1ys80cVpMGL0kYmxmomEBlZEUBCfUFThZvXXWXz3f+NI3J/EvO49o5+4C/7Lr6+3Hv0sDgWkuljyPxxRGJCb/HhIIxqnPFS6xOlrFaKDfroW1+VHnvo/HaBIc3yGj5XB+UkiXrV4ErCAPV918PXBoS52qBfzg5Ab4xfvIQjTFyn2Gtw+I6atN1dtvWte6p3eiPS1R8XQYf3dE8jZEtb0xYr8LGMPpvxxy04cC0yhYAiK8dzpa+R9s6h9kxtQuJFBkrdkCs6aZaTkzamS+ZnUsjAb6WlZz8Kaylc0FJqumKWuhUkpWxir2haNSt2isaRv0ZIqXNgzjQujnlpK9ya13gW9vCkHrhA6FFLPe6Z1QubmVrLrBQNK+nmbVWpSU0DBRamNTwW53Stdv05reppzWzZWI071a4RmHsRyPsji+D81bYN6GdGynhpmy7xt9FYBWs3tsUyP+heM5lD1gb7oany93x57le216DviVVr0aXMs7Rrb+m8t7RqO6mz2/X5Zs7T7nZ3/l2PLl6f6S3o1taqVmC3WM/Pj3w==&lt;/diagram&gt;&lt;/mxfile&gt;&quot;}"></div>
<script type="text/javascript" src="https://viewer.diagrams.net/js/viewer-static.min.js"></script>
</div>

<p>I recommend you watch the <a href="https://www.khanacademy.org/math/ap-statistics/summarizing-quantitative-data-ap/more-standard-deviation/v/review-and-intuition-why-we-divide-by-n-1-for-the-unbiased-sample-variance">khan academy review</a> and try those simulations before reading this.</p>
<p>One of the simulations shows how the unbiased variance estimates its true value when it uses n-1 degrees of freedom.</p>
<p>Another one tells us that for a sample size n we are approaching n-1/n times the population variance.</p>
<p>Calculating the unbiased estimate would be as follows</p>
<div align="center">
<img src="https://latex.codecogs.com/svg.image?\frac{n-1}{n}\times&space;\sigma^2&space;=&space;\frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n}&space;\\\\&space;&space;&space;&space;multiplying\;with\;&space;\frac{n}{n-1}&space;\;on\;both\;sides\;we\;get&space;\\\\&space;\frac{n-1}{n}\times&space;\sigma^2&space;\times&space;\frac{n}{n-1}&space;=&space;\frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n}&space;\times&space;\frac{n}{n-1}&space;&space;\\\\&space;^{}\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;s^2&space;=&space;\frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n-1}&space;&space;" title="\frac{n-1}{n}\times \sigma^2 = \frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n} \\\\ multiplying\;with\; \frac{n}{n-1} \;on\;both\;sides\;we\;get \\\\ \frac{n-1}{n}\times \sigma^2 \times \frac{n}{n-1} = \frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n} \times \frac{n}{n-1} \\\\ ^{}\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;s^2 = \frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n-1} " />
</div>

<p>&nbsp;<br>And in the last simulation, he/she records the sample estimate with respect to different values of a using the formula</p>
<p align="center">
<img src="https://latex.codecogs.com/svg.image?Variance&space;=&space;\frac{sum((x[i]-mean(x))^2)}{n&plus;a}&space;&space;" title="Variance = \frac{sum((x[i]-mean(x))^2)}{n+a} " /></p> 

<p>When we generate more and more samples the best estimate is recorded when a is close to -1. Also, we will overestimate and underestimate while a is less than or greater than -1 respectively. </p>
</div>

[1]: https://suhruthy.github.io/SuhruthY/blog/numerical-summary-part1
[2]: https://www.khanacademy.org/math/ap-statistics/summarizing-quantitative-data-ap/more-standard-deviation/v/review-and-intuition-why-we-divide-by-n-1-for-the-unbiased-sample-variance 

