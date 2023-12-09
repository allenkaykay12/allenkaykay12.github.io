---
title: "Post: Assignment 4"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Assignment
  
---


## *Draft: Clustering and Classifying Images*

For this part of the assignment, I chose to work with images of flowers. Even though I don't have a lot of knowledge about flowers, I thought it would be very interesting to study and understand how computer algorithms can analyze and classify different types of flowers based on their visual features. Since most of the algorithms are mainly trained to analyze and classify objects such as animals or other objects, working with flowers would provide a unique challenge. This is because flowers have a wide variety of shapes, colors, and different types of patterns, making it more complex for algorithms to accurately classify them. I wondered which of the features the algorithms would prioritize when analyzing and classifying flowers, whether it would be the shape, color, or pattern.

In constructing the corpus for this assignment, I did research on different online platforms, such as **Kaggle**, that have large datasets of images. I also performed the normal Google search to find any other datasets that may be present on the internet. For the dataset that I used for the assignment, I found it on [website](https://shorturl.at/qHIS0). It initially contained thousands of images of various flowers, and they all had names that were all numerical. The data set contained flowers from all around the UK and was divided into 102 categories. However, this was too large for the analysis. I decided to narrow down the dataset into a smaller set. The images used were randomly selected, but since I had to do classification after, I wanted to ensure that the dataset had a balanced representation of each flower category. Therefore, I manually selected an equal number of images from each category to create a more manageable dataset for analysis. In addition to that, my data set kept changing depending on the classification that I was doing. I would add flowers from the bigger set in case I needed more examples for a specific category. 

## Analysis and Interpretation of the Results 

For image analysis, I used orange data mining software to study and understand how computer vision algorithms can classify and recognize different flower categories based on their visual features. I applied various algorithms, such as Inception, Painters, and SqueezeNet, and it was interesting to notice that different algorithms resulted in different clusters. This could perhaps be due to the fact that each algorithm has its own unique way of interpreting and extracting visual features from the flower images. 

> Below are the image grids obtained using SqueezeNet, Inception, Painters, Deploc algorithms

<img src="/assets/images/image1.png" style="zoom:50%;" />
<img src="/assets/images/image2.png" style="zoom:50%;" />
<img src="/assets/images/painters.png" style="zoom:50%;" />
<img src="/assets/images/image3.png" style="zoom:50%;" />

**OpenFace:** *When I tried using the OpenFace algorithm, all the images were skipped since this algorithm is designned to work with faces.*
<img src="/assets/images/openFace.png" style="zoom:50%;" />

{: .notice--warning}
