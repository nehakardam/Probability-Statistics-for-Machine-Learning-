# Random Variable and Probability Distribution

### Explain what is Random Variables and Random Samples
Random sampling and random variables are related concepts in statistics, but they deal with different things:
- Random Variable: This is a variable whose value depends on the outcome of a random event. It basically assigns a numerical value to each possible outcome in an experiment. Imagine a coin toss - the random variable could be "Heads" (assigned a value of 1) or "Tails" (assigned a value of 0)
- Random Sample: This refers to a subset of data points chosen from a larger population, where every element in the population has an equal chance of being selected. It's like picking names out of a hat - each name has an equal probability of being drawn. The size of the sample (number of data points) is usually denoted by "n".

#### Here's an analogy to understand the difference:
- Think of a bag full of colored candies (population). A random variable could be the color you pick (red = 1, blue = 2, etc.).
- A random sample would be grabbing a handful of candies from the bag without looking (each candy has an equal chance of being chosen).
#### Here's how they connect:
- We can use random variables to analyze random samples. For example, if we measure the weight of each candy we pick from the random sample (weight is the random variable), we can calculate the average weight of the candies in the sample (a statistic).

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/e1944af7-b630-4e01-ba5d-680a03a9570e)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/e57b0840-1ccc-41a8-9eda-e3b23566314c)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/dc1eadf1-3b31-4232-8a72-fc3f2badeca0)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/bc5823be-29a4-4f48-85ca-84abe74a4fe7)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/cc046510-c514-4fac-ad12-df25631bc51f)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/e0b359b4-2971-4f09-8854-908fd55fe9ac)


### Using Random Variables and Probability Distributions for Expected Value (with Example)

Let's explore why random variables are useful with an example that uses math: expected value. Imagine you're running a lemonade stand, and the number of customers you get each day is uncertain (random).

1. **Random Variable (X):** Number of customers per day
2. **Possible Values:** X = 0 (no customers), X = 1 (one customer), X = 2 (two customers), etc. (This is a discrete random variable).

Now, suppose you charge $1 per lemonade and want to know your average daily income. However, the number of customers is random, so your income will vary each day. This is where the concept of expected value comes in.

#### Expected Value:
The expected value of a random variable is the average of the values it takes, weighted by their probabilities. It represents the average outcome you can expect in the long run.

#### Math behind Expected Value:
Here's the formula for expected value (denoted by E):
\[ E(X) = \sum (x * P(X = x)) \]
where:
- Σ (sigma) represents summation over all possible values of X.
- x is a specific value that X can take.
- P(X = x) is the probability of X taking the value x.

#### Example with Lemonade Stand:
Let's say you believe the following about your customer traffic:
- There's a 20% chance (probability) of getting no customers (X = 0).
- There's a 30% chance (probability) of getting one customer (X = 1).
- There's a 40% chance (probability) of getting two customers (X = 2).
- There's a 10% chance (probability) of getting three customers (X = 3).

#### Expected Daily Income Calculation:
We can calculate your expected daily income by considering the income for each possible number of customers and weighting it by the probability of that number occurring:
\[ E(Income) = E(X) * $1 \] (since income per customer is $1)
\[ E(X) = (0 * 0.2) + (1 * 0.3) + (2 * 0.4) + (3 * 0.1) \]
\[ E(X) = 0 + 0.3 + 0.8 + 0.3 = 1.4 \]

Therefore, your expected daily income (\( E(Income) \)) is $1.40. This doesn't guarantee you'll make exactly $1.40 every day, but over a long period (many days), your average daily income should be close to $1.40.

#### Why is this useful?
By calculating the expected value of your customers (X), you can estimate your average daily income. This helps you with planning: how much lemonade to prepare, how much change to keep on hand, etc.

This is a simplified example, but the concept of expected value using random variables is widely used in various fields, from finance (expected return on investments) to queuing theory (expected waiting time in line).

### Explain the difference between independent and un-correlated random variables

Independent and uncorrelated random variables are related concepts, but they have distinct meanings and implications in probability theory and statistics.

1. **Independent Random Variables:**
   - Independent random variables are variables whose outcomes do not influence each other.
   - Formally, two random variables \( X \) and \( Y \) are independent if and only if the probability of any event involving both \( X \) and \( Y \) occurring is equal to the product of the probabilities of the individual events.
   - Mathematically, if \( X \) and \( Y \) are independent, then \( P(X \cap Y) = P(X) \times P(Y) \).
   - For example, if you flip two fair coins, the outcome of one coin flip does not affect the outcome of the other. The events "getting heads on the first coin" and "getting tails on the second coin" are independent.

2. **Uncorrelated Random Variables:**
   - Uncorrelated random variables are variables whose covariance is zero.
   - Covariance measures the degree to which two random variables change together. If the covariance is zero, it means there is no linear relationship between the variables.
   - However, uncorrelated random variables can still be dependent, meaning that knowing the value of one variable provides information about the other.
   - For example, let \( X \) be a random variable representing the temperature in Celsius and \( Y \) be a random variable representing the temperature in Fahrenheit. These variables are uncorrelated because their covariance is zero, but they are not independent because knowing the value of one variable allows you to determine the value of the other through a linear transformation (Fahrenheit = Celsius * 9/5 + 32).

In colclusion, the main difference between independent and uncorrelated random variables is that independence implies no relationship whatsoever between the variables, while uncorrelatedness specifically refers to the absence of a linear relationship between the variables but does not necessarily imply independence.



