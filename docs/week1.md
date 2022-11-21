# Week 1 Summary

### 1. Machine Learning
Field of study that gives computers the ability to learn without being explicitly programmed.

### 2. AI General Intelligence
- Building machines as intellgent as humans.
- Machines try to behave, mimic human brain.

### 3. Supervised Machine Learning 
- Referes to Alogrithms that learn input to output mapping, x -> y mapping
- You provide learning algorithms expamples to learn from lables (right answers).
- Call it Supervised, baceause we try to supervise algorithm to give answers for a given input.

### i) Regression
- Type of supervised learning in which a learning algorithm learns to predict a number out of infinte possible values.

### ii) Classification
- Type of supervised learning in which we have to predict a category from a fixed set of possible values.
- Classification algorithm predict categories. Categories can be numeric or non-numeric.

### 4. Unseprvised Machine Learning
- Given data isn't associated with any output lables.
- We are not asked to diagnose whether a Tumor is `Benign` or `Malignant`. Instead, we have to find some pattern, structure, or something interesting in the data.
- We are not asked to predict output label.
- Call it unsupervised, baceause we are not trying to supervise algorithm to give right answers for a given input. Instead, we figure out what is interesting in the data.

### i) Clustering
- Find groups, clusters in the data.
- We divide (un-labelled) data in different clusters based on similar characteristics.
- Group similar data points together.
- Example <1> group customers into different market segments. 

    <2> categories of learners, e.g., growing skills, develop career, stay updated with AI.

### ii) Anomaly Detection
- Find something unsual in the data.
- Find unsual data points, e.g., unusual transactions.

### iii) Dimentionality Reduction
- Compress data using fewer numbers.
- Compress a large dataset into smaller dataset while loosing as little information as possible.
- Usually, resultant dataset has reduced features.

### 5. Types of Supervised Learning
- Regression
- Classification 

### 6. Types of Unsuprvised Learning
- Clustering
- Anomaly Detection
- Dimentionality Reduction 

### 7. Regression vs Classification Model
- Regression model > predicts numbers out of infinit possible values
- Classification models > predicts categories out of discrete, finite set of ouputs.


## Linear Regression Model
- Model fits straight line to data.

#### i) How do you get a trained Model?
> Training Set > Learning Algo > Model `f(x)`

#### ii) How Model predicts output?
> Features (x) > Model `f(x)` > Prediction (y^)

#### iii) How to represent `f(x)`?

$$ f_{w,b}(x^{(i)}) = wx^{(i)} + b \tag{1}$$
