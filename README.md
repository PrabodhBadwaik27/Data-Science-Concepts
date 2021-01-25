# Data Science Concepts
[Currently in making]  
This repository contains some of the most important concepts which must be studied and understood in order to be a better Data Science contributer.   
**Pre-requisite:** Willingness to learn  
**Expertise:** BEGINNER, INTERMEDIATE or ADVANCED  
  
## Index  
#### 1. Statistics  
1.1 [Datatypes in Statistics](#1.1.-datatypes-in-statistics)
    
    
 ## 1. Statistics
 
 ### 1.1. Datatypes in Statistics
 It's very important to understand this basic concept of Datatypes before even touching a *single dataset*.  Because it is the prerequisite for performing Exploratory Data Analysis(EDA) successfully. Data Science professionals emphasis on this because knowing the different types of data and their unique characteristics helps you not only to perform *feature transformations* correctly but also makes *visualization* of certain attributes super easy.

*NOTE: As the differences and characteristics are notably small and little confusing, it's better to remember them through analogies, examples or ways of interpretation. I have provided some, you are welcome to contribute and suggest* ^.^

Before going straight into the core, it's better to back ourselves up with a concept of **True Zero**
#### True Zero
Metrics whose values **can fall below zero** are called to hold **true zero** whereas, if this is not possible, they are said to not possess a true zero.  
Confused? Understanding this will be easy with example. Consider two measures: cm for **length** and deg C for **temperature**.  
It's possible that the temperature outside dip below zero to -10 deg C, hence it's called to hold true zero.  
Whereas, for any physical object, it's impossible to have length as -1 cm(!). And same is for weight too. Hence, length and weight can't have a true zero.  

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
        This type of metric values *cannot* be divided or multiplied to obtain a meaningful measure. 
        (e.g temperature; having 20 deg C at 'A' and 40 deg C at 'B' doesn't mean that B is twice hot as A. That means division doesn't make any sense)  
        - **Ratio**  
        Ratios has *true zero*.
        This type of metric values can be divided or multiplied to obtain a meaningful measure of characteristic.   
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
 
