# Data Science Concepts
[Currently in making]  
This repository contains some of the most important concepts which must be studied and understood in order to be a better Data Science contributer.   
**Pre-requisite:** Willingness to learn  
**Expertise:** BEGINNER, INTERMEDIATE or ADVANCED  
  
## Index  
- Data Science Project Lifecycle
    - [**Introduction**](#introduction)
- Data Science Project Scopes Implementation Guide
    - **Data Quality Assessment**
    - **Exploratory Data Analysis**
- Data Science Concepts & Theoretical Knowledge
    - **Statistics**  
        - [Datatypes in Statistics](#datatypes-in-statistics)  
    
## Data Science Project Lifecycle
 
### Introduction
Being a state-of-the-art domain, the different participants of Data Science projects might have different titles for the wrappers of reposibilities and tasks to be performed in order to achieve the desired objectives and resolve the business problems. Although, all the Data Science projects run through the six major processes as stated below.  
**1. Problem Framing**  
**2. Collection of Raw Data**  
**3. Data Preprocessing**  
**4. Data Exploration**  
**5. In-Depth Analysis of Data**  
**6. Results Presentation**  

#### 1. Problem Framing
- In order to frame the problem, **ask a lot of questions.**
- Translate an ambiguous request from client into a well defined (constrained with objectives) problem statement after understanding the business/industry priorities and motives
- **Skills Required**
    - Deep knowledge about *client's business* and *targetted product*
    - Undestanding of the strategies used by business 
    - Selection and enablement of team

#### 2. Collection of Raw Data

#### 3. Data Preprocessing

#### 4. Data Exploration

#### 5. In-Depth Analysis of Data

#### 6. Results Presentation

## Data Science Project Scopes Implementation Guide

### Data Quality Assessment
**Data Quality Assessment** or **DQA** is a foremost process in the [*Data Preprocessing stage*](#data-science-project-lifecycle) performed by *Data Analysts* in the team. DQA is nothing but ensuring the quality of collected data before using it for forecasting analytical results.      
  
**Why is it important to perform Data Quality Assessment?**
In the real world, data is collected from the various sources, which might be part of different datawarehouses handled by various organizations or even data manually collected by individuals. Thus, it is very prone to data entry errors, missing fields due to unavailability of data, different standards regarding datatype, schema, classification followed in data collected from different sources and vast inconsistency (i.e. same attribute/title signifies different meaning in different datasets).  In this scenario, if such *noisy data* is used for model training or forecasting directly, the conclusions drawn can't be relied upon.  
Hence DQA ensures that the highest quality data is provided for the further processing.  
  
In this process, Every attribute is closely analysed, the usability is verified in terms of datatypes & values; if needed, datasets/attributes are transformed to meet the required standards.  

/*
At the first glance, DQA might seem to be a quite complicated task. Also, considering that the Data Preprocessing Stage alone spans over 80% of the time of complete project, it's a difficult task. But, following a systematic framework over the process would certainly make the task easier and achievable. 
*/

### Exploratory Data Analysis (EDA) [Currently in Making]
Exploratory Data Analysis is also abbreviated as EDA, or called as Data Exploration.  
1. Choose **Target Variable**

2. Type of *Target Variable*  specifies the type of model to implement;
  - If *Discrete*, *Classification* model
  - If *Continuous*, *Regression* model
3. Review *Relevancy* of all attributes in datasets towards the *target variable* prediction.

4. Bivariate Analysis
Correlation Analysis
  - Continuous v/s Continuous Attributes
    - Heatmap - Visual Correlation Map
  - Continuous v/s Categorical Attributes 
    - z-value, t-value Test
  - Categorical v/s Categorical Attributes 
    - Chi-square Test

5. Missing Value Treatment
  - Types of Missing Values
    - Missing at complete random (MACR) #Deletion can be used
    - Missing at random (MAR) #Deletion can be used; #Correlation analysis is another method
    - Missing that depends on unobserved predictors
    - Missing that depends on missing value 
  - Mising Value Imputation Techniques
    - Deletion
      - List wise deletion #Direct deletion
      - Pair wise deletion #Correlation analysis
      - Column deletion #In case of high missing value percentage for certain attribute
    - For Time-Series Data
    - For General Data
      - Continuous data
        - Mean/ Median imputation
          - Mean #Normal Distribution
          - Median #Skewed Distribution
          - Mode #Skewed Data
        - Linear regression
      - Categorical data
        - Mode imputation
        - Logistic regression

6. Outlier Analysis
The simplest way to detect the occurrence of outliers in any attribute is to plot them graphically. Different types of visual representation plots used for outlier detection are;
- Box plot
  - Used for both Univariate and Bivariate Analysis
  - Plotted between:
    - Continuous Variable
    - Continuous and Categorical Variables
- Scatter plot
  - Used for Bivariate Outlier detection of two Continuous Variables
  
7. Feature Engineering


 ## Statistics

 ### Measures of Central Tendency

 ### Measures of Dispersion
 1. ***Variance $s^{2}$***
  - Variance is the measure of **dispersion** around the *mean*.
  - It is determined as **squared difference of all the values with mean**.  
  <img src="https://render.githubusercontent.com/render/math?math=s^{2} = \frac{\sum (x_{i} - \bar{x})^{2}}{N - 1}">  

 2. ***Standard Deviation***
  - Standard Deviation is another measure of dispersion, only **termed in same unit** as the data points.
  - It is determined by calculating the **square root of Variance**

 3. ***Covariance***
  - Covariance is the measure of **join variability** of two random variables.
  - Covariance values can be *positive* or *negative*.
  **Positive** value denotes that, greater value of one variable corresponds to greater value of other variable.  
  Whereas, **negative** covariance suggests that lesser value of one variable corresponds to higher value of other variable.  
  - However, *magitude of covariance doesn't specify the strength of relationship, but only direction*.   
  - **Correlation Coefficient** is normalized version of covariance, which specifies the strength of the linear relation by its magnitude.    
  <img src="https://render.githubusercontent.com/render/math?math=cov_{x,y} = \frac{\sum\limits_{i=1}^{n}{(x_i-\overline{x}) \cdot (y_i-\overline{y})} }{n-1}">   

 
 ### Datatypes in Statistics
 It's very important to understand this basic concept of Datatypes before even touching a *single dataset*.  Because it is the prerequisite for performing Exploratory Data Analysis(EDA) successfully. Data Science professionals emphasis on this because knowing the different types of data and their unique characteristics helps you not only to perform *feature transformations* correctly but also makes *visualization* of certain attributes super easy.

*NOTE: As the differences and characteristics are notably small and little confusing, it's better to remember them through analogies, examples or ways of interpretation. I have provided some, you are welcome to contribute and suggest* ^.^

Before going straight into the core, it's better to back ourselves up with a concept of **True Zero**
#### True Zero
Metrics whose values **can't fall below zero** are called to hold **true zero** whereas, if it's possible, they are said to not possess a true zero.  
**OR** If the value being 'zero' for certain metric depicts absence or no existence of the entity, it's said to possess true.  
Confused? Understanding this will be easy with example. Consider two measures: cm for **length** and deg C for **temperature**.  
It's possible that the temperature outside dip below zero to -10 deg C, hence it doesn't hold true zero.  
Whereas, for any physical object, it's impossible to have length as -1 cm(!). And length being 0cm means the objects is non-existent. Same holds true for weight too. Hence, length and weight has a true zero.  

- Types of Data  
   - **Categorical**  
   This type of data is *non-numerical* and describes *characteristics which can't be measured*. (e.g. Happiness)  
   Hence, this type of data is known to have **Qualitative Measurements**.
      - **Ordinal**
      It can be *ordered*.  
      (e.g. Easy, Medium, Hard; *Comparison of ease*)  
      ^.^ *Remember the simple abb.: Ord-inal = Ord-ered*
      - **Nominal**
      It can not be *ordered*.  
      (e.g. Summer, Winter, Monsoon; *As before, weather can't be compared*)  
      ^.^ *N-O-minal = Not-Ordered*  
    - **Numerical**
    As the name suggests, this type of data is *numerical* and may describe *measure* or *quantity*.  
      - **Continuous**
      Continuous data represents measurements or quantity.  
      Thus, such data is known to have **Quantitative Measurements**.
      It *can be measured, but not counted*.  
      The answer to **How much?** may be a **decimal number**.  
        - **Interval**  
        Interval data doesn't have *true zero*.  
        Doesn't have equidistant ccale: This type of metric values *cannot* be divided or multiplied to obtain a meaningful measure. 
        (e.g temperature; having 20 deg C at 'A' and 40 deg C at 'B' doesn't mean that B is twice hot as A. That means division doesn't make any sense)  
        - **Ratio**  
        Ratios has *true zero*.
        It possess equidistant scale. This type of metric values can be divided or multiplied to obtain a meaningful measure of characteristic.   
        (e.g length; 10cm pencil is obviously twice as long as 5cm pencil)  
      - **Discrete**
      Discrete data is the data which must have non-continuous numeric values.  
      This type of data *can be counted, but not measured*.
      The answer to **How many?** will be a **whole number**.
      (e.g. No. of students | 'How many' students? can be answered only as a whole number and not in decimal!)  
      
#### Bonus Tip!  
_**Use of Visualization Method**_  
_For **continuous** datatype, following methods are used;_  
_1. Box plot; it is useful tool in case of data consisting **outliers** and to check the distribution of values_  
_2. Histogram_  
  
_For all other datatypes except **continuous** data, following methods are used;_  
_1. Frequency Distribution Tables_  
_2. Bar charts_  
_3. Pie charts; since it's difficult to notice the difference by looking at the pie chart, it is avoided at the workplaces_  
  
_For further explainations, refer the links attached;_
_[Reference 1](https://towardsdatascience.com/data-types-in-statistics-347e152e8bee)_,
_[Reference 2](https://www.questionpro.com/blog/ratio-scale-vs-interval-scale)_
 
