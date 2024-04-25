# Random Variable and Probability Distribution

### 1. Explain what is Random Variables and Random Samples
Random sampling and random variables are related concepts in statistics, but they deal with different things:
- ***Random Variable***: This is a variable whose value depends on the outcome of a random event. It basically assigns a numerical value to each possible outcome in an experiment. Imagine a coin toss - the random variable could be "Heads" (assigned a value of 1) or "Tails" (assigned a value of 0)
- ***Random Sample***: This refers to a subset of data points chosen from a larger population, where every element in the population has an equal chance of being selected. It's like picking names out of a hat - each name has an equal probability of being drawn. The size of the sample (number of data points) is usually denoted by "n".

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


### 2. Using Random Variables and Probability Distributions for Expected Value (with Example)

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

### 3. Explain the difference between independent and un-correlated random variables

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

 ### 4. What is the difference between Discrete and Continous Random Variables?

#### Discrete Random Variables 
Take on a countable number of distinct values (e.g., 0, 1, 2, ...)
***Characteristics***
* Have a finite or infinite number of possible outcomes
* Probability is assigned to each specific value
***Examples***
* Number of heads in 5 coin tosses
* Number of defective products in a batch

#### Continuous Random Variables
Can take on any value within a certain range or interval (e.g., 0 ≤ x ≤ 1)
***Characteristics***
* Have an uncountable number of possible outcomes
* Probability is assigned to intervals or ranges of values
***Examples***
* Height of a person
* Time until a component fails

#### Key Differences
***Number of possible outcomes***
* Discrete variables: countable
* Continuous variables: uncountable
***Probability assignment***
* Discrete variables: assign probability to specific values
* Continuous variables: assign probability to intervals or ranges
***Distribution functions***
* Discrete variables: use probability mass functions (PMFs)
* Continuous variables: use probability density functions (PDFs) and cumulative distribution functions (CDFs)
 
![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/a6164125-a2e1-48f8-b795-26712d0ebf6a)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/0de0b4f1-febc-42b0-874e-bdd19f4ea79d)

### 5. Explain Mean, Variance, and Covariance

#### Mean

* **Definition**: The mean, also known as the average, represents the central tendency of a dataset.
* **Calculation**: Sum of all values divided by the number of values (n).
* **Interpretation**: Provides a single number that summarizes the "middle" of the data.

#### Variance

* **Definition**: Measures how spread out the data is from the mean.
* **Calculation**: Squared deviations from the mean, averaged and considering the sign.
* **Relation to Expectation**: Calculates the average squared deviation from the expected value (the mean).
* **Note**: Slight variations in calculation for sample vs. population.

#### Expectation

* **Definition**: Average value expected from a random variable or function of a random variable.
* **Relation to Variance**: Variance calculates the average squared deviation from the expected value (the mean).

#### Covariance

* **Definition**: Measures the direction and strength of the linear relationship between two variables.
* **Calculation**: Considers how much two variables tend to change together.
* **Interpretation**:
	+ Positive covariance: Variables tend to move in the same direction.
	+ Negative covariance: Variables tend to move in opposite directions.
* **Note**: Measured in units that are the product of the units of the two variables.

#### Key Points

* **Mean**: Central tendency.
* **Variance**: Spread around the mean (uses squared deviations from the mean, related to expectation).
* **Covariance**: Direction and strength of linear relationship between two variables.

#### Example

Analyzing student heights and test scores:

* **Mean**: Average height and average test score.
* **Variance**: Spread of student heights and scores from their respective means.
* **Covariance**: Whether taller students tend to have higher scores (positive covariance) or shorter students tend to have higher scores (negative covariance).

### 6. Explain expected value calculations for discrete random variables

#### Expected Value (Mean) for Discrete Random Variables

The expected value, also known as the mean (μ), represents the average value you expect to get if you were to repeat a random experiment a large number of times.
It considers all possible outcomes of the experiment and their associated probabilities.

***Formula:***
The expected value for a discrete random variable X is calculated by summing the product of each possible value (x) of X and its corresponding probability (P(X=x)):
E(X) = Σ(x * P(X=x)) for all possible values x

#### Simple Probability Scenarios
Here are some examples of expected value calculations in simple probability scenarios:

***1. Coin Flip:***
You flip a fair coin (heads or tails are equally likely).
Possible outcomes (X): {heads, tails} with probability P(heads) = P(tails) = 1/2.
Expected value (average outcome you expect from many flips):
E(X) = (1 * 1/2) + (0 * 1/2) = 1/2 (heads get 1 point, tails get 0 points, so the average is halfway between).

***2. Rolling a Die:***
You roll a fair die with six sides (1 to 6).
Possible outcomes (X): {1, 2, 3, 4, 5, 6} with equal probability P(x) = 1/6 for each side.
Expected value (average roll you expect in many rolls):
E(X) = (1 * 1/6) + (2 * 1/6) + (3 * 1/6) + (4 * 1/6) + (5 * 1/6) + (6 * 1/6) = 3.5

***3. Picking a Card:***
You pick a card from a standard deck of 52 cards without replacement.
There are 4 aces (A).
Possible outcomes (X): {number card, face card, ace} with probabilities depending on the specific question.

***Example:*** What's the expected value of X if you get a point for aces and no points for others?
P(ace) = 4/52, P(not ace) = 48/52
E(X) = (1 * 4/52) + (0 * 48/52) = 1/13 (since only aces get points).


