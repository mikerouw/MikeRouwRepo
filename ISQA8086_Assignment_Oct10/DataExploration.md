### Data Exploration - Jean Lafitte National Historical Park & Preserve

The purpose of this assignment was to explore the project data and practice the use of the RStudio to view the data in several different visual views.  This document will contain several views of the data, each with a plot, the associated R code, and a brief discussion of the data view.  Prior to this plotting exercise, the data had to be cleaned to eliminate entries of "-9999" for what is really a point of "no observation".  The R code assumed the "-9999" values were valid on the first pass, so the data was cleaned to remove elements of "no observation".  Specifically, any instance where the _First_Yes_Sample_Size = 0_, that row was removed from the dataset.


![Plot1](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Phenophase_FirstYES.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID))

this description

![Plot2](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Species_FirstYES.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Species_ID))

this description

![Plot3](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Phenopase_FirstYES_Kingdom.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID,color=Kingdom))

this description

![Plot4](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_ScatterPlot_wTrend.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
geom_smooth(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="black")

this description

![Plot5]()

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
facet_wrap(~ Site_ID, nrow = 2)

this description

![Plot6]()

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_bar(mapping=aes(x=Site_Name),color="red")

this description

**Summary**

For the Jean Lafitte dataset, there is little information that can be gained from looking at the entirety of the data.  Rather, the dataset will need to be separated and segmented so that meaningful comparisons and observations can be made.  This is because each species has very different phenophase events with very differnt timings.  The data most likely will need to be segmented by species to obtain any valuable observations.
