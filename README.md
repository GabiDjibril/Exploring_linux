Ce projet consiste à explorer uun dataFrame contenant les différentes modifications apportées auu noyau linux sur ces dernières années.
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GabiDjibril/Exploring_linux/HEAD)

| 1502382966#Linus Torvalds    |
|------------------------------|
| 1501368308#Max Gurtovoy      |
| 1501625560#James Smart       |
| 1501625559#James Smart       |
| 1500568442#Martin Wilck      |
| 1502273719#Xin Long          |
| 1502278684#Nikolay Borisov   |
| 1502238384#Girish Moodalbail |
| 1502228709#Florian Fainelli  |
| 1502223836#Jon Paul Maloy    |

1.Introduction

In this notebook, we will analyze the evolution of a very famous open-source project – the Linux kernel. The Linux kernel is the heart of some Linux distributions like Debian, Ubuntu or CentOS. Our dataset at hand contains the history of kernel development of almost 13 years (early 2005 - late 2017). We get some insights into the work of the development efforts by identifying the TOP 10 contributors and visualizing the commits over the years.

2.Reading in the dataset The dataset was created by using the command git log --encoding=latin-1 --pretty="%at#%aN" in late 2017. The latin-1 encoded text output was saved in a header-less CSV file. In this file, each row is a commit entry with the following information: timestamp: the time of the commit as a UNIX timestamp in seconds since 1970-01-01 00:00:00 (Git log placeholder "%at") author: the name of the author that performed the commit (Git log placeholder "%aN") The columns are separated by the number sign #. The complete dataset is in the datasets/ directory. It is a gz-compressed csv file named git_log.gz

2.Getting an overview The dataset contains the information about every single code contribution (a "commit") to the Linux kernel over the last 13 years. We'll first take a look at the number of authors and their commits to the repository.

3.Finding the TOP 10 contributors¶ There are some very important people that changed the Linux kernel very often. To see if there are any bottlenecks, we take a look at the TOP 10 authors with the most commits.

4.Wrangling the data For our analysis, we want to visualize the contributions over time. For this, we use the information in the timestamp column to create a time series-based column.

5.Wrangling the data For our analysis, we want to visualize the contributions over time. For this, we use the information in the timestamp column to create a time series-based column.

6.Treating wrong timestamps As we can see from the results above, some contributors had their operating system's time incorrectly set when they committed to the repository. We'll clean up the timestamp column by dropping the rows with the incorrect timestamps.

7.Grouping commits per year To find out how the development activity has increased over time, we'll group the commits by year and count them up.

8.Visualizing the history of Linux Finally, we'll make a plot out of these counts to better see how the development effort on Linux has increased over the the last few years.

9.Conclusion:   

Thanks to the solid foundation and caretaking of Linux Torvalds, many other developers are now able to contribute to the Linux kernel as well. There is no decrease of development activity at sight!  
