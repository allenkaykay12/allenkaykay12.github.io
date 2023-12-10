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

## Part1: Clustering: Analysis and Interpretation of the Results 

For image analysis, I used orange data mining software to study and understand how computer vision algorithms can classify and recognize different flower categories based on their visual features. I applied various algorithms, such as Inception, Painters, and SqueezeNet, and it was interesting to notice that different algorithms resulted in different clusters. This could perhaps be due to the fact that each algorithm has its own unique way of interpreting and extracting visual features from the flower images.

**Results:** *By observing the results from clustering, we can note that all of the algorithms are clustering the images based on their colors. However, what is rather interesting is the fact that, for different algorithms, these clusters appear on different sides of the image grid.*
{: .notice--warning} 

> Image grid for SqueezeNet

<img src="/assets/images/image1.png" style="zoom:50%;" />

> SqueezeNet Algorithm analysis

The SqueezeNet algorithm seems to have used **color** as a primary feature for clustering. Flowers with similar petal colors are grouped together, which is evident from the distinct blocks of color—yellows with yellows, pinks with pinks. In addition to that, the clusters also seem to take into account the **texture and pattern of the flowers**. For example, flowers with smooth petals are grouped separately from those with multi-layered petals, even if their colors are similar. The **shape and size of the flowers** and **their petals** appear to be another clustering criteria. For example, large, round flowers are in one cluster, while smaller, star-shaped flowers are in another. Overall, flowers with warm and vivid colors seem to be positioned lower on the grid, while as we move up, the colors appear cooler and less saturated. Furthermore, moving from left to right across the grid, there is a notable transition in the color and complexity of the flowers. On the far left, we observe a dominance of yellow flowers, which could be indicative of simpler shapes and fewer color variations. As we move to the right, the flowers become more complex in terms of the petal arrangement and patterns.

> The snapshot below indicates despite having similar colors and patterns the algorithm clustered them into other sub-clusters

<img src="/assets/images/Hierachy1.png" style="zoom:50%;" />
<img src="/assets/images/cluster1.png" style="zoom:50%;" />

<img src="/assets/images/cluster2.png" style="zoom:50%;" />

> Image grid for inception 

<img src="/assets/images/image2.png" style="zoom:50%;" />

> Inception V3 Algorithm analysis

The Inception algorithm seems to cluster based on the dominant colors of the flowers. The top row starts with flowers that are predominantly orange and red. As we move from left to right, there is a clear change in color. Across the grid, there is a mix of saturation levels and brightness, with both vibrant and lightly colored flowers scattered everywhere. Within each color cluster, there are variations in texture and pattern. For example, in the red and pink clusters, we can see flowers with both smooth and multi-layered petals grouped together. The bottom rows are primarily filled with yellow flowers. The sorting here seems to emphasize a different attribute since we can observe a mix of colors and different types of flowers being grouped together.

<img src="/assets/images/inception1.png" style="zoom:50%;" />
<img src="/assets/images/inception2.png" style="zoom:50%;" />

<img src="/assets/images/inceptioncluster.png" style="zoom:50%;" />
<img src="/assets/images/inceptioncluster1.png" style="zoom:50%;" />
<img src="/assets/images/inceptioncluster3.png" style="zoom:50%;" />


> Inception V3 VS SqueezeNet algorithm

Looking at the two image grids, we can see that for inception, the brighter colors are at the top, unlike in the SqueezeNet algorithm, where the brighter colors are at the bottom. This could suggest that the two algorithms prioritize different aspects of the images when sorting them. Inception seems to prioritize the visual appeal of brighter colors, while SqueezeNet prioritizes the arrangement of flowers based on their attributes, such as petal shape and color variety. In the inception algorithm, we can still see a clear color progression; however, it seems less about the brightness and more about the shade. The colors transition from oranges and reds to various shades of pink, purple, and then blues as we go from left to right. In addition to that, the bottom rows are dominated by yellow flowers, which are placed at the top and central parts of the grid for SqueezeNet. This suggests a shift in the algorithm’s emphasis or a different feature being prioritized in the clustering process. We still observe an apparent increase in complexity from left to right, with simpler flowers on the left and multi-petaled flowers towards the right in the inception algorithm. In both grids, we observe that the far-right end has flowers with complex features. The saturation appears to be more evenly distributed across the grid for the inception algorithm, with both highly saturated and less saturated flowers appearing throughout the grid rather than being confined to a specific area, as observed in SqueezeNet. In both algorithms, there are a few clusters that are more isolated from the main body of the grid, even though they are more common in the SqueezeNet algorithm.  This isolation could indicate that the algorithm finds these flowers to be significantly different from all others enough to separate them from the main clusters.

> Image grid for Deploc algorithm 

<img src="/assets/images/image3.png" style="zoom:50%;" />

> Clusters from the grid

<img src="/assets/images/deploccluster.png" style="zoom:50%;" />
<img src="/assets/images/deploccluster1.png" style="zoom:50%;" />
<img src="/assets/images/deploccluster2.png" style="zoom:50%;" />


> Image grid for Painters algorithm 

<img src="/assets/images/painters.png" style="zoom:50%;" />

> Clusters from the grid

<img src="/assets/images/paintercluster.png" style="zoom:50%;" />
<img src="/assets/images/paintercluster1.png" style="zoom:50%;" />
<img src="/assets/images/paintercluster2.png" style="zoom:50%;" />
<img src="/assets/images/paintercluster3.png" style="zoom:50%;" />

**OpenFace:** *When I tried using the OpenFace algorithm, all the images were skipped since this algorithm is designned to work with faces.*
{: .notice--warning}
<img src="/assets/images/openFace.png" style="zoom:50%;" />


