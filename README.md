# Prediction Task: Home Value Prediction

---

## Data & Web Mining - Lab Project Statement

### Prediction Task: Home Value Prediction

The dataset is found [here](https://www.openml.org/search?type=data&status=active&id=43926&sort=runs)

### To be delivered 

1. One or more notebooks (and possibly other python files) and a 5-page pdf
report discussing your critical choices. 
    * No more than 5 pages! 
    * The pdf report can be the export of a notebook.
2. Project is discussed at the oral exam, about one week after the written exam.
3. Deadline: a couple of days before the oral exam via Moodle.

### Work to be done

* Add custom features to your dataset (e.g., avg. prices in the same
geographical area) and evaluate their contribution
* Compare at least two prediction methods, after fine-tuning their parameters
* Investigate instances with the most correct predictions and with the most
wrong predictions. Do they have some peculiarities? Any strange feature
distribution?
* Experiment beyond scikit-learn, e.g., with LightGBM or XGBoost or CatBoost
* Can be done in groups, multiply the work by the size of the group

### Evaluation

* Quality of the report
* Quality of the code (I'll ask about every single line of code)
* Depth of the analysis
* Project can be insufficient (the exam is not passed), or it may add up to 3 points to the score of the written exam

---

## My Project Entry


### Requirements for the project


### Process

Even though, ideally, the process of exploratory data analysis should leave the data untouched, I decided to perform changes whenever I had the chance to improve the quality of the data. This was crucial as the presence of outliers is very high and there is evidence of data incoherence. What I mean by this, is that even though it is believed that the best approach is to separate the *passive* analysis and the actual feature engineering phase, I personally believe it is possible to do both for each step. Namely, at any moment we can use the inference we make to modify the data in order to achieve the best version of the original dataset.

### Structure of the notebooks

The project has 5 notebooks:
1. Introduction and Data Preparation
    * Domain research, Context of Data
    * Preliminary Dataset Overview
    * Correction of possible errors and coherence check 
    * Some preliminary feature creation
2. Exploratory Data Analysis 
    * Univariate, Bivariate and Multivariate analysis
    * Outliers removal 
3. Data Encoding, Type Conversion and Feature Selection
    * Encoding of Categorical Features
    * Conversion of all types
    * Feature Importance Assessment
    * Feature Selection
4. Bagged Random Forest Regression
    * Data Rescaling
    * Train, Validation, Test
    * Hyperparameters Tuning
    * Diagnostics and Evaluation
5. Graph Neural Network Regression
    * Data conversion to graph and edges creation
    * Data Rescaling
    * Train, Validation and Test loops
    * Diagnostics and Evaluation

**Gianmaria Pizzo - 872966@stud.unive.it**

---

### Credits & References
As we know from this guideline by [University of Michigan](https://guides.lib.umich.edu/c.php?g=282964&p=3285995), 
there is no clear protocol on how to cite datasets. However, I will try my best 

#### Dataset

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

---

##### Final Note
All digital supports (such as images), are not of my property and are protected by the law on copyright.

If you recognize that I included any of your work without permission, or you feel like I should remove any of the
content, please contact me as soon as possible.
