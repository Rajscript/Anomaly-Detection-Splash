__Anomaly detection__

This is based on the kaggle competition "[Anomaly Detection](https://www.kaggle.com/competitions/anomaly-detection/overview)"


__Overview__

Let us assume that, we have a company called "Splash", and you are a newly joined Machine Learning Engineer at our company, held at 30 LPA CTC. So, the below thing describes our company and the task in hand.

Currently we at Splash, help retailers with pricing intelligence and business monitoring.

One of our main challenges comprise of monitoring and analyzing our client's business metrics in real time for instant detection of the incidents that may impact their revenue.

One subpart of this challenge is Anomaly Detection which generates alerts on our client's business metrics.

The Problem Statement presented below highlights the problem which we are tackling right now

__Data Description__

The description of the column are as follows:

timestamp [ float ] : is provided as a Unix epoch in seconds.

value [ int ] : is a real value measurement of some metric at the timestamp.

is_anomaly [ boolean ] : is a boolean value which is True if the corresponding value is identified as an anomaly.

predicted [ float ] : is a real value prediction coming from a black box forecasting model for that timestamp. This black box forecasting model is assumed to be aware of only the true data distribution.

Since the company is concerned about the anomaly data more than non-anomaly data, we have to be careful in making the predictions for the anomaly cases. Here we have used different ML models to compare their performances in determining the anomaly cases.


__Methods__

We have two notebooks applying two different way of solving this problem. One of the major problem in anomaly detection dataset is the data imbalance due to having considerably lesser amount of anomaly cases compared to regular ones. 

One approach to handle such class imbalance is to populate the minority class with randomly duplicated data using <span style= 'color: blue;'>**Random Sampling** </span> or generating synthetic data using <span style= 'color: blue;'>**SMOTE**</span>. This approach and its corresponding scoring metrics can be found in the [Anomaly_detection notebook](/Anomaly_detection.ipynb)

The other approach is applying the in-built class imbalances handling tool in ensemble models like <span style= 'color: blue;'>**XGBoosting** </span> and <span style= 'color: blue;'>**CatBoost** </span>. This approach and their corresponding findings can be found in the [catboost notebook](Anomaly-Detection-Splash/XgboostVsCatboost.ipynb)