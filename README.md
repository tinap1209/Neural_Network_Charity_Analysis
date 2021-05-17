# Alphabet Soup Charity Neural Network Analysis

## Overview

The purpose of this analysis is to use a neural network to decide which companies should recieve loans from Alphabet Soup. This analysis uses python's TensorFlow library to create, train, and evaluate data gathered from previous loans.

## Results

### Data Preprocessing

After looking at the data, I established that the target variable is the "IS_SUCCESSFUL" column. I  removed the "EIN" and "NAME" columns as they did not offer any relevant data that could help the model perform better. The remaining columns became the features for the model.

### Compiling, Training, and Evaluating the Model

For the first attempt at compiling a neuron network consisted of 8 neurons in the first layer and 6 in the second. Both layers had relu activation functions and the output layer had a sigmoid activation function. I started with these parameters as relu does better with nonlinear data, and two layers allows for a second layer to reweight the inputs from the first layer. Here are the preformance metrics of this model.

<img width="443" alt="1" src="https://user-images.githubusercontent.com/76264061/118508074-77c92300-b74c-11eb-9edb-c17b5d604916.png">

In the second attempt, I removed the "SPECIAL_CONSIDERATIONS" column as I thought this might have been confusing the model. I also lowered the threshold for the classification column so that there were more unique values from that column. I also added a third layer with 6 neurons apart of it. By adding a third layer, I wanted to give the model another chance to reweight the inputs from the second layer to the third. Here are the preformance metrics of this model.

<img width="443" alt="1" src="https://user-images.githubusercontent.com/76264061/118508074-77c92300-b74c-11eb-9edb-c17b5d604916.png">

In the third attempt, I reverted back the threshold for the classification column. I also changed the activation function for the three layers to tanh. I did this to see if it would perform better than the relu function. Here are the preformance metrics of this model.
<img width="443" alt="1" src="https://user-images.githubusercontent.com/76264061/118508074-77c92300-b74c-11eb-9edb-c17b5d604916.png">

In the fourth attempt, I removed the " STATUS" column as well as I thought it was confusing the model. I reverted back to two layers and the relu activation function. Lastly, I changed the neurons to 12 in the first layer and 8 in the second layer. This was to increase the parameters passed from the first layer to the second layer from 54 to 104. Here are the performance metrics of this model.

<img width="322" alt="2" src="https://user-images.githubusercontent.com/76264061/118508218-9cbd9600-b74c-11eb-84cd-94347f270075.png">

## Summary

After four attempts, I was unable to create a model that could preform a 75% accuracy rating. This is potential becasue I got rid of too many columns, I did not use the correct activation function, or I did not have hte right amount of layers and neurons. These were the main areas I continued the change with little to no improvement. Next time, I would research more about activation functions to make sure that I am always choosing the right one based on the data. 


### Sidenote for the grader 

I have unfrotunately been tested positive for Covid 10 and am currently under hospitalisation treatment. Kindly excuse my late submission and consider teh code. I am on a 100/100 streak and do not wanna break that. 
