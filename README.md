# Purpose
Predict the salary of a company's employee.
## Creator
- [jpedrou](https://github.com/jpedrou)
## Tools 
<img width="48" height="48" src="https://img.icons8.com/color/48/python--v1.png" alt="python--v1"/>  <img width="48" height="48" src="https://img.icons8.com/fluency/48/jupyter.png" alt="jupyter"/>
# About Dataset
This dataset contains information about the salaries of employees at a company. Each row represents a different employee, and the columns include information such as age, gender, education level, job title, years of experience, and salary.

Columns:

- `Age`: This column represents the age of each employee in years. The values in this column are numeric.

- `Gender`: This column contains the gender of each employee, which can be either male or female. The values in this column are categorical.

- `Education Level`: This column contains the educational level of each employee, which can be high school, bachelor's degree, master's degree, or PhD. The values in this column are categorical.

- `Job Title`: This column contains the job title of each employee. The job titles can vary depending on the company and may include positions such as manager, analyst, engineer, or administrator. The values in this column are categorical.

- `Years of Experience`: This column represents the number of years of work experience of each employee. The values in this column are numeric.

- `Salary`: This column represents the annual salary of each employee in US dollars. The values in this column are numeric and can vary depending on factors such as job title, years of experience, and education level.
# Model Selection
As this dataset is very small and simple, I chose just 3 models for this experiment, without features selection, just with padronization to the models perfom better:
- Linear Regression
- Polynomial Regression
- DecisionTreeRegressor
## Linear Regression
After doing the Exploratory data analysis (EDA), I could observe that some columns followed a linear correlation between the target **(Salary)** as `Age` and `Years Of Experience` columns. Because of that, I chose, as the first model, Linear regression.

**Age x Salary**

![Age](https://github.com/jpedrou/SalaryPredictionML/assets/127536464/8c89a9fd-2c6f-4df4-990d-65907c3465a2)

**Years Of Experience x Salary**

![Years](https://github.com/jpedrou/SalaryPredictionML/assets/127536464/c1fe46ca-87fc-45ab-9075-003aa512d296)

## Polynomial Regression
As the second option, I tried to improve the results using the polynomial version of Linear Regression, as an attempt to agroup better the features. But, at the end, the final metrics were very similar with the first experiment.

## DecisionTreeRegressor
As the last model, I chose the DecisionTree, because its work with a better features specification, given that it generates, as the name suggests, an unique tree that place in the top the most important variable of the data and making other branches from it. But, I got a very similar result with the other models that were chosen.

# Conclusion
The best model will depend of the  evaluation metric used, if it's **MAE** the best one will be DecisionTree Regressor, but if it's **R2** the best one will be Linear Regression.

**OBS: To really check which of these models are actually the best one is necessary use cross validation techniques and extract the mean of scores, make tests of normality and, posteriorly, Hypothesis Test. I will not follow this adictional steps, because in this situation the database is very simple, being for learning purposes only.**
