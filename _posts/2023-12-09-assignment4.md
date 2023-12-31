---
title: "Clustering and Classifying Images"
excerpt_separator: "<!--more-->"

tags:
  - Assignment
  
---


## *Corpus of Flowers*

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

## Part2: Classification of Images

For the second part of the assignment, I took the large dataset that I had and just split it into smaller subsets based on the different flower categories, such as color, number of flowers in the image, and type of flower. The main aim of this exercise was to look at how easily the algorithm understood the classification that I was implementing. By analyzing the confusion matrix, I was able to evaluate the accuracy of the algorithm in correctly classifying the images.

> Color classification 

<img src="/assets/images/colorCM.png" style="zoom:50%;" />

Firstly, I put the flowers into different groups depending on their colors, such as white, pink. In order to see how well the algorithm could differentiate the colors, I created a pink-purple subset that contained flowers that had both pink and purple colors. This allowed me to assess the algorithm's ability to accurately classify flowers based on their specific colors. I also had a subset of flowers that had traces of white on their petals. All the subsets had a fairly similar number of flowers. According to the confusion matrix that was generated, it was clear that the inception algorithm did a great job of accurately classifying the flowers based on their specific colors. The confusion matrix showed a high percentage of correct classifications for both the pink-purple and whitish subsets. Furthermore, the algorithm was able to clearly differentiate the white and whitish subsets, even though I thought it would pose a challenge to the algorithm. On the other hand, we can see that when it comes to pink flowers, the inception algorithm confused some of them with pink-purple and white flowers. Overall, the inception algorithm demonstrated strong performance in accurately classifying flower colors.


**Color confusion** *The snapshot below shows the flowers in pink-pink purple and white-pink categories, respectively, which the algorithm confused.
From the first picture, we can see that flowers have traces of both pink and purple, which is perhaps what made it difficult for the algorithm to accurately classify them. In the second picture, some flowers appear to be a mix of white and pink, which may have caused confusion for the algorithm.*
{: .notice--warning}

<img src="/assets/images/pink:pinkpurple.png" style="zoom:50%;" />
<img src="/assets/images/white:pink.png" style="zoom:50%;" />

> Below is the image grid for this classification, and we can see flowers cluster depending on their color, with very few exceptions. For instance, on the far left, we observe two purple flowers in the whitish subset when all the other purple flowers are in the central part of the grid. 

<img src="/assets/images/colorGrid.png" style="zoom:50%;" />
<img src="/assets/images/colorcluster1.png" style="zoom:50%;" />

> SqueezeNet Algorithm Results 

<img src="/assets/images/squeezeCM.png" style="zoom:50%;" />
<img src="/assets/images/pink,purple.png" style="zoom:50%;" />

<img src="/assets/images/squeezeGrid.png" style="zoom:50%;" />
<img src="/assets/images/squeezecluster.png" style="zoom:50%;" />

> Type classification 

The second classification was based on the types of flowers, where I put the flowers into groups like morning glories, daisies, and sunflowers. I used the computer algorithm to see how accurately it could classify the images into their respective flower categories. I first used the inception algorithm and then the SqueezeNet algorithm to compare their performance in flower classification. 

> Confusion Matrices for inception and Squeeze algorithms respectively

<img src="/assets/images/typeinceptionCM.png" style="zoom:50%;" />
<img src="/assets/images/typeSqueezeCM.png" style="zoom:50%;" />

Both algorithms accurately classified the images into their respective flower categories, achieving a high accuracy rate. They both only confused one daisy flower for a sunflower, but overall, they performed exceptionally well. 

<img src="/assets/images/daisy:sunflower.png" style="zoom:50%;" />
<img src="/assets/images/daisy:sunflowerSqueeze.png" style="zoom:50%;" />

However, it was interesting to see that in the clustering process for both algorithms, there were clusters that contained both daisies and sunflowers; however, in the classification process, this confusion was resolved. 

> Confusion in the clusters generated in the clustering process for the inception and SqueezeNet algorithms 

<img src="/assets/images/typecluster2conf.png" style="zoom:50%;" />

<img src="/assets/images/squeezeconf.png" style="zoom:50%;" />

> Image Grid for Inception and SqueezeNet algorithms respectively

<img src="/assets/images/inceptiontypeGrid.png" style="zoom:50%;" />
<img src="/assets/images/squeezetypeGrid.png" style="zoom:50%;" />

> Number of flowers classification 

> Confusion Matrices for inception and Squeeze algorithms respectively

<img src="/assets/images/inceptionNumberCM.png" style="zoom:50%;" />
<img src="/assets/images/squeezenumberCM.png" style="zoom:50%;" />

> Some of the confusions that arose in inception and squeezeNet algorithms respectively

<img src="/assets/images/1:2inceptionconf.png" style="zoom:50%;" />
<img src="/assets/images/1:3inceptionconf.png" style="zoom:50%;" />

<img src="/assets/images/1:3Squeezeconf.png" style="zoom:50%;" />
<img src="/assets/images/2:3squeezeconf.png" style="zoom:50%;" />

> Image Grid for Inception and SqueezeNet algorithms respectively

<img src="/assets/images/inceptionnumberGrid.png" style="zoom:50%;" />
<img src="/assets/images/squeezenumberGrid.png" style="zoom:50%;" />

## Distant Viewing

Throughout this assignment, all the concepts that were discussed in the book [Distant Viewing: Computational Exploration of Digital Images](https://rb.gy/n63hqn) became very apparent. As discussed in the book, the first step towards clustering and classifying images is annotation, which involves assigning labels based on identifiable features within the images, such as color, shape, texture, or the presence of specific objects. And this is what I did as well. In addition to that, this initial stage helped me make changes if need be to the dataset. Furthermore, I realized that image visualization is not a one-step process but rather a continuous and iterative one. The book emphasized the importance of experimenting with different visualization techniques and refining them based on the specific goals and requirements of the project. This iterative approach allowed me to gain deeper insights into the dataset and uncover patterns and relationships that were not initially apparent. 

> The screenshot below represents the workflow for image analysis that was discussed in the book 

<img src="/assets/images/distantViewing.png" style="zoom:50%;" />

