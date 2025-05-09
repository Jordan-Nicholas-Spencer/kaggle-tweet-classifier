# Predicting Natural Disaster Tweets Using Binary Classification
This is a group project for a machine learning class at San Diego State.
We are basing our project on the Kaggle competition [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/overview)

These notebooks may be run on [jupyterhub.sdsu.edu](https://jupyterhub.sdsu.edu) with the PyTorch notebook and 1 GPU.

## Install Additional Packages
Assuming that you are running this from the PyTorch notebook:

From the root of the repo, run `pip install -r requirements.txt`

## Getting the Data
Follow these steps to get the data (assumes running linux, macOS or Windows Subsytem for linux):

1. Log into or create your Kaggle account
2. Accept the competition at the link above
3. Install kaggle CLI:
    ```bash
    pip install kaggle
    ```
4. Sign in and download your kaggle.json from [settings](https://www.kaggle.com/settings) > API > Create new token
5. Configure kaggle CLI with kaggle.json:
    ```bash
    mkdir -p ~/.kaggle
    mv ~/Downloads/kaggle.json ~/.kaggle/kaggle.json
    chmod 600 ~/.kaggle/kaggle.json
    ```
6. Run the [get_data.sh](./getting-started/get_data.sh) script or use the [data_exploration](./getting-started/data_exploration.ipynb) notebook

## Running the Models
All of our individual models are available in the base-models directory.
These models are logically named after the type of machine learning model that they defined, trained and evaluated.
These models should be run before the ensemble models.

### Final Model
Our best and final model, which we submitted to Kaggle for the competition, is the [Modular Ensemble](./stacking-models/modular_ensemble.ipynb).

## Evaluation
Each of our models' respective notebook contains evaluation code to check its accuracy, precision, recall and F1 scores.
In addition to this, we generated charts for comparison in the [evaluation](./evaluation/evaluation.ipynb) notebook.

## Prediction
You may load up and run our model against arbitrary text using the [prediction](./prediction/prediction.ipynb) notebook.

## Results
Our best model, the modular ensemble, gained a competition score of 0.83849 placing us at position 70 on the leaderboard. 

