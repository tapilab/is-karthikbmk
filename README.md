# Text Summarization using Deep Learning and Ridge Regression.
A template for students doing M.S. or undergraduate independent studies/theses.

See instructions here: [Instructions.md](Instructions.md)

This README.md file should summarize your project. Think of it as the short version of your project report.

## Problem

TBU

## Research questions

Here are the core questions / subproblems you will address:

1. ...
2. ...
3. ...

## Related work

Here's how other people have tried to solve this problem, with a few links/citations. 

## Data

DUC 2001 dataset will be used to build the initial model.

Here is an example data record.

## Methods

1. Extract Features. This will be X_train
2. Compute ROGUE score for every sentence across all the documents. This is will be y_train
3. This is now a regression problem. Use Ridge as the initial baseline model  
4. Predict using the trained model  
5. Repeat steps 1,2,3,4 with Deep Models


## Validation Errors

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/ridge.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/adam_logistic.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/adam_tanh.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/sgd_logistic.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/sgd_tanh.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/lbfgs_logistic.png)

![Ridge](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/lbfgs_tanh.png)

## Test Errors:  
![Test](https://github.com/tapilab/is-karthikbmk/blob/master/src/Results/Test.png)

## Summaries : 

Predicted Summary for doc  1 ::
-----------------------------------
Second Amendment states (1791): "A well regulated militia, being necessary to 
the security of a free State, the right of the people to keep and bear Arms, 
shall not be infringed."


Real Summary for doc  1 ::
-----------------------------------
The Second Amendment to the Constitution reads: "A well regulated militia, being necessary to the security of a free state, the right of the people to keep and bear arms shall not be infringed". The Second Amendment was originated by some of the states as protection against the federal government. The word "people" is used collectively and refers to a political entity such as a state. The Supreme Court on several occasions in the past has ruled that this amendment did not create a federally- protected right of individuals to bear arms but rather, limited the power of the federal government.


Predicted Summary for doc  2 ::
-----------------------------------
Johnson testified this week at a Canadian inquiry that his seven-year 
involvement with illegal performance-enhancing drugs included injections before 
the 1987 World Championships in Rome, where he set the existing world record of 
9.83 seconds.


Real Summary for doc  2 ::
-----------------------------------
US track and field officials said that Johnson should be stripped of his world record in the 100 meter dash. Johnson testified at a Canadian inquiry that he had been involved with illegal performance-enhancing drugs for seven years and had injections before he set the world record in the 1987 World Championship in Rome. His coach and physician had also testified at the inquiry. Carl Lewis said that while Johnson had not told the truth earlier, he was doing so now and speaking out against drugs and should be allowed back in the sport after he finishes his suspension.


Predicted Summary for doc  3 ::
-----------------------------------
Exxon Corp. on Wednesday increased its estimate of the total 1989 costs of 
cleaning up the massive Alaskan oil spill to $2 billion and said it would take 
another $500-million charge in the fourth quarter to cover costs from what is 
now the most expensive environmental disaster in history.


Real Summary for doc  3 ::
-----------------------------------
Exxon increased its estimate of the 1989 costs of cleaning up the most expensive environmental disaster in history to $2B and it could take another $500M. Exxon noted that these costs were the major reason for their lower net income for the year, but analysts said that Exxon's size would insulate it from serious long-term financial damage. Exxon's stock has lagged behind that of major oil firms and Exxon could suffer from continuing negative publicity from the Valdez spill and the subsequent heating oil spill into a waterway between New York and New Jersey.

Predicted Summary for doc  4 ::
-----------------------------------
Reforestation would give wooded areas in Yellowstone a "five-year jump" on natural regrowth of the woods and would "get it green again," says John Davis, Willamette Industries Inc.'s general manager for Western timber logging operations in Lewiston, Idaho.


Real Summary for doc  4 ::
-----------------------------------
Following the worst fire on record in Yellowstone National Park, biologist, Donald Despain examines the forest looking for signs of new life. By next spring, many seeds released from rock-hard pine cones will be fertilized by nutrients leaching into the soil from the now-packed ash, will sprout. Grasses and several types of wildflowers are already sprouting less than seven weeks after the fire. Next year, the ground cover replacing the park's burnt stands of aging lodgepole pines should provide a 30-fold increase in plant species. The new growth will attract a larger variety of birds and other animal life to the area.


Predicted Summary for doc  5 ::
-----------------------------------
The director of the county Social Services Agency wants all Orange County 
residents, including illegal aliens, to be counted in the 1990 Census, and he 
will ask the Board of Supervisors to support his position.


Real Summary for doc  5 ::
-----------------------------------
The Social Services director in Orange County wants all residents in the county to be counted in the 1990 Census. He will ask the Board of Supervisors to pass a resolution supporting his position. If the approximate 200,000 illegal aliens were not counted, the county would loose an estimated $56 million a year in federal revenue and lose representatives in Congress. On Thursday, the U.S. Senate and House agreed that illegal aliens should be counted. Before Thursday, the Senate had voted to bar the Census Bureau from counting illegal aliens. The House had twice rejected efforts to exclude aliens.


## Conclusions / Future Work

Here's the main conclusions and a list of directions for improvement.

1. Generate the summary instead of extracting it.  
2. Train on all the DUC Datasets - DUC 2002, 2003....2006  
3. Regularize the Deep Models using Dropout.  

