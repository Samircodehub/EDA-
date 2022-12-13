# EDA-

plt.subplot()

![image](https://user-images.githubusercontent.com/108605935/207088450-97bb4f9e-6998-4ec2-a025-0c80026ca54b.png)
![image](https://user-images.githubusercontent.com/108605935/207232327-2f5ef984-7323-4257-949e-28e34bd07a32.png)


![image](https://user-images.githubusercontent.com/108605935/207231911-b87e5e2f-b406-449c-9452-b2701f0457e0.png)

Nominal data is a data where we cant order any categoes in order. While ordinal data is a data where categories can be ordered in meaningful way.
Nominal data include country, gender, race, hair color etc. of a group of people, while that of ordinal data includes having a position in class as “First” or “Second”


A positive correlation exists when two variables operate in unison so that when one variable rises or falls, the other does the same. A negative correlation is when two variables move opposite one another so that when one variable rises, the other falls.


# Exploratory Data Analysis(EDA)
In EDA as soon as possible we get the raw data because the entire Features engineering is actually done on the raw data itself.
So as soon as possible we get the raw we start doing the analysis now question arises here is that what kind of analysis we do ?

Check how many numerical features may be there . (we try to see numerical features with the help of drawing of different diagrams like histogram , pdf function )
Check categorical features ( In categorical features we are try the analyze category features like how many category feature may be there . In those feature may be we have multiple categories)
Checking for missing values (For checking checking missing value just try to visualize all the graphs all these graphs )
.Checking for outlier ( We can simply check whether there are outliers with help of box plot)
Handling Missing values ( There are many ways to handel missing value like mean , mode , median and many more )
Handling imbalanced Data Set
Treating Outliers
Scaling down the data (standardization and normalization)
Converting categorical data to numerical data(One hot encoding, Label encoding)

# Using StandardScaler() Function to Standardize Python Data
Standardization is a scaling technique wherein it makes the data scale-free by converting the statistical distribution of the data into the below format:
* mean - 0 (zero)
* standard deviation - 1
* ![image](https://user-images.githubusercontent.com/108605935/207280138-540799e3-3fe2-4d46-8309-3f93cfe797aa.png)

By this, the entire data set scales with a zero mean and unit variance, altogether.


# Mean/ Median /Mode imputation
![image](https://user-images.githubusercontent.com/108605935/207281320-3524a9f0-1473-4357-a65c-a6e1ed1eb048.png)

We solve this missing value problem by replacing the NAN values with the Mean/ Median /Mode
* Mean: It is the average value
* Median: It is the midpoint value.
* Mode: Highest reapeted value or  It is the most common value.

# One hot encoding vs label encoding in Machine Learning
One-hot encoding
One-hot encoding converts the categorical data into binary code as 0 and 1 by splitting the column into multiple columns. 

Label encoding
Label Encoding is converting labels/words into numeric form

Using one-hot encoding increases the dimensionality of the data set. Label encoding doesn’t affect the dimensionality of the data set. One-hot encoding creates a new variable for each level in the variable whereas, in Label encoding, the levels of a variable get encoded as 1 and 0.
![image](https://user-images.githubusercontent.com/108605935/207283418-1b2cde66-0e97-40b4-b1f3-2569ae9e6792.png)

#  People think that one-hot encoding and dummy-encoding are exactly the same thing, but that's not entirely true.
![image](https://user-images.githubusercontent.com/108605935/207284030-20100424-0c4b-493e-8f9e-c8889888cdac.png)

Often times people think that one-hot encoding and dummy-encoding are exactly the same thing, but that's not entirely true. If you use pandas pd.get_dummies() for dummy-encoding, the default value of the option drop_first is set to False, which basically results in one-hot encoding. But if you set drop_first = True, there are less generated columns, as one can see in the image.


## Categorical values
* Nominal Categories
Nominal categories are unordered e.g. colours, sex, nationality.
Ordinal Categories
* Ordinal categories are ordered, e.g. school grades, price ranges, salary bands.
source: https://benalexkeen.com/mapping-categorical-data-in-pandas/ 

# When to not use One-Hot and Dummy Encoding
One hot encoder and dummy encoder are two powerful and effective encoding schemes. They are also very popular among the data scientists, But may not be as effective when-

A large number of levels are present in data. If there are multiple categories in a feature variable in such a case we need a similar number of dummy variables to encode the data. For example, a column with 30 different values will require 30 new variables for coding.
If we have multiple categorical features in the dataset similar situation will occur and again we will end to have several binary features each representing the categorical feature and their multiple categories e.g a dataset having 10 or more categorical columns.
In both the above cases, these two encoding schemes introduce sparsity in the dataset i.e several columns having 0s and a few of them having 1s. In other words, it creates multiple dummy features in the dataset without adding much information.

Also, they might lead to a Dummy variable trap. It is a phenomenon where features are highly correlated. That means using the other variables, we can easily predict the value of a variable.
Due to the massive increase in the dataset, coding slows down the learning of the model


One-Hot Encoding

![image](https://user-images.githubusercontent.com/108605935/207285705-6dc366de-8203-4282-9219-cccc0225ba69.png)

#Fit and transform Data
data_encoded = encoder.fit_transform(data)
data_encoded

![image](https://user-images.githubusercontent.com/108605935/207285978-c7f8c0bf-311e-441e-9e9b-cd439daad31d.png)


Dummy Encoding

![image](https://user-images.githubusercontent.com/108605935/207286459-c9db1235-886d-422d-a1f3-124e04810658.png)

#encode the data
data_encoded=pd.get_dummies(data=data,drop_first=True)
data_encoded

![image](https://user-images.githubusercontent.com/108605935/207286659-e1a07f7a-deba-4b65-964d-2721f2aa4347.png)



