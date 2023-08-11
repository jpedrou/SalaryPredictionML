# Purpose 
Predict the salary of a company's employee. Dataset used to study and practice.
### Tools 
<img width="48" height="48" src="https://img.icons8.com/color/48/python--v1.png" alt="python--v1"/> <img width="48" height="48" src="https://img.icons8.com/fluency/48/jupyter.png" alt="jupyter"/>
### Creator
[@jpedrou](https://github.com/jpedrou)
# About Dataset
The dataset contains information about the salaries of employees at a company. Each row represents a different employee, and the columns include information such as age, gender, education level, job title, years of experience, and salary.

Columns:

- `Age`: This column represents the age of each employee in years. The values in this column are numeric.

- `Gender`: This column contains the gender of each employee, which can be either male or female. The values in this column are categorical.

- `Education Level`: This column contains the educational level of each employee, which can be high school, bachelor's degree, master's degree, or PhD. The values in this column are categorical.

- `Job Title`: This column contains the job title of each employee. The job titles can vary depending on the company and may include positions such as manager, analyst, engineer, or administrator. The values in this column are categorical.

- `Years of Experience`: This column represents the number of years of work experience of each employee. The values in this column are numeric.

- `Salary`: This column represents the annual salary of each employee in US dollars. The values in this column are numeric and can vary depending on factors such as job title, years of experience, and education level.
# Model Selection
As the dataset is very small and was used exclusively for study purposes, I chose 3 different models for the experiences. Because it's a simple problem, is not necessary the use of Neural Networks. Said that, these are the models:
- Linear Regression
- Polynomial Regression
- DecisionTree Regressor

### Linear Regression
This model was chosen first, because after doing the Exploratory Data Analysis (EDA), was observed that some columns had a linear correlation with the target column, as the column `Age` and `Years Of Experience`. These two columns are directly proportional, that is, the greater these variables are, the greater the salaries.


**Age x Salary**

![Captura de tela 2023-08-11 155032](https://github.com/jpedrou/SalaryPredictionML/assets/127536464/da1df11e-534a-4c30-9606-53b78f3d670b)

**Years Of Experience x Salary**

![Captura de tela 2023-08-11 155708](https://github.com/jpedrou/SalaryPredictionML/assets/127536464/115a5389-d440-422f-8b87-76da61ea470a)

### Polynomial Regression
After getting the Linear Regression results, I used the Polynomial version as an attempt to agroup better the attributes, but at the end got similar results of Linear Regression.
### DecisionTree Regressor
This models is awesome, because it can specify better the conditions using as the name suggests a unique decision tree, where it will place at the tree's top the most importance variable. Got a good resut too; very similar to the models above.
# Conclusion
In this case, as the models used had similar results, the best model will depend of the evaluation metric, if it's **MAE** the best one will be DecisionTree Regressor, but if it's **R2** the best one will be Linear Regression.
> ### **Obs**
> **To really check which of these models are actually the best one is necessary use cross validation techniques and extract the mean of scores, make tests of normality and, posteriorly, Hypothesis Test. I will not follow this adictional steps, because in this situation the database is very simple, being for learning purposes only.**
