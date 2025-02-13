Overview of the Analysis

The purpose of this analysis is to develop a binary classifier that can predict whether applicants for funding from Alphabet Soup will be successful in their ventures. Using a dataset containing metadata on over 34,000 organizations, we applied deep learning techniques to train a model capable of making these predictions with a high degree of accuracy.

Results

Data Preprocessing

Target Variable:

The target variable for the model is the IS_SUCCESSFUL column, which indicates whether an applicant’s funded venture was successful.

Feature Variables:

The feature variables include all columns that provide meaningful data about the applicants and their ventures, such as:

APPLICATION_TYPE

AFFILIATION

CLASSIFICATION

USE_CASE

ORGANIZATION

STATUS

INCOME_AMT

SPECIAL_CONSIDERATIONS

ASK_AMT

Removed Variables:

Certain columns were removed from the dataset because they were not relevant for prediction or contained redundant data, such as:

EIN (Employer Identification Number, which is unique to each organization but not predictive)

NAME (Organization name, which does not contribute to classification)

Compiling, Training, and Evaluating the Model

Neural Network Architecture:

Number of Layers: 3

Number of Neurons:

Input Layer: 80 neurons

Hidden Layer 1: 30 neurons (ReLU activation)

Hidden Layer 2: 15 neurons (ReLU activation)

Output Layer: 1 neuron (Sigmoid activation for binary classification)

Model Performance:

The initial model achieved an accuracy of approximately 72%.

The target performance was 75% or higher, which was not met initially.

Steps Taken to Improve Performance:

Tuning Hyperparameters: Adjusted the number of neurons and layers to optimize the model’s learning capabilities.

Feature Engineering: Removed irrelevant or low-impact features to enhance model efficiency.

Data Normalization: Applied normalization techniques to improve convergence.

Epoch Adjustments: Increased the number of epochs to allow the model more training time.

Alternative Activation Functions: Tested different activation functions, such as Leaky ReLU and Tanh, to assess their impact on accuracy.

Summary

The deep learning model successfully classified funding applicants but did not reach the target performance of 75% accuracy. Despite tuning efforts, the model plateaued at around 72% accuracy.

Recommendation

A different machine learning model, such as a Random Forest Classifier or XGBoost, could potentially improve classification performance. These models are often more interpretable, require less tuning, and perform well on structured tabular data. Implementing ensemble techniques, such as stacking models, could also enhance predictive power. Further exploration of feature selection and engineering could refine the dataset to improve overall performance.