# Telecom

**Introduction**
The operator of communication "Niedinogorazryva.com" wants to learn how to predict the outflow of customers. If it turns out that the user plans to leave, he will be offered promo codes and special conditions.

**Target**
To prepare a prototype of a machine learning model that will predict customer churn. Target metric ***AUC-ROC >= 0.85***

**Description of services**

The operator provides two main types of services: 

1. Landline telephone service. It is possible to connect the telephone to several lines at the same time.
2. Internet. The connection can be of two types: via a telephone line (DSL*,* from the English * digital subscriber line*, "digital subscriber line") or fiber optic cable (*Fiber optic*).  

The following services are also available:

- Internet security: antivirus (*DeviceProtection*) and blocking unsafe sites (*OnlineSecurity*);
- Dedicated technical support line (*TechSupport*);
- Cloud file storage for data backup (*OnlineBackup*);
- Streaming TV (*StreamingTV*) and movie catalog (*StreamingMovies*).

Customers can pay for services every month or sign a contract for 1-2 years. Various payment methods and the possibility of receiving an electronic receipt are available.

# Results of the research

According to the terms of reference from the telecom operator "Niedinogorazryva.<url>" we have prepared a machine learning model, which, according to the provided lists, should predict whether the client will stop using communication services or not.

The work consists of the following key stages:

* Primary study of information*. According to the results of the data upload, it was noted that 4 datasets provided by the customer differ in sample sizes. This information had to be taken into account during the subsequent consolidation of datasets.


* *Data preprocessing*. During preprocessing, the absence of explicit duplicates was verified. After combining the datasets, technical gaps were formed, which were filled with values with "plugs" depending on specific conditions. Also, all the necessary data were brought to the correct type.


* *Data analysis*. During the study of the data, the fact of unbalance of the sample by target was reflected (this factor was further taken into account in the preparation of machine learning models). The main trends in the care of current customers and the dynamics of the emergence of new customers are investigated. The target prize was also defined as `finish_date`, which is derived from the original feature `EndDate`. 


* *Preparation of machine learning models and quality control*. RandomForestClassifier and LGBMClassifier were taken as machine learning models for consideration. According to the results of model training and parameter selection, the LGBMClassifier model proved to be the most successful (AUC-ROC reached 0.91 in the training sample).


**Detailing  machine learning model**

The size of the original dataset df = (7032, 19)

The size of the training sample features_train_L = (5274, 18)

Test sample size features_test_L = (1758, 18)

*Target attribute* = `finish_date'. This is a derived attribute from the original `EndDate'.

**Signs for prediction* = `gender`, `Senior Citizen', `Partner', `Dependents', `Type`,
       ``Paperless Billing`, `Payment Method`, `Monthly Charges`, `Total Charges`,
       ``Multiple Lines`, `Internet Service`, `Online Security`, `Online Backup`,
       ``Device Protection`, `TechSupport`, `Streaming TV`, `StreamingMovies`,
       `finish_using`, `duration`.  (`duration` is a derived attribute.)

Parameter parameter random_state = 130223

**Final model**

```python
model_LGBMClassifier = LGBMClassifier(boosting_type = 'gb dt', class_weight = 'balanced',
                                      n_estimators = 50 ,random_state = 130223)
```

**ROC-AUC metric on the test sample**
0.9
