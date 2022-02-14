# wine_strategic_pricing
This project on Red wine quality will examine physicochemical inputs to identify empirical (if any) support for a relation between the price of wine and its quality. Price is defined under the connotation of being strategic and not the literal price of a particular wine as it is absent in the dataset. Kaggle is the source of physicochemical and sensory data. Following the results of this study we hope to answer questions regarding strategic price setting possibilities (e.g. Which combinations of materials would yield quality sensory results to a customer). Reasoning for this topic selection stems from a curiosity to whether we owe wine quality to brand reputation.

## Project Outline
1. The wine quality classification problem
2. The benefits of using a machine learning classification model for predicting wine quality
3. The data set
4. Preprocessing the data
5. Building the model
6. Evaluating the model


## Data Exploration
![alt text](https://github.com/DvegaDv01/wine_strategic_pricing/tree/main/artifacts/head.png)
### Stats
![alt text](https://github.com/DvegaDv01/wine_strategic_pricing/tree/main/artifacts/stats.png)
### Normalized Data
![alt text](https://github.com/DvegaDv01/wine_strategic_pricing/tree/main/artifacts/normalized.png)
### Info and Dtypes
![alt text](https://github.com/DvegaDv01/wine_strategic_pricing/tree/main/artifacts/info.png)
### Data preprocessing, feature engineering, spliting and other preparation
To make sure the data is ready for training the model we use a Pytorch api (fastai) to wrap our dataset with a dataloader. Once this is done we utilize transforms to fill missing and normalize the data. With only 12 features in the original dataset there will be no feature enginering. All of the features are continous, minus the dependent variable. Data is randomly seperated into a 80/20 split. The model chosen is classification in nature made up of a simple RNN architecture. There are many limitions to this model approach but the most relevant to mention is the use of a descret model (of formed of hidden layers) for continous variables. This limitation should be mentioned with the benefit that neural networks are natural feature extraction tools via hidden layers.
