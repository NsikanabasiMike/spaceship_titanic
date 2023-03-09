## Table of Contents
- [Installation](#install)
- [Project Overview and Motivation](#motivate)
- [File Descriptions](#describe)
- [Licensing, Authors, and Acknowledgements](#acknowledge)

<a id='install'></a>
### Installation
1. Python 3.6 and latest from [here](https://www.python.org/downloads/)
2. Anaconda distribution of Python from [here](https://www.anaconda.com/blog/anaconda-distribution-2022-10#).

<a id='motivate'></a>
### Project Overview and Motivation 
This project is a competition staged at kaggle. More info about the competition is [here](https://www.kaggle.com/competitions/spaceship-titanic/overview).<br>  

Welcome to the year 2912, where your data science skills are needed to solve a cosmic mystery. We've received a transmission from four lightyears away and things aren't looking good.

The Spaceship Titanic was an interstellar passenger liner launched a month ago. With almost 13,000 passengers on board, the vessel set out on its maiden voyage transporting emigrants from our solar system to three newly habitable exoplanets orbiting nearby stars.

While rounding Alpha Centauri en route to its first destination—the torrid 55 Cancri E—the unwary Spaceship Titanic collided with a spacetime anomaly hidden within a dust cloud. Sadly, it met a similar fate as its namesake from 1000 years before. Though the ship stayed intact, almost half of the passengers were transported to an alternate dimension!

To help rescue crews and retrieve the lost passengers, you are challenged to predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system.

Help save them and change history!<br>

The first part is the Extract, Transform, and Load(ETL) process. Here, the dataset is read into a dataframe, explored, and cleaned with pandas.<br>

The second part is the machine learning portion. A random forest model is built and twerked with different hyperparameters. The prediction from the model is used to form a new dataframe.<br>


<a id='describe'></a>
### File Descriptions

There is one file and one folder. The file __spaceship_titanic__ contains the code for the competition.
Two files are available in the __data__ folder: spaceship_titanic.zip, and result.csv.<br>

Files
1. __spaceship_titanic.zip__ contains the following files:
_train.csv_ -  Personal records for about two-thirds (~8700) of the passengers, to be used as training data. It contains the following columns:
- PassengerId - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. People in a group are often family members, but not always.
- HomePlanet - The planet the passenger departed from, typically their planet of permanent residence.
- CryoSleep - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
- Cabin - The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard.
- Destination - The planet the passenger will be debarking to.
- Age - The age of the passenger.
- VIP - Whether the passenger has paid for special VIP service during the voyage.
- RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
- Name - The first and last names of the passenger.
- Transported - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.<br>
- _test.csv_ - Personal records for the remaining one-third (~4300) of the passengers, to be used as test data. The task is to predict the value of Transported for the passengers in this set.<br>
_sample_submission.csv_ - A submission file in the correct format. It has the following features:

- PassengerId - Id for each passenger in the test set.
- Transported - The target. For each passenger, predict either True or False.<br>
2. __result.csv__ - model prediction result appended to the passenger ids:
- PassengerId - Id for each passenger in the test set.
- Transported - Prediction.<br>


<a id='acknowledge'></a>
### Licensing, Authors, Acknowledgements
The data used is from [kaggle](https://www.kaggle.com/competitions/spaceship-titanic/data).
