# Predicting Natural Disaster Tweets Using Binary Classification
This is a group project for a machine learning class at San Diego State.
We are basing our project on the Kaggle competition [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/overview)

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
6. Run the [get-data.sh](./get-data.sh) script or use the [DataExploration](./DataExploration.ipynb) notebook
