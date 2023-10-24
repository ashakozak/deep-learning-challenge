# Alphabet Soup Charity Funding Prediction Challenge

Repository for the Monash University Bootcamp Module 21.

## File Structure

- **Starter_Code.ipynb**: The initial Jupyter Notebook containing the basic model without optimizations.
- **AlphabetSoupCharity_Optimisation.ipynb**: The Jupyter Notebook where model optimization was performed.
- **nn_model**: Model file.
- **nn_2_model**: Optimized model file.
- **README.md**: The document you're currently reading, which offers a full report of the project with an overview and its results. It also lists the included files.

## Project Overview

The project focuses on building a deep learning model to predict the success of charity funding applications based on various features related to the organizations. Using the `charity_data.csv` dataset, which contains historical data on funding applications, the project's primary goal is to optimize a neural network to classify the success of these applications.

### Data Preprocessing

- **What variable(s) are the target(s) for your model?**
  - `IS_SUCCESSFUL`: Indicates if the funds were used effectively by the organization. A value of `0` means the funds were not used effectively, while a value of `1` signifies successful use of the funds.

- **What variable(s) are the features for your model?**
  - `APPLICATION_TYPE`: Type of application.
  - `AFFILIATION`: Affiliated sector of the industry.
  - `CLASSIFICATION`: Government organization classification.
  - `USE_CASE`: Intended use of the funds.
  - `ORGANIZATION`: Type of organization.
  - `INCOME_AMT`: Organization's income classification.
  - `SPECIAL_CONSIDERATIONS`: Any special considerations for the application.
  - `ASK_AMT`: Funding amount requested.

- **What variable(s) should be removed from the input data?**
  - `EIN`: Unique identifier.
  - `NAME`: Name of the organization.
  - `STATUS`: Active status of the organization.

### Compiling, Training, and Evaluating the Model

- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
  - **Initial Model**: 2 layers (80 and 30 neurons) with 'relu' activation. This setup served as a baseline.
  - **Optimized Model**: 3 layers with varied neurons and 'LeakyReLU' activation. The intent was to capture more intricate patterns in the data.

- **Were you able to achieve the target model performance?**
  - The model attained an accuracy close to 73.3%, just shy of the desired 75%.

- **What steps did you take to enhance model performance?**
  - **Data Preprocessing**: Dropped the 'STATUS' column and binned the 'ORGANIZATION' column.
  - **Neural Network Adjustments**: Incorporated more neurons, layers, and altered activation functions. Reduced epochs to curtail overfitting.

### Summary

The deep learning model, at its peak accuracy of 73.3%, provides a commendable predictive capability for the Alphabet Soup dataset, albeit marginally below the 75% target. Key enhancements originated from adept data preprocessing.

**Recommendation**: Consider exploring ensemble machine learning models like Random Forest or Gradient Boosted Trees. These models might present a superior performance balance, effectively handling both numerical and categorical data.
