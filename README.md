# SuperLearnerClassifier_MachineLearning
This is new supervised learning classifier I have developled using the existing classifier. I have stacked the 5 classifier and made the ensemble model which train on 60000 data set of MNIST fashion data set.
Super Learner Classifier
Super Learner Classifier is a ensemble model used in supervised learning of Machine Learning.
I have developed this model using existing classifier present in scikit learn library. 
I have vertically stacked the 5 supervised learning classifier and made a ensemble model. 
This ensemble I trained on MNSIT fashion data set and test on various other data set. 
The accuracy is impressive and using grid search I have found out the best parameters for this classifier. 
As it is a ensemble model which is trained on the prediction output of the base classifiers like Decision Tree, KNN, Naive Bayes, 
Logistic Regression and Random Forest classifiers. I have taken the prediction output of each classifier which are individually 
trained on the Zalando’s Fashion MNIST data set. In order to fit the base model I have used the K fold validation with K values as 5 
for better accuracy. I have ran the fit method and predict method of every classifier 5 times. After getting the prediction output of 
the base classifiers I have stacked them vertically or in other words I have concatenated the all the prediction output together 
and then split that data into training set and testing followed by the labels. 
Now, I have fitted the stack layer classifier aka final classifier in the Super Learner class with those prediction
outputs and used the trained model for predicting the labels as well as calculating the probability of label of the data set.
This is a user based customised model where user can give the parameters as per their requirement. It gives the flexibility 
to choose K values for K fold cross validation(by default it is 5) for base classifiers. Also, user can choose which stack layer
classifier he/she wants to use in their execution. The stack layer has 2 classifier named Decision Tree and Logistic Regression 
which are set as a flag in the condition and call according to the parameter passed. Moreover, it has the functionality to 
train the model either using the predict method output of the base classifier or predict_proba method output of the base classifier 
depends on the parameter passed to it. The Super Learner Classifier contains the fit, predict and predict_proba method which can
be used by making the object of the super learner classifier. Once you train your model you can run it to any dataset available and 
predict the output. It has included the code for the grid search to find the best parameters for this stack layer or final classifiers. 
Besides, it has all the code for getting the performance measures which even visualised by matplots.

To use this code please download the ipython notebook runs on Jupyter and download the dataset, As Dataset has 60000 recordes with 784 columns 
so it takes time to execute so to avoid this I have sampled the data with the sampling rate as 6000 records which basically 600 records for 
each class so it is in data prepreating cell, you can change it according to your ease nut make sure you are having equal amount of data for
every class e.g. 600 for each class(total 10 class ) which is 6000 in total.
Also, need more help read y article on https://medium.com/@prateekshrivastav786/slc-f5aad2e37c8a
Chrees!!!
