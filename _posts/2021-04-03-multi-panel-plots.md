---
title: Working with Multi-Panel-Plots in R
layout: post
post-image: https://ih1.redbubble.net/image.459070279.6514/st,small,507x507-pad,600x600,f8f8f8.u1.jpg
description: ggplot2 is a data visualization package for the statistical programming language R. Created by Hadley Wickham in 2005, ggplot2 is an implementation of Leland Wilkinson's Grammar of Graphics—a general scheme for data visualization which breaks up graphs into semantic components such as scales and layers.
tags:
- ggplot2
- facet
- panel plots
---


&nbsp;&nbsp;&nbsp;&nbsp;Subplot creates a figure and a grid of subplots with a single call,
while providing reasonable control over how the individual plots are
created. In this markdown I’m going to introduce you to the panel
plotting system in R.

    # loading neccessary packages
    library(datasets)
    library(ggplot2)

# Panel Plots with 
## **Base-R**

&nbsp;&nbsp;&nbsp;&nbsp;As you all may know one can plots functions using the base R
plotting system. One of the major functions we use in doing the task is
the par function.

We can check more about the par function using ?

    ?par

Amoung all of the arguments the one that is useful for us is the `mfrow`. Let’s use it and create a simple bi-panel plot.

    ## loading the cars data
    library(datasets)

    attach(mtcars)

#### Vertical panel
    par(mfrow=c(2,1), mar=c(2,8,2,4))

    plot(wt,mpg, main="Scatterplot of Weight vs. Miles per Gallon")
    plot(wt,disp, main="Scatterplot of Weight vs Displacement")

![][1]

#### Horizontal panel
    par(mfrow=c(1,2), mar=c(4,1,2,2))

    hist(wt, main="Histogram of wt", xlab="weight(lbs)")
    boxplot(wt, main="Boxplot of wt", xlab="weight(lbs)")

![][2]

&nbsp;&nbsp;&nbsp;&nbsp;With the par( ) function, you can include the option mfrow=c(nrows, ncols) to create a matrix of nrows x ncols plots that are filled in by row. mfcol=c(nrows, ncols) fills in the matrix by columns.

### layout function
&nbsp;&nbsp;&nbsp;&nbsp;The layout( ) function has the form layout(mat) where mat is a matrix object specifying the location of the N figures to plot. simple plot could be like this.

    layout(matrix(c(1,1,2,3), 2, 2, byrow = TRUE))

    hist(wt)
    hist(mpg)
    hist(disp)

![][3]

&nbsp;&nbsp;&nbsp;&nbsp;With all this I’m leaving it to you to experiment with base R systems and come up with some special plots. One example could be

    par(fig=c(0, .8, 0, .8), new=TRUE)

    plot(mtcars$wt, mtcars$mpg, xlab="Car Weight", ylab="Miles per Gallon")

    par(fig=c(0, 1, .55, 1), new=TRUE)
    boxplot(mtcars$wt, horizontal=TRUE, axes=FALSE)

    par(fig=c(0.65,1,0,0.8),new=TRUE)
    boxplot(mtcars$mpg, axes=FALSE)

    mtext("Enhanced Scatterplot", side=3, outer=TRUE, line=-3)

![][4]
  
## **Facetting**
 &nbsp;&nbsp;&nbsp;&nbsp;The facet approach divides a plot into a m x n sub-panels where each panel shows a different subset of the data.

There are two main functions for faceting : 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - facet_grid() 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - facet_wrap()

Let’s first create a basic plot using ggplot2

    attach(ToothGrowth)

    ToothGrowth$dose <- as.factor(ToothGrowth$dose) # making sure it is categorical 

    g <- ggplot(ToothGrowth , aes(x=dose, y=len, group=dose)) # storing for future use

    bxplt <- g + geom_boxplot(aes(fill=dose))

    bxplt

![][5]

Now lets create 2 panels using the facet grid

    bxplt + facet_grid(supp ~ .)

![][6]

    bxplt + facet_grid(. ~ supp)

![][7]

Adding another variable to facet

    bxplt + facet_grid(supp ~ dose)

![][8]

    bxplt + facet_grid(dose ~ supp)

![][9]

By default, all the panels have the same scales (scales=“fixed”). They
can be made independent, by setting scales to free, free\_x, or free\_y.

    bxplt + facet_grid(dose ~ supp, scales='free')

![][10]

The argument labeller can be used to control the labels of the panels

    bxplt + facet_grid(supp ~ dose, labeller=label_both)

![][11]

Now we will use the facet\_wrap function to create the plots

    bxplt + facet_wrap(~ dose, ncol=3)

![][12]

    bxplt + facet_wrap(~ supp, nrow=2)

![][13]

As we can see above, facet\_wrap returns a symmetrical matrix of plots
for the number of levels of variable .

&nbsp;&nbsp;&nbsp;&nbsp;**facet\_grid** is most useful when you have two discrete variables, and all combinations of the variables exist in the data whereas **facet-wrap** is used when a single variable with many levels and want to arrange the plots in a more space efficient manner.

&nbsp;&nbsp;&nbsp;&nbsp;I will end this with this plot that I made a few days back when I was working with the famous *titanic data*.
![][15]  
you can find out the process and more such plots here: [Exploring the Training data](https://www.kaggle.com/suhruthyambakam/exploring-the-training-data)



[1]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/v_stack.png
[2]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/h_stack.png
[3]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/layout.png
[4]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/enh_scatter.png
[5]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/simple.png
[6]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet2.1.png
[7]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet2.2.png
[8]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet3.1.png
[9]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet3.2.png

[10]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet4.1.png
[11]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet4.2.png
[12]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet5.png
[13]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet6.png
[14]: https://raw.githubusercontent.com/SuhruthY/SuhruthY/master/assets/images/Panel_Plots/facet6.png
[15]: https://www.kaggleusercontent.com/kf/55354731/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..V69Yukd580UN4CSgyUNwPg.IetSnOBniws6H1xsRqhRCVdQmMpXghfiSwjuioanEKElm_TNR_G1OR45yDumJwefZDp_v62zaJoGEJZtOQJ1SmxjsmEO8AsC3HwKYbwPfH2_8QM6hRed-LLVDW98u5Jw04-nb6CSLMMSDTIXHlLbHAi6vXtgtX6r-GjaTEzBTzA7qfsuzkOHTSsok-og4ihIs1tL95q7lMy7kPASJOYRb-fOF2xLB9_qowKY9Rr3vU4HTClYDX9_yCptm91CPD5XfQoVBRJI8Dvd27pFS2KVLIaeYbdA2vKxMR4hiyYA1l_xks6482sKYMM-6B9zLkUfL2XmWQ_abPdDR6VNOpLEkt0RdRzNtwkEfTzhsRttw67QPEJoiv8LUWvc_AT8mBhxyLJahEFdT4bq3srrAiputmYnzrRFEopznQFda4nhnOcjU2T4IFHQvimW-7tVTlz-Lh2hvaoUkZN3BiVSfjy-TU_pIFZTvU8azpS5l_eiG7JMFqn8juK-5dOFpNcqwpS858Qx1rsyS81f3FMyojYDAip-DGyu_ygBStWBPrEZP93BDeu8wr1xXkKQrj1ueMiHf6SSjkzLwPLd1rIaavTOGq5DO8ho-7AV5oP4H7dAxlLHIlRLEJWwL_HTcycpKqoUuMBReRLaYjwOMiQRoUvtg_L7VSh6xn5z8svTs35b3tp_ztyaqxxBJoMd7srBxBRT.vfI_olK_gs1Rpn0JJYow9A/__results___files/__results___24_0.png
