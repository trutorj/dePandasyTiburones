# The most  conflictive human vs the most trouble maker shark
### Data cleaning with Pandas
## Introduction
The main purpose of this project is double. In one hand, we want to determine the profile of the people who has provoked the most of the provoked incidents (nationality, activity, sex and age). Global Shark Attack File defines a provoked incident as one in which the shark was speared, hooked, captured or in which a human drew "first blood". In the other hand, we want to know which shark species (and from which regions) have the largest number of recorded attacks (provoked and unprovoked).

## Materials and methods
The data used in this work was downloaded from (https://www.kaggle.com/teajay/global-shark-attacks). The data cleaning process used pandas, regex and numpy libraries.
We started dividing the dataset into two sets:
* Humans: with the variables *Type*, *Country*, *Activity*, *Sex* and *Age*.
* Sharks: with the variables *Country*, *Area* and *Specie*.

As we are only interested in provoked incidents, the first action was filter the human dataset by provoked incidents. The next step was asses the amount and percentage of NA's values. Because of the high percentage of NAs in *Age* (>50%), we decided to drop it. For the rest of variables, we drop the rows containing NA's. Then, to simplify the name of the activities in the moment of the incident by using a regex expression, in order to categorize better the activities.

Regarding the cleaning of sharks datasets, we started by evaluating the NA's and deleting the rows containing NA's. Then, we extracted  the species names, by selecting the one or two words preceding the main shark species's names (i.e: shark, catfish and pointer). After that, we performed several cleanings of whitespaces and words not related with sharks species.

## Results
### The most conflictive human
In order to determine the most conflictive human, we analyze the most repeated value in *Country*, *Activity* and *Sex* variables. Therefore, based of this values, the most conflictive human would be a US citizen male who is fishing.
### The most trouble maker shaker
As we did with the humans, we determine the most agresive specie and its region. We groupped the number of attacks by region and country and selected the top five highest values. We obtained the next ranking:
1. White shark in California (USA). 157 attacks.
2. White shark in Western Cape Province (SOUTH AFRICA). 99 attacks.
3. Tiger shark in Hawaii (USA). 83 attacks.
4. White shark in South Australia (AUSTRALIA). 41 attacks.
5. Bull shark in Florida (USA). 41 attacks.


