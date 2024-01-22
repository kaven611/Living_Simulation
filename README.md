# Living_Simulation
## Summary
Here I created a decision model for a theoretical person named Hugh who recently completed his Master's Degree and is contemplating where to begin his career to maximize his net income (income after expenses). I used simulation functions in Excel like RAND() to simulate scenarios for his alternatives. Hugh lived in London ON and was deciding between working as a Data Analystin the following cities: London ON, Toronto ON, and Houston TX. Each with different possibilities of renting, buying and commuting. Each alternative had different costs of living and salaries for his desired job, and he could not be certain about the actual numbers for anything. For example, if he were to move to Toronto, he can't be certain how much his salary would be before landing a job, therefore I specified a range and simulated the possibilites. After doing research to obtain rough figures for each variable (salaries, house prices, etc.), after 1000 iterations it was deemed that renting a house in Houston was the most financially feasible alternative.

## Data Acquisition
I acquired all of the data from public sources such as glassdoor.com for the salary data. I did not need an actual data set, but instead needed ranges with estimated probabilities, therefore allowing me to simulate possibilities. Full reference list at the end.

## Data Preparation
For the data preparation I needed to assure that the data was in a unit that made sense to perform calculations on. I needed all expenses to be monthly. Further, in my Excel sheet I needed all of the raw figures to be in cells so I could use cell references later in formulas rather than hard coding. This was especially important for simulated data.
Examples of the raw data and randomized figures:

![image](https://github.com/kaven611/Living_Simulation/assets/156690481/08481e6a-c706-4eec-9624-45d6377d1f76)
![image](https://github.com/kaven611/Living_Simulation/assets/156690481/c676f2c1-7c7e-4897-9222-da5a36856ff0)

## Data Analysis
 I needed to simulate many of the values that could change in his first year of working or any time. For example, I needed to simulate the USD/CAD foreign exchange (FX) rate using the RANDBETWEEN() function. This function takes a range for your figure and spits out a random number within this range. For the FX rate  I took the minimum and maximum over the last 5 years allowing the simulation to take anything in between. I used the same technique to randomize mortgage rates and gas prices. Tables:

 ![image](https://github.com/kaven611/Living_Simulation/assets/156690481/874c9c5d-5e27-443b-97f0-667c9183c395)
![image](https://github.com/kaven611/Living_Simulation/assets/156690481/d6f53684-c345-458d-a381-ca52fcdcecb0)
![image](https://github.com/kaven611/Living_Simulation/assets/156690481/d85293a2-ba5a-4b00-9303-4d3275fbe345)


The RANDBETWEEN() function follows a uniform distribution, therefore all values are equally probable. For salary data this was not the case. Each city had a fairly large range from glassdoor.com. Each value in the range had a different number of survey responses. I calculated rough probabilities for approximate cutoff values within the range. For example, the London survey responses had the vast majority responding with salaries around the $53,000 range, some responses were over $62,000 and even less were around $72,000. Therefore I assigned probabilities of 85%, 10%, 5% for salaries of $53,000, $62,000, and $72,000 respectively. I then used the RAND() and VLOOKUP() functions in tandem to simulate figures that follow the probability distrubtion. I followed the same proccess for the other two cities. VLOOKUP tables:

![image](https://github.com/kaven611/Living_Simulation/assets/156690481/ec0983f0-5877-4941-bf60-09ff8fc95524)
