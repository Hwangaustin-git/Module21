# Module21

##Alphabet Soup Deep Learning Model Report##

Overview of the Analysis : 
- The purpose of this analysis was to develop a deep learning model to predict whether applicants for funding from Alphabet Soup would be successful.
- By training a neural network on historical data, we aimed to identify patterns that could improve funding decisions.

Results :
- Data Preprocessing
-- Target Variable: IS_SUCCESSFUL (1 = successful funding, 0 = unsuccessful).
-- Feature Variables: Included categorical and numerical attributes such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, and ASK_AMT.
-- Removed Variables: EIN and NAME were dropped as they were non-beneficial identifiers.
-- Encoding: Used pd.get_dummies() for categorical data conversion.
-- Splitting: Data was divided into training (80%) and testing (20%) sets.
-- Scaling: Applied StandardScaler() for numerical feature normalization.

Model Compilation, Training, and Evaluation:
- Neural Network Architecture:
-- Input layer based on feature count.
-- Three hidden layers (100, 50, 30 neurons) with ReLU activation.
-- Output layer with a sigmoid activation function for binary classification.

- Performance Metrics:
-- Initial Accuracy: 72.67%
-- Loss: Decreased steadily but failed to reach target accuracy of 75%.

- Optimization Attempts:
-- Increased neuron count in hidden layers.
-- Added an extra hidden layer.
-- Adjusted batch size and number of epochs.
-- Tried different activation functions and optimizers (Adam, RMSprop).
-- Applied dropout regularization to reduce overfitting.

Summary and Recommendations:
- Final Model Accuracy: 72.67%, below the 75% goal.
- Challenges: Model struggled to generalize, possibly due to data imbalance or limitations in neural network architecture.
- Alternative Models:
-- Random Forest or XGBoost could provide better feature importance insights and handle categorical data efficiently.
-- Logistic Regression might work well if the dataset is linearly separable.
- Future Steps: Further feature engineering, tuning hyperparameters, and experimenting with ensemble methods could improve results.


## Conclusion
While deep learning showed promise, a tree-based model like XGBoost may yield higher accuracy with less training time. Exploring alternative algorithms and refining feature selection would enhance prediction performance.
