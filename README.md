# Business Analytics Capstone Project

__Project Overview:__ 

Based on records of previous 311 complaints, can we predict how long an incident will take to resolve?

__Context:__ 

In choosing a business problem to solve, my team and I decided to look into the problem of reducing abnormally long 311 call resolution time. Specifically, we attempted to build supervised regression models that can predict 311 call resolution times. 

In theory, the predictions would reflect normal resolution times and if a call, in actuality, exceeds the prediction by a lot, we can conclude that the resolution of the issue in the call should be prioritized since it is outside of normal processing time.

__Link to Reports:__
1. [Data Preparation and Understanding](https://docs.google.com/presentation/d/1cNAAgVxRoOjzag2rKMAHLFmK46ZXGNRW_qmfJ-iy3uk/edit?usp=sharing)
2. [Model Selection](https://docs.google.com/presentation/d/1bqSDOui2vZBtfdjYC2-SaFutK6x_-t_AX1RFgxYnALM/edit?usp=sharing)
3. [Model Findings and Results](https://docs.google.com/presentation/d/12Ww5un8kX3s4O1QaNZfMki8OF6bZz94bsmFw85RYWrc/edit?usp=sharing)

*Note: Some files created during the project are not in this repository due to file misplacement (e.g. the tree-based models I created). However, model performance results are included in the "Model Findings and Results report".*

## Project Breakdown/Summary
### Stage 1: [Data Preparation and Understanding Data](https://docs.google.com/presentation/d/1cNAAgVxRoOjzag2rKMAHLFmK46ZXGNRW_qmfJ-iy3uk/edit?usp=sharing) 

<img src = "images/Dataset Joining - Overview.png" width = 700 height = 400>

Steps performed at this stage:
- Finding Data and Joining Datasets ([2020 311 Cases in San Francisco](https://data.sfgov.org/City-Infrastructure/311-Cases/vw6y-z8j6), Registered Business Locations, City Facilities, and San Francisco Socio-Economic Profiles)
- Feature Selection (removing unneeded columns to reduce dimensionality)
- Extract Resolution Time
- Conduct Basic Data Cleaning (removing duplicates and NA values)
- Feature Engineering and Data Exploration (Done by me using Python in Jupyter Notebook and Excel)

<img src = "images/Data Exploration.png">

### Stage 2: [Model Selection](https://docs.google.com/presentation/d/1bqSDOui2vZBtfdjYC2-SaFutK6x_-t_AX1RFgxYnALM/edit?usp=sharing)

Having learnt various machine learning methods/algorithms, we narrowed down the types of models we will build using the following criteria:
- Uses supervised learning (since we are using historical data)
- Able to perform regression (since we are predicting a quantitative, continuous dependent variable - resolution time)

Due to time constraint, we only built the following types of models: Multiple Linear Regression, RandomForest, and XGBoost.

### Stage 3: [Model Findings and Results](https://docs.google.com/presentation/d/12Ww5un8kX3s4O1QaNZfMki8OF6bZz94bsmFw85RYWrc/edit?usp=sharing)

After building various machine learning models, we compared and evaluated the performance of all three types of models. We decided to use the performance of the Multiple Linear Regression model as the baseline since it is the most basic model.

The models were evaluated with the following the metrics: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-Squared.
Of all models, the XGBoost model I built had the best performance. However, even our best models only explained 25% of the variation in resolution time.

We also concluded that our models were not accurate enough for production, with too large of residuals.
<img src = "images/Residuals per Model.png">


### Takeaway:
<img src = "images/Project Takeaways.png" width = 700 height = 400>


__Personal Reflection:__ 
We should also have accounted the data for a larger range of years for potentially better prediction performance in our models, in addition to researching other features that could have been better predictors. 
