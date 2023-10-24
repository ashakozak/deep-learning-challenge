# Alphabet Soup Charity Funding Prediction Challenge

Repository for the Monash University Bootcamp Module 21.

## File Structure

- `Starter_Code.ipynb`: The initial Jupyter Notebook containing the basic model without optimizations.
- `AlphabetSoupCharity_Optimisation.ipynb`: The Jupyter Notebook where model optimization was performed.
- `AlphabetSoupCharity`: Original Model file.
- `AlphabetSoupCharity_Optimisation`: Optimized model file.
- `README.md`: The document you're currently reading, which offers a full report of the project with an overview and its results. It also lists the included files.

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

![Original_model](https://github.com/ashakozak/deep-learning-challenge/assets/134185577/e92e8101-ec3b-4fbc-9d44-307561a5fdc7)

  - **Optimized Model**: 3 layers with neuron configurations of 100, 50, and 30, all utilizing the 'relu' activation function. The model retained the original number of epochs. The intent was to capture more intricate patterns in the data.

  ![Optimized_model](https://github.com/ashakozak/deep-learning-challenge/assets/134185577/e6a9c246-6156-4bfa-b3c4-4dd18dd07a16)

- **Were you able to achieve the target model performance?**
  - The original model had an accuracy of 72.89%. After optimization, the model's accuracy increased to approximately 73.3%, which is an improvement, albeit slight, and remains slightly under the target accuracy of 75%.

- **What steps did you take to enhance model performance?**
  - **Data Preprocessing**: Dropped the 'STATUS' column and binned the 'ORGANIZATION' column.
  - **Neural Network Adjustments**: Incorporated more neurons, layers, and altered activation functions. Reduced epochs to curtail overfitting.

### Summary

The deep learning model, at its peak accuracy of 73.3%, provides a notable predictive capability for the Alphabet Soup dataset, however marginally below the 75% target. Key enhancements originated from data preprocessing.

**Recommendation**: While the neural network model is decent, ensemble machine learning models like Random Forest or Gradient Boosted Trees might offer improved performance. These models can handle a mix of numerical and categorical data well and might offer a better balance between performance and complexity.
