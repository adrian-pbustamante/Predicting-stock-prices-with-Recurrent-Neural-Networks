# Predicting-stock-prices-with-Recurrent-Neural-Networks

Adrian P. Bustamante, Ph.D.
adrianpebus@gmail.com

## Objective

We consider prices/volume of IBM stocks in a period of around 1000 days, between January 2020 and April 2024. The objective is to use Recurrent Neural Networks (RNN) to predict the stock prices and volume for 90 days (about 10% of the data). We consider a few simple RNN architectures, including LSTM and GRU. We also use keras tuner to optimize hyperparameters (Dropout, units, optimizer, and learning rate). 

## About the data

Description

International Business Machines Corporation, together with its subsidiaries, provides integrated solutions and services worldwide. The company operates through Software, Consulting, Infrastructure, and Financing segments. The Software segment offers a hybrid cloud and AI platforms that allows clients to realize their digital and AI transformations across the applications, data, and environments in which they operate. The Consulting segment focuses on skills integration for strategy, experience, technology, and operations by domain and industry. The Infrastructure segment provides on-premises and cloud based server, and storage solutions, as well as life-cycle services for hybrid cloud infrastructure deployment. The Financing segment offers client and commercial financing, facilitates IBM clients' acquisition of hardware, software, and services. The company has a strategic partnership to various companies including hyperscalers, service providers, global system integrators, and software and hardware vendors that includes Adobe, Amazon Web services, Microsoft, Oracle, Salesforce, Samsung Electronics and SAP, and others. The company was formerly known as Computing-Tabulating-Recording Co. International Business Machines Corporation was incorporated in 1911 and is headquartered in Armonk, New York.

This dataset contains historical stock price data for International Business Machines Corporation (IBM) from [Jan/01/2020] to [May/01/2024]. The dataset includes daily closing prices, adjusted closing prices, and other relevant information. Features:

Date, Open, High, Low, Close, Adj Close, Volume.

Source: https://www.kaggle.com/datasets/innocentmfa/ibm-stock-prices-dataset

## Conclusion

We considered a dataset containing stock Prices and Volumes for about 1000 days. We tuned hyperparameters (number of units, dropout rate, optimizer, learning_rate) and train some RNN models to predict the stock price/volume for the last 90 days of the dataset. After RandomSearch hyperparameter tuning, and using MSE as error metric, we found the Deep_LSTM (with two hidden layers) and the GRU models as the ones with the lowest error metric.

The models considered were very simple and there could be many ways in which they can be improved. For example, using different scaling techniques, consider a custom metric for data series, consider data from other companies with the same characteristics, explore different model architectures, perform a thorough hyperparameter search. In general, predicting stock prices is not an easy task.
