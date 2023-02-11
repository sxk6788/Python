# Python
# Project Title: Credit Card Customer Churn Prediction #
Introduction#
Now-a-days it is observed that many customers apply for credit card service and 
cancel it just after earning initial benefits like welcome bonus. This process of 
opening and closing service is termed as credit card churning. Reduction of credit 
card users in a company is a major red flag. Bank managers are concerned about 
the loss. They would like to use the available data with the bank to identify what 
factors are affecting customers to cancel the service and how it can be reduced. 
Identifying factors that previously caused customers to churn could help the bank 
in taking steps so that customers do not abandon. These factors can be identified 
using different visualization techniques and predictive analysis can be performed 
to identify if the customer is going to churn or not.
Motivation
Having work experience in the financial industry, I always wondered how huge 
amount of data available can be used to resolve business issues. Also. I want to 
explore different packages available and get a technical understanding of python. 
This has motivated me to work on such a kind of dataset where I can enhance my 
knowledge both from technical and business perspective. 
Research questions
What factors are causing customers to switch service? 
What additional benefits can be provided so that customers do not churn?
Description
This project is about predicting the churning possibility of credit card customers 
using the dataset which consists of 10,000 customers mentioning their age, 
salary, marital status, credit card limit, credit card category, etc. The dataset has 
21 columns and 10128 rows. The datasets has 83% of Existing customer, only 
have 16% of customers who have attrite. Thus, we need to try different machine 
learning models to select the best one.
Analysis and methodology:
As part of Data Preprocessing and exploration, I Analyzed each column in the 
datasets to check which information will be useful for prediction. Most of the 
columns are useful in predicting churners, but we need to ignore the last two 
columns as they have less impact.
I initially checked the number of columns and rows in the dataset and their 
datatypes. I checked for the missing and duplicate values. First, I analyzed all the 
columns using matplotlib and seaborn libraries, and created different types of 
graphs like histogram, pie-chart and box-plot to see the distribution, and decide 
which approach to use in converting columns. I checked distribution of graphs by 
taking two variables- input and target variable to visualize data with the target 
variable. Created heatmap to see the relation between variables.
It was observed that variables like Customer age and Gender seem irrelevant to 
decide whether customers will leave the credit card service or not. Variables like 
Total_trans_ct and Total_Trans_Amt have more effect on determining whether a 
customer will churn or not.
Second, I converted the most of the columns with categorical values to numerical 
values using dummy function.
Building a machine learning model suitable for the objective.
In this project, I tried Logistic Regression, Random Forest Classifier and Extreme 
Gradient Boosting Model. I created two DataFrames inside X and Y variables, the 
dataframe in X has no 'attrition' column while the dataframe in Y variable has only 
'attrition' column as this is my target variable. Next, I split into train and test
dataset, training data is 80% while testing data is 20%. Used stratify to
preserve portion of target variable into train and test dataset.
Initially, I tried fitting the train datasets in the machine learning models - Then 
check the metric scores against testing data. I also used SelectFromModel to 
create Feature graph. Feature graph shows factors most useful to least useful 
from the dataset. By using feature selection, have reduced the number of 
features present in the dataset. Then I passed feature to train dataset and defined 
a “model” function. I created three models: Logistic Regression, Random Forest 
Classifier and Extreme Gradient boost using sklearn.model.selection library. Later, 
I build a boxplot to compare the best model visually. 
I also used precision recall curve (area under curve) score to evaluate
performance of the model. The positive class is more important than negative 
class, because misclassifying positive example as negative example result in loss 
of business. Ata the end calculated accuracy score, precision, recall, F1 scores.
