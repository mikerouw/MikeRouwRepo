### Data Exploration - Jean Lafitte National Historical Park & Preserve

The purpose of this assignment was to explore the project data and practice the use of the RStudio to view the data in several different visual views.  This document will contain several views of the data, each with a plot, the associated R code, and a brief discussion of the data view.  Prior to this plotting exercise, the data had to be cleaned to eliminate entries of "-9999" for what is really a point of "no observation".  The R code assumed the "-9999" values were valid on the first pass, so the data was cleaned to remove elements of "no observation".  Specifically, any instance where the _First_Yes_Sample_Size = 0_, that row was removed from the dataset.


[Scatter Plot](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Phenophase_FirstYES.png)

> CodeBlock1

this description

[Plot2]()

> CodeBlock2

this description

[Plot3]()

> CodeBlock3

this description

[Plot4]()

> CodeBlock4

this description

[Plot5]()

> CodeBlock5

this description

[Plot6]()

> Codeblock6

this description

**Summary**

For the Jean Lafitte dataset, there is little information that can be gained from looking at the entirety of the data.  Rather, the dataset will need to be separated and segmented so that meaningful comparisons and observations can be made.  This is because each species has very different phenophase events with very differnt timings.  The data most likely will need to be segmented by species to obtain any valuable observations.
