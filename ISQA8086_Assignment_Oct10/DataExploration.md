### Data Exploration - Jean Lafitte National Historical Park & Preserve

The purpose of this assignment was to explore the project data and practice the use of the RStudio to view the data in several different visual views.  This document will contain several views of the data, each with a plot, the associated R code, and a brief discussion of the data view.  

Prior to this plotting exercise, the data had to be cleaned to eliminate entries of "-9999" for what is really a point of "no observation".  The R code assumed the "-9999" values were valid on the first pass, so the data was cleaned to remove elements of "no observation".  Specifically, any instance where the _First_Yes_Sample_Size = 0_, that row was removed from the dataset.

**Plot 1 - Scatterplot of phenophase and date of "first YES" observation**

![Plot1](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Phenophase_FirstYES.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID))

This scatterplot shows the specific phenophase identifier and the day of the year when the specified phenophase was first observed.  There is really no pattern to this view, nor would it be expected, as the data includes a multitude of species which have different phonphase identifiers and timings.  Data segmented by species would probably be more appropriate.

**Plot 2 - Scatterplot of species and date of "first YES" observation**

![Plot2](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Species_FirstYES.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Species_ID))

This scatterplot shows the specific species and the day of the year when the specified phenophase was first observed.  Much like before, there is really no pattern in this view, as again the data is mixed and unsegmented at this point.

**Plot 3 - Scatterplot of phenophase and date of "first YES" observation identified by kingdom (plant or animal)**

![Plot3](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Phenopase_FirstYES_Kingdom.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID,color=Kingdom))

This scatterplot simply adds color to **Plot 1** above, showing which obeservations were made for plants versus animals.  Again, without further segmentation into specific species, this view does not provide much insight.

**Plot 4 - Scatterplot of phenophase and date of "first YES" observation with trend line**

![Plot4](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_ScatterPlot_wTrend.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
geom_smooth(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="black")

This scatterplot simply adds a trend line to **Plot 1** above.  In this case, the trend line is pretty meaningless, as again the whole of the dataset is mixed, and should first be segmented into specific species for more meaningful analysis.

**Plot 5 - Faceted scatterplot of Plot 1 divided by site location**

![Plot5](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_Faceted_ScatterPlot.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_point(mapping=aes(x=Mean_First_Yes_DOY,y=Phenophase_ID),color="blue") +
facet_wrap(~ Site_ID, nrow = 2)

This faceted scatterplot shows the same data and view from **Plot 1** above, except divided into four different views based on site location.

**Plot 6 - Bar chart of total number of observations by site location**

![Plot6](https://github.com/mikerouw/MikeRouwRepo/blob/master/ISQA8086_Assignment_Oct10/Rplot_BarChart.png)

> ggplot(data=site_phenometrics_data_wo_zero_oberservations) +
geom_bar(mapping=aes(x=Site_Name),color="red")

This bar chart shows the total number of observations made at each site as contained within the dataset.  It shows that some sites have had more observations than others, but not much else.

**Summary**

For the Jean Lafitte dataset, there is little information that can be gained from looking at the entirety of the data.  Rather, the dataset will need to be separated and segmented so that meaningful comparisons and observations can be made.  This is because each species has very different phenophase events with very differnt timings.  The data most likely will need to be segmented by species to obtain any valuable observations.

**Contributorship Statement**

I, Mike Rouw, am the sole author and contributor to this document, save the original data provided by Jean Lafitte National Historical Park and Preserve.

**Proofreader Statement**

I, Mike Rouw, have proofread this document and approved it for submission.
