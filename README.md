# Internship Project <br>
## MotoGP rider analysis

Author: Zheng Jing <br>
Programming Language 1: Python (.ipynb) <br>
Programming Language 2: R (.rmd) <br>

## Goals

for all races and all riders, we

​ a) implemented the predator index and prey index

​ b) implemented the net index, volatility index, and efficiency index

​ c) developed weighted predator & prey indexes (additional weight & exponential weight)

​ d) implemented summary statistics & data aggregation

​ e) visualizaions of riders' annual trajectory (2015 - 2019)

## Indexes Descriptions & Algorithm design


​ a) **Grid** = Rider's starting position, determined from the qualifying race

​ b) **Final** = Rider's final position

​ c) **Predator** = the total number of positions that a rider moves forward, regardless of him moving backward

​ d) **Prey** = the total number of positions that a rider moves backward, regardless of him moving forward

​ e) **Net** = Predator - Prey = Final - Grid, (which measures a rider's pure movement/displacement throughout the entire race)

​ f) **Volatility** = Predator + Prey, (which measures a rider's riding style - high means aggressive; low means conservative)

​ g) **Efficiency** = Net/Volatility, (the percentage of efficient movements)

- For example, a rider has net =2 and volatility = 10 . That means only 2 out of 10 moves are efficient for moving forward, and the other 8 moves are 4-4 cancelled off. So net/volatility = 2/10 = 20% gives us the efficiency of the rider’s movement.

- Since volatility is always positive but net can be negative, let’s consider another example with net = -2 and volatility = 10. That means 2 of 10 moves are counter-efficient for moving forward, and again the other 8 moves are 4-4 cancelled off. So net/volatility = -20% gives us a negative efficiency of the rider’s movement.

​ h) **Weighted Predator** = Predator - Grid, (a way to compare riders' offensive ability by taking grid position into account)

​ i) **Weighted Prey** = the number of total riders - Grid - Prey, (a way to compare riders' defensive ability by taking grid position into account)


## Data
https://www.motogp.com/en/Results+Statistics <br>
All the data (lap charts) are collected from MotoGP official website. <br>


## Methodology

​ a) algorithm implementations

​ b) data aggregation <br>

- compute the summary statitics - grouped by rider, rider and year, rider and circuit...

*by looking at the summary table, we are able to break down riders' performance in parts: offensive, defensive, volatility, efficiency, and final position*

​ c) visualizations (barplot, boxplot, histograms, scatterplot...) <br>
 
- Efficiency vs Volatility, e.g. Joan Mir (rookie) vs Alex Rins (veteran) <br>
- Riders' annual trajectories (to study riders' improvement)
- A comparison of riders' performances by circuit <br>

## Conclusion & Analysis
