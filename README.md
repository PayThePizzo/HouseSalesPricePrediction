# Prediction of House Prices' Sales

Problem definition
The problem definition works as the driving force for a data analysis plan execution.

How can we assess the value of a house, or better, the sale price? The short answer is we cannot, since the database is not made for that. However, we can predict the log-error.

logerror=log(Zestimate)−log(SalePrice) 

Now, it is easier to understand what our real goal is: predicting a number through regression. This is something we know how to do!

Understand the context: hosing-market in the west coast of the U.S.A.
Other than finding links between features, we need to point out some factors we cannot easily include when making our predictions.

We are given a "full list of real estate properties in three counties (Los Angeles, Orange and Ventura, California) data in 2016 and 2017", What problems are we facing now?

We are focusing on a particular geographical area, which we are not familiar with;
We are focusing on a market we have no prior domain-knowledge of;
There is no price sale in the dataset.
Therefore, we have not a clue of how the market is going for houses there, nor we know what gets a house to a particular sale price (the weight of each feature). While the first can be hardly tracked, we can find out about the latter two through data exploration and domain research.

As we know, datasets rarely are perfect, so we must perform some magic to make it usable with our regression algorithms and find out useful information!

Need for a clean & clear dataset
What do we need to do to achieve a clean dataset?

The following approac allows us to use a vast variety of cleaning and feature engineering strategies to converge to a perfect training dataset.

Basic Exploration
Data Cleaning & Feature Engineering
Modeling
Export
However, we will not follow a linear approach. We will improve the quality of the dataset as soon as we have the chance

---

### Credits & Copyright
As we know from this guideline by [University of Michigan](https://guides.lib.umich.edu/c.php?g=282964&p=3285995), 
there is no clear protocol on how to cite datasets. However, I will try my best 

#### Data

    @article{OpenML2013,
      author = {Joaquin Vanschoren and Jan N. van Rijn and Bernd Bischl and Luis Torgo},
      title = {OpenML: networked science in machine learning},
      journal = {SIGKDD Explorations},
      volume = {15},
      number = {2},
      year = {2013},
      pages = {49-60},
      url = {http://doi.acm.org/10.1145/2641190.264119},
      doi = {10.1145/2641190.2641198},
      publisher = {ACM}
    }



The dataset used was taken from [openml.org](https://www.openml.org/),  [https://creativecommons.org/licenses/by/4.0/]


#### Images
The background image of this repo was downloaded from [Wallpaper Flare](https://www.wallpaperflare.com/reflection-hallstattersee-alps-tourism-bad-goisern-town-wallpaper-tgifx/download/1280x640)
and follows these [terms of usage](https://www.wallpaperflare.com/terms-of-use).

##### Final Note
All digital supports (such as images), are not of my property and are protected by the law on copyright.

If you recognize that I included any of your work without permission, or you feel like I should remove any of the
content, please contact me as soon as possible.
