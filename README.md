# F1Score_Metric_DecisionTreeClassification_and PlotDecisionTree
##Classification on Emails. Since F1Score metric is not readily available in Sklearn package, this method in the code specially allows one to do category by category F1 score.

This project is a project i did in my previous company pertaining to ML on email data, using NLP. Since the data from my company is highly confidential,
I used partial data from "ENRON Email" dataset. Their data set is huge, so I took part of it for training and another part of it for prediction.

One of the special features in a email is sometimes we see "From:" , "To:", etc. All these are repeated and may affect the frequency of these words
appearing in a email data, hence we remove them. I saw the pattern in the email data and created a list words where in the email thread if the
**line** starts with these, we remove:
[starts with these words each line](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/startsWith.csv). 

Take note that the keyword is "Starts with" not "contains" these words.

Typically, if we use the **sklearn.metrics.accuracy_score**, there wont be a column of **F1-score** in the metrics, the **F1-score** is an aggregated
value only. In my project, I have made a column class wise **F1-score** appended to the metrics we usually see in sklearn package:  

![F1-score Metrics](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/F1_score_metric.PNG)   

You can see the csv file here:
![F1-score metrics csv](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/output/f1_Score_ROC_decisionTree.csv).
Codes can be found in this file: [this file](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/F1Score_DecisionTreeClassification_onEmails.ipynb)  


Next, we also made a max_depth= 7 decision tree on the training set and visualised it in .png format in order of top number of words appearing.
![top words appearing in emails(selected emails)](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/DecisionTreeEmailTopWords.png)  

Codes can be found in this file: [this file](https://github.com/cjy93/F1Score_Metric_DecisionTreeClassification/blob/master/plot_decisionTree_TopWords.ipynb)
