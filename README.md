# Pratice-Titanic-Machine-Learning-from-Disaster

<h2>Overview</h2>
The data has been split into two groups:

training set (train.csv)
test set (test.csv)
The training set should be used to build your machine learning models. For the training set, we provide the outcome (also known as the “ground truth”) for each passenger. Your model will be based on “features” like passengers’ gender and class. You can also use feature engineering to create new features.

The test set should be used to see how well your model performs on unseen data. For the test set, we do not provide the ground truth for each passenger. It is your job to predict these outcomes. For each passenger in the test set, use the model you trained to predict whether or not they survived the sinking of the Titanic.

We also include gender_submission.csv, a set of predictions that assume all and only female passengers survive, as an example of what a submission file should look like.


<h2>Variable Notes</h2>
pclass: A proxy for socio-economic status (SES)
1st = Upper
2nd = Middle
3rd = Lower

age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

sibsp: The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

parch: The dataset defines family relations in this way...
Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children travelled only with a nanny, therefore parch=0 for them.






<h2>How did I work on it</h2>

It all starts with to knowing the dataset properly.We have know know the important features in the dataset and also the features which are not important or which will effects on the prediction ability of the model so remove these features.the process of doing this is called <b>Exploratory data analysis</b>

Lets start doing it.
To know the data basic statistical details like percentile, mean, std etc. we use <b>describe()</b>
![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/11.png)

<b>Number of people survived</b> 

As we know that the people on the ship either survived or dead so its a binary classification problem because the end result is either 1 or 0.Lets find out how many survived and how many didn't.

![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/12.png)

We can see that there are less people survived.Graphical way is the best way to visualize the data. 

Now we have see that overview of the data.Now lets find out the important features of the data.


<b>Pvalue effects on the peoples survival:</b>


![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/13.png)

In this way of representing the data we have see that the people with Pclass=1 have survived then the other Pclasses.This tells you that the people who where rich survived.So Pclass is the one of the important feature that can help in predicting the survivability of a person.


<b>Gender effects on the peoples survival:</b>

![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/14.png)

We can see that there are female passengers survived rather then male passengers.So this adds one more feature as important one because let say a passenger who is female and let say other passenge who is a male and let say only one person can sit in the Lifeboat then observing the above graph says that the passenger who is a female have more chance of survivle.

<b>Embarked effects on the peoples survival:</b>

![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/15.png)

Embarked='S' has higher Survival ad death rate.But there is one more observation is that there are many null values in Enbarked='C' and 'Q' because ther are very less number of passengers shown in the graph.This is also an important feature but need some preprocessing


<b>Preprocessing:</b>

1. Find weather the null values or present in Emberked.
2. Drop the unwanted column.
3. Emberked has categories like 'S' , 'C' , 'Q' convert them to 0 , 1 , 2.
4. Gender has categories like 'male','female' convert them to 0,1.
5. Drop all the rows with null values.

After carring all this changes we get.

![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/16.png)

Now we can carry out all needed changes in the data now we can apply the machine learning models on top of it which can work on classification.We get

![GitHub Logo](https://github.com/saneet09/Pratice-Titanic-Machine-Learning-from-Disaster/blob/master/17.png)

We can see that Decision Tree and Random Forest work well























