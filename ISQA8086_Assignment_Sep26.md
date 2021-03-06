> ISQA 8086 – Data to Decisions
> Assignment for September 26, 2019
> Author:  Mike Rouw

### Summary of Assignment:  
This assignment is to review three different data files concerning observations of plankton and identify problems or potential issues with the form and format for the data collected and shared thus far.  Specifically, the assignment is to identify problem areas within the data, and then recommend a table-format for collecting the data in the future.

**Problems and Issues with the Data:**
The following will outline several issues with the data, in structure, content and definition.

*Three files* – It would be much easier to analyze the data if all observations were captured in a single file.

*No metadata* – There is very little description of the data itself, or its purpose, or anything about the methods use to capture the data.  This would be helpful over time as it is likely that multiple people will be taking the data samples.

*Inconsistent labeling* – There is little consistency in labeling the columns for the data.  Z in one file seems to be Depth in another.  Density in one file seems to be Count/Liter in another.  However, without consistency it is not possible to know for sure.

*Inconsistent formatting* – One of the data files separates the data for the two different sub-species of plankton, while the others identify the sub-species by column.  This makes it difficult to combine the data observations into a consistent format for analysis.

*Lack of definitions* – There is little or unclear definitions given for the specific columns of data in the files.  Without clear definitions, it is difficult to determine what analysis could be done on the dataset.  For instance, is the depth in meters?  Or some other measurement?

*Lack of time of day* – The description of the study mentions that there are differences to be noted based on day or night observations.  The files seemed to have no indication of a time of day when the measurements were taken.

*Missing data* – Some of the observations are simply missing data elements.  Without the proper values, it may be difficult to provide a proper analysis.

**Recommendations for Data Gathering:**
Below are the recommendations for the gathering of data in the future.

*Data Rows* – Each observation should be captured in a row in the table, with new observations adding new rows as they occur.

*Data Columns* – These should contain all relevant information about the observation.  Here are the columns that are recommended:
1. Date – This is the date of the observation (YYYYMMDD)
2. Time – This is the time of the observation (HHMM) on a 24-hour clock
3. Day/Night – This is a day/night indicator (D or N)
4. Location – This is an indicator of the observation location (A or B)
5. Temp – This is the temperature measured (degrees F or C)
6. Chlorophyll – This is the measurement of the chlorophyll
7. Cuni Density – This is the number of Cuni measured (count/liter)
8. Cuni Size – This is the diameter of the Cuni colony as measured (mm)
9. Chippo Density – This is the number of Chippo measured (count/liter)
10. Chippo Size – This is the diameter of the Chippo colony as measured (mm)

*Metadata* – A description for the overall purpose of the data, as well as measurement procedures and data value definitions should be developed for the dataset.

Below is a sample of a table which may be used to better organize the data collection for this study.  The first column is a unique, incremental observation number just to sort the data.

| Number | Date | Time | D/N | Location | Temp | Clorophyll | CuniDensity | CuniSize | ChippoDensity | ChippoSize |
|:------:|:--------:|:----:|:---:|:--------:|:-------:|:----------:|:-----------:|:--------:|:-------------:|:----------:|
| 1 | YYYYMMDD | HHMM | D/N | A or B | degrees | measure | count/L | mm diameter | count/L | mm diameter |

*Author: Mike Rouw*

*Proofreader: Mike Rouw (individual assignment)*

