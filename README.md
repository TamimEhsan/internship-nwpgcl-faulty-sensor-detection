## Task 1

Flow meters are devices used to measure the volumetric or mass flow  of a fluid with ultrasound. However, these devices present serious  engineering problems that give rise to a defective meter function and  cause errors in reading the flow velocity.

In this study, we analyze a database with the characteristics of a  liquid ultrasonic flowmeter and its state (healthy or unhealthy) to know the relevant factors that cause failures in the system.

Therefore, a solution that balances accurate measurement and the necessary costs of recalibration is needed.

 

**Resources:** Dataset ([Download Excel data](https://buetedu-my.sharepoint.com/:x:/g/personal/esrdlab_cse_buet_ac_bd/ESujzf0RsblJrLs1NFF_EroB-T181j12DlbHLLCMEt94XA?e=ozORng))

**N.B.** This problem is the foundation of this  internship program and you will get three weeks to learn the required  technology and tools. The mentor will help you to complete the tasks of  this problem.



### Solution

The data set is divided into training and testing by 0.6:0.4 ratio

```python
X_training, X_testing, y_training, y_testing = train_test_split(
    X_main, y_main, test_size=0.4,random_state=42
)
```

Multiple models were tested. Among them XGBoost performer best. which is a regularizing gradient boosting framework. Confusion matrix and accuracy of the models are added.

| Model            |   Support Vector Machine   |       Logistics Regression       |            XGBoost             |
| ---------------- | :------------------------: | :------------------------------: | :----------------------------: |
| Confusion Matrix | ![](Task 1\assets\svm.jpg) | ![](Task 1\assets\logistics.jpg) | ![](Task 1\assets\xgboost.jpg) |
| Accuracy         |            0.54            |               0.57               |              0.8               |

