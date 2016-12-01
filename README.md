# Text Summarization using Deep Learning and Ridge Regression

## Problem


## Research questions

1.What are the relevant features for summarization?
2.How to tune the Hyper-parameters for a given model?
3.Which model works best for summarization?
4.How to stich together multiple sentences for summarization?

## Related work

Here's how other people have tried to solve this problem:  

1. Query-Oriented Multi-Document Summarization via Unsupervised Deep Learning 
http://www.aaai.org/ocs/index.php/AAAI/AAAI12/paper/view/5058 

2. Ranking with Recursive Neural Networks and Its Application to Multi-document Summarization:  
http://www.aaai.org/ocs/index.php/AAAI/AAAI15/paper/download/9414/9520

3. Reader-Aware Multi-Document Summarization via Sparse Coding:  
www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/download/11398/10841

## Data

DUC 2001 dataset will be used to build the initial model.Here is an example data record:

<DOC>
<DOCNO> LA021090-0005 </DOCNO>
<DOCID> 174161 </DOCID>
<DATE>
<P>
February 10, 1990, Saturday, Home Edition 
</P>
</DATE>
<SECTION>
<P>
Metro; Part B; Page 6; Column 4; Op-Ed Desk 
</P>
</SECTION>
<LENGTH>
<P>
873 words 
</P>
</LENGTH>
<HEADLINE>
<P>
GUN NUTS HAVE A REAL POINT; 
</P>
<P>
CONSTITUTION: THE CLIMATE MAY NOW BE RUNNING IN FAVOR OF MORE RESTRICTIONS, 
INCLUDING A BAN ON HANDGUNS. BUT THERE'S STILL THE SECOND AMENDMENT. 
</P>
</HEADLINE>
<BYLINE>
<P>
By MICHAEL KINSLEY, Michael Kinsley writes the TRB column for The New Republic. 
</P>
</BYLINE>
<TEXT>
<P>
Around the world, national theologies are crumbling: communism, apartheid and, 
here in America, the worship of guns -- to foreigners, the single craziest 
thing about us. 
</P>
<P>
Do you sense an outbreak of sanity about gun control? I do. There was retired 
Chief Justice Warren Burger preaching sacrilege on the cover of Parade magazine 
a couple of weeks ago. A Time Magazine/Cable News Network poll reports that 87% 
of gun owners themselves favor a seven-day waiting period for handgun 
purchases; three-quarters favor registration of semi-automatic weapons and 
handguns, and half favor registration of rifles and shotguns. 
</P>
<P>
Unfortunately, there is the Second Amendment to the Constitution: "A well 
regulated militia, being necessary to the security of a free State, the right 
of the people to keep and bear arms, shall not be infringed." 
</P>
<P>
Most right thinkers take comfort in that funny stuff about the militia. Since 
the amendment's stated purpose is arming state militias, they reason, it 
creates no individual right to own a gun. That reasoning is good enough for the 
ACLU. But would civil-libertarians be so stinting about an amendment they felt 
more fond of? Say, the First? 
</P>
<P>
The purpose of the First Amendment's free-speech guarantee was pretty clearly 
to protect political discourse. But liberals reject the notion that free speech 
is therefore limited to political topics, even broadly defined. True, that 
purpose is not inscribed in the amendment itself. But why leap to the 
conclusion that a broadly worded constitutional freedom ("the right of the 
people to keep and bear arms") is narrowly limited by its stated purpose, 
unless you're trying to explain it away? A colleague says that if liberals 
interpreted the Second Amendment the way they interpret the rest of the Bill of 
Rights, there would be law professors arguing that gun ownership is mandatory. 
</P>
<P>
The most thorough parsing of the Second Amendment is a 1983 article in the 
Michigan Law Review by Don Kates, a gun enthusiast. Kates expends most energy 
demonstrating that at the time of the Bill of Rights, all able-bodied men were 
considered to be part of the "militia" and were expected to defend the state if 
necessary. I'm not sure this is as clinching an argument as Kates seems to 
think. The fact that once upon a time everyone was a member of the militia 
doesn't prove that everyone still has a right to a gun even after the 
composition of the militia has changed. 
</P>
<P>
But Kates has other bullets in his belt. The phrase "right of the people" 
appears four other times in the Bill of Rights (including the First Amendment). 
In all these other cases, everyone agrees that it creates a right for 
individual citizens, not just some collective right of states as a whole. Kates 
also marshals impressive historical evidence that the Second Amendment, like 
other Bill of Rights protections, was intended to incorporate English common 
law rights of the time, which pretty clearly included the right to keep a gun 
in your home for reasons having nothing to do with the militia. 
</P>
<P>
If there is a good reply to Kates's fusillade, the controllers haven't made it. 
Of course the existence of an individual right to own guns doesn't mean that it 
is absolute. What are the limits? In the Supreme Court's one 20th-Century 
treatment of the Second Amendment, it held somewhat ambiguously in 1939 that 
sawed-off shotguns aren't necessarily protected by the Constitution without 
proof that they are the kind of weapon a militia might have used. 
</P>
<P>
Working from that decision and the common law, Kates says the amendment's 
protection should be limited to weapons "in common use among law-abiding 
people," useful for law enforcement or personal defense, and lineally descended 
from weapons known to the Framers. (No nuclear bombs.) He adds that they must 
be light enough for an ordinary person to carry ("bear"), and even that they 
can't be especially "dangerous or unusual." He says that the amendment places 
no limit on mandatory registration or laws against concealed weapons in public. 
</P>
<P>
This list seems quite reasonable and moderate, though where it all comes from 
is not clear. In suggesting, for example, that it would be fine to ban 
automatic rifles but not semi-automatics, Kates is slicing the constitutional 
salami pretty thin. But in what I suspect was the main purpose of his exercise 
-- establishing that a flat ban on handguns would be hard to justify under the 
Constitution -- Kates builds a distressingly good case. 
</P>
<P>
The downside of having a Bill of Rights is that the protection of individual 
rights usually entails social costs. This is as true of the Second Amendment as 
it is of the First, Fourth, Fifth and Sixth. The downside of having those 
rights inscribed in a Constitution, protected from the whims of majority rule, 
is that they can't be re-defined as life changes. It would be remarkable indeed 
if none of the Bill of Rights became less sensible and more burdensome with 
time. 
</P>
<P>
Talking and writing are as central to American democracy as they ever were; 
shooting just isn't. Gun nuts are unconvincing (at least to me) in their 
attempts to argue that the individual right to bear arms is still as vital to 
freedom as it was in 1792. But the right is still there. 
</P>
</TEXT>
<TYPE>
<P>
Opinion 
</P>
</TYPE>
</DOC>

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

## Test Accuracy:  
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

