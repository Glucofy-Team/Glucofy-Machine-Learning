# <img src="https://github.com/Glucofy-Team/.github/blob/main/profile/img/logo.png" width="50"> Glucofy-ML

## Overview
The Machine Learning part of this application are glycemic index and glycemic load prediction. We create a model for predict glycemic index and glycemic load from specific food nutritions. User could put the nutritions such as calories, proteins, carbohydrats and fats and the glycemic index and glycemic load will be processed in the model.

## Datasets
The dataset used in this project was obtained through web scraping from the following website: [Glycemic Index Guide](https://glycemic-index.net/). The dataset includes detailed nutritional information such as category, name, glycemic index, glycemic load, calories, proteins (g), carbohydrates (g), and fats (g).

For more details and access to the dataset used in training the machine learning models, please visit the following link: [Nutrition Food Dataset](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/blob/main/data/nutrition%20food%20dataset%20-%20modified.csv).

Feel free to explore the dataset and utilize it for your own analyses or experiments.

## Model Architecture

We evaluated several machine learning models to predict glycemic index and glycemic load, including linear regression, decision tree, support vector regression (SVR), and FFNN. Through our experimentation, we found that the FFNN model outperformed the others, achieving the lowest MAE (Mean Absolute Error). Here is a breakdown of FFNN model architecture:

- **Input Layer**: The model starts with an input layer shaped to accommodate the number of numeric features in the dataset.

- **Hidden Layers**:

    - Two dense layers with 32 units each and ReLU activation functions.
    - One dense layer with 64 units and a ReLU activation function.
    - One dense layer with 128 units and a ReLU activation function.
    - Dropout Layer: A dropout layer with a dropout rate of 0.2 is included to prevent overfitting during training.

- **Output Layer**: The model concludes with a dense layer that outputs a single value (the predicted glycemic index) using a ReLU activation function.

This architecture is chosen based on its performance in minimizing Mean Absolute Error (MAE) during model selection, demonstrating its effectiveness in predicting glycemic index from the provided dataset.

![choose best model](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/assets/51023310/b5a402b1-22ac-4bf3-8ecb-4a5b7b224fe3)
*example of best model for glycemic index predcition*

![image](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/assets/51023310/ee64296c-0021-4cdd-bb15-33fee7ea9c55)
*example of best model for glycemic load predcition*


Upon evaluation, the model achieved promising results in predicting glycemic index, providing valuable insights into the nutritional characteristics of the foods analyzed.
![image](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/assets/51023310/733afc78-4afc-4bba-b3b9-b8ae756ead31)
*example of glycemic index prediction*

![image](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/assets/51023310/a29272a7-7436-4a15-8423-35244aa4c2b0)
*example of glycemic load prediction*


## How to use our projects

- Clone this repository or you can [download the dataset](https://github.com/Glucofy-Team/Glucofy-Machine-Learning/blob/main/data/nutrition%20food%20dataset%20-%20modified.csv)
- Install the required libraries
- Pre-process the data
- Build and compile the model with the architectures as mentioned above
- Convert the model to .h5 format
