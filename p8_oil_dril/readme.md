# Choosing the location for oil well

Glavrosgosneft Mining Company. We need to decide where to drill a new well.

We were provided with oil samples in three regions: in each 10,000 fields, where the quality of oil and the volume of its reserves were measured. It is necessary to build a machine learning model that will help determine the region where mining will bring the greatest profit. To analyze possible profits and risks, we will use the *Bootstrap technique.*

Task conditions:

- The budget for the development of wells in the region is 10 billion rubles.
- At current prices, one barrel of raw materials brings 450 rubles of income. The income from each unit of the product is 450 thousand rubles, since the volume is indicated in thousands of barrels.
- After risk assessment, it is necessary to leave only those regions in which the probability of losses is less than 2.5%. Among them, the region with the highest average profit is chosen.

# Results of the research
The best Region to invest in development will be No. 2, since:

1) It has the highest average profit: 518 million rubles.

2) It has the highest total profit: 518,259 million rubles.

3) Absence of losses (negative profit) in the confidence interval

4) The lowest risk of losses: 0.3%.

**Libraries** - pandas, numpy, seaborn, stats, sklearn,  LinearRegression, GridSearchCV
