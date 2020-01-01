Getting and Cleaning Data Course Project
==============================================

This file describes how run_analysis.R script works.

1. First, unzip the data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and rename the folder with "UCI HAR Dataset" to contain all provided data.

2. Make sure the folder "UCI HAR Dataset" is set as current working directory using setwd() command.

3. Second, use source("run_analysis.R") command in RStudio.

4. Third, you will find two output files are generated in the current working directory:
     * z-merged_data.txt (8150 KB): it contains a data frame called cleanedData with 10299*68 dimension.
     * z-data_with_means.txt (220 KB): it contains a data frame called result with 180*68 dimension.

5. Finally, use data <- read.table("data_with_means.txt") command in RStudio to read the file. Since we are required to get the average of each variable for each activity and each subject, and there are 6 activities in total and 30 subjects in total, we have 180 rows with all combinations for each of the 66 features.