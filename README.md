# Wine quality prediction using Random Forest Classifier

What's done here -
* Import all the required libraries/modules.
* Load and review the dataset from the given 'winequality_red.csv' file.
* Our dataset has 1599 rows and 12 columns.
* Here we don’t have any null value to care about.
* Calculated Mean, Percentile, Standard Deviation of data using describe().
* We used distplot from seaborn on our dataset and got much of a normalized graph.

![img1](/img/rfc1.PNG)

* Plotting data for outlier detection.

![img2](/img/rfc2.PNG)

* Again plotting the data to check the correlation.

![img3](/img/rfc3.PNG)

* Now, we have to do some data preprocessing in order to get good/bad wine quality target column.
* We have used cut() method from pandas and made a new column named 'q2'.
* The column 'q2' depends upon the 'quality' column, it has 0,1 values which determines whether the wine is good{1} or bad{0}.
* Now, Checking the Multicollinearity we found that 'fixed acidity' and 'density' have VIF values of 7.7 and 6.3. But we continued with that.
* Spit the data into training and testing with a test size of 0.30.
* Then fit the trainig data into our Random Forest Classifier model to train.
* The accuracy score is 0.80. Other metrices like precision, recall and f1-score are in good range of 0.78-0.83.
* On Plotting the confusion matrix, we get

![img4](/img/rfc4.PNG)

* Lastly, the roc curve is also upto 0.80 and the graph is as below.

![img5](/img/rfc5.PNG)
