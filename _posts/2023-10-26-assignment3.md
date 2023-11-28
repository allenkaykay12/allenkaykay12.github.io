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

<img src="/assets/{kepler.gl}.png" style="zoom:50%"/>

<img src="/assets/images/male.png" style="zoom:50%;" />
<img src="/assets/images/female.png" style="zoom:50%;" />
