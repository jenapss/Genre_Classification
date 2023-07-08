# Genre classification
Exercise 14 of the Udacity class on Machine Learning workflows. The objective of this exercise is to bring the lesson's contents together in a complete ML pipeline that produces a trained Random Forest model.

## Dataset
The dataset used in this exercise is a modified version of the original songs dataset: [here](https://www.kaggle.com/mrmorj/dataset-of-songs-in-spotify)

## Model
We use a Random Forest to perform songs' genre classification (NLP).

## Results

The model was evaluated using a test set from the dataset, with an AUC (Area Under the Curve) of 0.95326. The following figures show the feature importance and the confusion matrix computed during the evaluation step: 

 <!-- Images -->

<p float="left">
  <img src="figures/feature_importance_0_f1fd3194294f7a484f72.png" width="300" />
  <img src="figures/confusion_matrix_0_f02dfbea4d35c8b2f32b.png" width="300" />
</p>

## Pipeline

You can use this pipeline at version 1.0.0 with mlflow and w&b (you need to be logged in: `wandb login`):
```
mlflow run -v 1.0.0 git@github.com:AMergy/genre_classification.git
```
for instance:
```
mlflow run https://github.com/AMergy/genre_classification.git \ 
             -v 1.0.0 \
             -P hydra_options="main.project_name=remote_execution"
```
