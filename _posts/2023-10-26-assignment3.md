---
title: "Post: Assignment 3"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---

##DRAFT: Spatial Data: *Brooklyn City and Business Directory*

For the spatial data assignment, I worked with [**The Brookly City Business Directory 1879–80.**](https://shorturl.at/oqCJY)
This directory contains information about businesses in Brooklyn during the years 1879–1880. It includes the names of people, their professions, and street addresses. When I chose this corpus, I wanted to look at the spatial distribution of different types of professions in Brooklyn and analyze how they were clustered in different neighborhoods. By mapping the professions onto the street addresses, I wanted to explore if there were any patterns or concentrations of specific professions in certain areas of Brooklyn. In addition to that, I looked at how the profession was related to gender and whether there were any noticeable disparities in the distribution of professions based on gender. This analysis aimed to provide insights into the occupational landscape in Brooklyn. 

Since there is a lot of information available in the directory, I didn't do manual data extraction. Instead, I used ChatGPT to automate the process of extracting the data. This allowed me to efficiently gather a large amount of information, and this ensured consistency and accuracy in the data extraction process, reducing the chances of human error. To extract the data, I prompted ChatGPT to create a CSV file that contained the names of people, their occupations, and street addresses. ChatGPT was able to classify all the information I gave it, but I needed to do some cleaning up to remove some formatting errors in the CSV file.  I randomly chose different names from different pages of the directory so as to have diversity in the extracted data. This helped me work with different types of names and ensure a more comprehensive dataset. 

>Below is a snapshot of the prompt to ChatGPT and the CSV file generated 

<img src="/assets/images/prompt.png" style="zoom:50%;" />
<img src="/assets/images/response.png" style="zoom:50%;" />

**Note:** *The snapshot above is just a small part not the entire CSV file*
{: .notice--warning}

## Enriching Data: *GeoCoding*

To enrich the data, I geocoded the data by converting the street addresses into geographic coordinates: latitude and longitude. When I used the original addresses, there was a lot of missing data because some addresses were not recognized by the geocoder. To solve this problem, I used the **CONCATENATE** function in Google Sheets to add Brooklyn, New York, to the already existing addresses. This helped improve the geocoding accuracy and reduced the amount of missing data significantly. With concatenation, Geocoder was able to convert all the addresses into geographic coordinates successfully. This method allowed me to obtain accurate latitude and longitude values for each address, ensuring the reliability of my data analysis. 

<img src="/assets/images/missing.png" style="zoom:50%;" />
<img src="/assets/images/concat.png" style="zoom:50%;" />

## Data Visualization 

For data visualization, I used [*Kepler.gl*](https://kepler.gl/), an online platform that allows one to create interactive maps and visualizations. I used Kepler.gl because it provides a user-friendly interface with various customization options, such as filters and layers, which makes it easier to study and understand the relationship between the geographic coordinates and other variables in the data. 

<img src="/assets/images/kepler.gl_general.png" style="zoom:50%"/>

The picture above is a general representation of different occupations in Brooklyn, New York. The colors on the map represent different types of occupations, and each circle represents an individual. If the circles of the same color are close to each other, it indicates that individuals with similar occupations tend to cluster together geographically. However, this map visualization didn't give me a lot of information since there were too many occupations, and by compressing everything into 11 classifications, there wasn't much to learn about the specific types of occupations in Brooklyn. So I decided to further the occupations into different categories, such as food, law enforcement, wood, beauty, and so on. This further categorization allowed me to put together occupations that had similar skill sets or job requirements, giving me a better understanding of the specific industries present in Brooklyn. By analyzing these categories, I was able to identify patterns and trends within each industry, such as the concentration of food-related occupations in certain neighborhoods.

>The map below represents the further classification of occupations 

<img src="/assets/images/kepler.gl_occupation.png" style="zoom:50%"/>

## Gender and Professions in Brooklyn

> Visual for the males and females

<img src="/assets/images/kepler.gl_gender.png" style="zoom:50%"/>

I also looked at gender distribution in relation to occupations and found that more men were in the work force compared to females. This could be due to various factors, such as societal norms, discrimination, or personal preferences. To get the gender of different people, I took their first names and asked ChatGPT to classify them into "male" and "female" based on common gender associations with names. The association was accurate because, had it been me, I would have done the same thing, just looking at the name and thinking about how many people I know who have such a name and whether they are male or female. When I used "occupations" and "gender" filters, most of the females who were shown on the map were mostly widows, with a few exceptions. It was interesting to note that for the widows, their husbands' names were put in brackets, but these women did not have any occupation that they did. This observation suggests that the association between names and gender was not only accurate but also reflective of societal norms during that time period. Additionally, it raises questions about the roles and identities of these widowed women in society, as their lack of occupation may indicate a dependence on their husbands' names for recognition or status. 

<img src="/assets/images/promptG.png" style="zoom:50%;" />
<img src="/assets/images/gender.png" style="zoom:50%;" />

> Map that represents females and their occupations 

<img src="/assets/images/female.png" style="zoom:50%;" />

On the other hand, there was diversity in the kinds of jobs that men did. These activities ranged from drivers, cigars, grocers, lawyers, and so on. This diversity in occupations highlights the varied opportunities that were available to men during that time, giving them a chance to achieve social mobility as well as economic independence. This can also be supported by the fact that there is a higher representation of men in the directory book of businesses, indicating their active participation in the workforce. Even now, there is still a gender disparity in certain industries and occupations, with men often dominating fields such as engineering, technology, and finance. However, efforts are being made to promote gender equality and encourage women to pursue careers in traditionally male-dominated fields. So this representation of the ratio of males and females and the kinds of jobs from the 1879–1880 perspective is accurate in reflecting the historical gender dynamics of that time period. 

> Map that represents males and their occupations 

<img src="/assets/images/male.png" style="zoom:50%;" />

> Classification: different jobs done 

<img src="/assets/images/kepler.gl_jobs.png" style="zoom:50%"/>
