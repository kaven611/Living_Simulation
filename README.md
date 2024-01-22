# Living_Simulation
## Summary
Here I created a decision model for a theoretical person named Hugh who recently completed his Master's Degree and is contemplating where to begin his career to maximize his net income (income after expenses). I used simulation functions in Excel like RAND() to simulate scenarios for his alternatives. Hugh lived in London ON and was deciding between working in the following cities: London ON, Toronto ON, and Houston TX. Each with different possibilities of renting, buying and commuting. Each alternative had different costs of living and salaries for his desired job, and he could not be certain about the actual numbers for anything. For example, if he were to move to Toronto, he can't be certain how much his salary would be before landing a job, therefore I specified a range and simulated the possibilites. After doing research to obtain rough figures for each variable (salaries, house prices, etc.), after 1000 iterations it was deemed that renting a house in Houston was the most financially feasible alternative.

## Data Acquisition
I acquired all of the data from public sources such as glassdoor.com for the salary data. I did not need an actual data set, but instead needed ranges with estimated probabilities, therefore allowing me to simulate possibilities. Full reference list at the end.

## Data Preparation
For the data preparation I needed to assure that the data was in a unit that made sense to perform calculations on. I needed all expenses to be monthly. Further, in my Excel sheet I needed all of the raw figures to be in cells so I could use cell references later in formulas rather than hard coding. This was especially important for simulated data.
Examples of the raw data and randomized figures:
![image](https://github.com/kaven611/Living_Simulation/assets/156690481/08481e6a-c706-4eec-9624-45d6377d1f76)
![image](https://github.com/kaven611/Living_Simulation/assets/156690481/c676f2c1-7c7e-4897-9222-da5a36856ff0)
