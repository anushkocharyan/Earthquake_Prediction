# Earthquake_Prediction
Predict time left until an earthquake strikes. Technologies used: Python, MongoDB, SparkSQL and SparkML


LANL Earthquake Prediction
(group project by  Anush Kocharyan, Jyoti Prakash Maheswari, Wenkun Xiao and  Viviana Marquez) 

For this project, we used data provided by Los Alamos National Laboratory for a [Kaggle competition](https://www.kaggle.com/c/LANL-Earthquake-Prediction) to predict time
remaining before laboratory earthquakes occur from real-time seismic data.

We stored the data on a S3 bucket, used an AWS EC2 instance to conduct feature engineering and transferred
the dataset to a sharded and distributed MongoDB database (2 shards and 3 nodes per shard). Afterwards, we used AWS EMR clusters
of various configurations to build Spark ML models. 


In our experiment, we found that Random Forest was the best performing algorithm. For that reason,
we decided to run cross validation to further improve our results. Our lowest RMSE score is 1.40, which is a
significant improvement from our previous score of 2.20 for Random Forest with default parameters.


Please check out the full report [here](https://github.com/anushkocharyan/Earthquake_Prediction/blob/master/Project_Report.pdf): 










