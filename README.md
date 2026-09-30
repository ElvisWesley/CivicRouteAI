# CivicRouteAI assessment
## Project Overview
The assessment project builds a small tensorflow/keras classification model that predicts
the category of a service request such as pothole or water leak.
## Problem description
Residents send request about a problem such as a pothole, broken streetlamp, water leak or similar issues.
The requests include information such as location, channel, description etc.
This request is then manually inspected, categorized and then routed to the correct department that will handle the issue.
This is a time-consuming and costly process. To help speed up this process, 
an AI system can be used as a support decision tool to categorize the request, making it easier to route to the correct department.
## Dataset Description
The dataset can be found in "civic_requests_prepared.csv" with a dictionary explaining them in "CivicRoute_AI_Data_Dictionary.pdf".
It consists of 600 synthetic records, balanced between the 4 classes, resulting in 150 records each. 
These records include information about a service request such as neighbourhood, channel, urgency level or report_repeat_count.
## Tools and libraries
- Python
- Pandas / NumPy
- Scikit-learn (train/test split, confusion matrix)
- TensorFlow / Keras
- Matplotlib / Seaborn
## Installation instructions
1. Clone this repository.
2. Install the required libraries:
- pip install pandas numpy scikit-learn tensorflow matplotlib seaborn
## How to run the model
1. Open civicroute_structured_tensorflow_starter.ipynb in Jupyter or PyCharm.
2. Run the cells in order:
- Step 2 loads and inspects the data, handles missing values, encodes categorical fields, and engineers an old_asset_flag feature.
- Step 3 splits the data into train/validation/test sets, defines and trains a Dense Sequential model with two hidden layers , and evaluates it on the test set.
3. Inspect the test accuracy and confusion matrix for the results
## Results
The model reached an accuracy of 62.5% on the test set and the confusion matrix showed a reliable prediction for the "illegal dumping" category with 26/30 correct predictions,
whereas the "pothole" category performed the worst with only 12/30 correct predictions.
## Future improvements
For future improvements I would suggest collecting more training data to give the model more examples to learn from. I would also tune the model and train it for longer because it did not converge.
I would also use scaling to put the different features on the same scale to give them the same importance.
Another important improvement is to improve explainability with tools such as shap to explain the models predictions and what drove them.
Graph neural network could also be explored in the future to learn relationships between the features.
