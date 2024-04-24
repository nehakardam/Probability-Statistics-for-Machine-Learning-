## Introduction to Probability 

This document provides a basic understanding of probability concepts relevant to machine learning.

### 1. What is Probability?

Probability is a measure of the likelihood that an event will occur. It quantifies the uncertainty or randomness associated with a particular event. In the context of machine learning, understanding probability is crucial as it forms the basis for various algorithms and models. 

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/b914206a-1e9f-4a4f-b452-95f00bc18b8b)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/78673069-9151-4525-bcfd-ada89cf4e948)

#### Simple Example: Coin Toss

Consider the simple example of tossing a fair coin. The possible outcomes are either heads (H) or tails (T). The probability of getting heads (P(H)) is 0.5, and the probability of getting tails (P(T)) is also 0.5. Here, each outcome is equally likely.

### 2. Complement of Probability

The complement of an event A, denoted by $A$' or $A^c$, represents all outcomes that are not in event A. The probability of the complement of event A is given by $P(A')$ = $1$ - $P(A)$.

**Example:**

- Consider the event of getting a head when tossing a fair coin. The complement of this event (not getting a head) is getting tails. Thus, $P(not getting a head)$ = $1$ - $P(getting a head)$ = $1$ - $0.5$ = $0.5$

### 3. Sum of Probabilities (Union and Intersection of Events)

There are two main concepts related to combining probabilities of events:

* **Union of Events:** The probability of the union of two events A and B, denoted by $P(A \cup B)$, is the probability that at least one of the events occurs. If A and B are disjoint events (mutually exclusive), then $P(A \cup B)$ = $P(A)$ + $P(B)$.
* **Intersection of Events:** The probability of the intersection of two events A and B, denoted by $P(A \cap B)$, is the probability that both events occur simultaneously.

**Example:**

- Suppose we have two events: Event A is rolling an even number on a fair six-sided die, and Event B is rolling a number greater than 3. 
  - P(A) = $\frac{1}{2}$ (since there are 3 even numbers out of 6).
  - P(B) = $\frac{1}{2}$ (since there are 3 numbers greater than 3 out of 6).
  - As the events are mutually exclusive, $P(A \cup B)$ = P(A) + P(B) = $\frac{1}{2}$ + $\frac{1}{2}$ = $1$
  - The probability of the intersection of A and B ($P(A \cap B)$) is the probability of rolling an even number greater than 3, which is $P(A \cap B)$ = $\frac{1}{3}$.

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/818f3d39-e127-4b1a-8ea0-2182cdc154a1)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/f2be9450-09d9-439b-a522-bd75cbda34ab)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/85701772-34df-4e13-aa30-455fc30152c7)

### 4. Disjoint Events vs Joint Events

In probability theory, events are described as "join" or "disjoint" based on their relationship with each other.

#### 4.5 Joint Events:
Joint events, also known as "simultaneous" or "dependent" events, are events that can occur at the same time or are related in some way.
In simpler terms, joint events have outcomes that can happen together.
For example, if we have two events A and B, the joint probability of both events occurring (denoted as P(A ∩ B)) represents the probability that both A and B occur simultaneously.

#### 4.6 Disjoint Events:
Disjoint events, also known as "mutually exclusive" events, are events that cannot occur at the same time or have no outcomes in common.
In other words, if one event happens, the other cannot happen at the same time.
For example, if we have two events A and B, and they are disjoint, it means that P(A ∩ B) = 0, indicating that the events cannot occur simultaneously.

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/5317780b-62d4-431e-b8f8-6af36635c9e3)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/01272290-f9ed-4a5d-a075-52a69b2117b4)

### 5. Independence of Events

Two events A and B are said to be independent if the occurrence of one event does not affect the occurrence of the other. Mathematically, for independent events, $P(A \cap B)$ = $P(A) \times P(B)$.

**Example:**

- Consider tossing a fair coin and rolling a fair six-sided die. The outcomes of these two events are independent since the result of tossing the coin does not influence the result of rolling the die.

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/141fb7ad-c703-43a5-aa71-561a13ed6d2e)

### 6. Calculate Probability of Union of Multiple Events

#### General Principles:
- **Set Theory:** Events can be thought of as sets. The union (denoted by U) of two sets includes elements that belong to at least one of the sets, while the intersection (denoted by ∩) includes elements common to both sets.
- **Probability Rules:** Two main rules exist depending on whether events are mutually exclusive (cannot occur together) or not:
  - *Addition Rule (Mutually Exclusive Events):* When events cannot occur simultaneously, the probability of their union (A or B) is the sum of their individual probabilities (P(A) + P(B)).
  - *General Addition Rule (Not Mutually Exclusive):* For events that can co-occur, we consider the probability of both happening (intersection). The probability of the union (A or B) is the sum of the individual probabilities minus the probability of their intersection (P(A) + P(B) - P(A ∩ B)).

#### Key Points to Remember:
- **Identify Independence:** Determine if events are mutually exclusive or not to apply the appropriate rule (addition or general addition).
- **Conditional Probability:** In complex scenarios with multiple events, conditional probability (P(B|A)) might be necessary.

#### Examples:
- *Coin Flip (Mutually Exclusive):* Flipping heads (H) and tails (T) are mutually exclusive. P(H or T) = P(H) + P(T) = 1/2 + 1/2 = 1 (since one or the other must happen).
- *Rolling a Die (Not Mutually Exclusive):* Getting a 2 (event A) and getting an even number (event B) are not mutually exclusive (both can happen). If P(A) = 1/6, P(B) = 3/6, and P(A ∩ B) = 1/6, then P(A or B) = P(A) + P(B) - P(A ∩ B) = 1/6 + 3/6 - 1/6 = 1/2.

#### Additional Points:
- Formulas exist for calculating probabilities of intersections of more than two events, with the core concept remaining the same.
- Be ready to discuss conditional probability if the interview explores more complex scenarios.

### 7. Calculate Probability of Intersection of Multiple Events

When dealing with multiple events, we often need to calculate the probability of their intersection, i.e., the probability that all events occur simultaneously. This concept is crucial in various fields, including machine learning, statistics, and data science.

#### Definition:

The probability of intersection of multiple events is defined as the probability that all events occur together. It is denoted as P(A ∩ B ∩ C ...), where A, B, C, ... are the events.

In other words, in probability theory, the intersection of events refers to the scenario where all the considered events occur simultaneously. Calculating the probability of this intersection helps us determine how likely it is for multiple conditions to be met together.

#### Formula

If events A and B are independent (the occurrence of one doesn't affect the probability of the other), the probability of their intersection (P(A ∩ B)) is calculated by multiplying their individual probabilities:

P(A ∩ B) = P(A) * P(B)

The probability of intersection of multiple events can be calculated using the following formula:

P(A ∩ B ∩ C ...) = P(A) * P(B|A) * P(C|A ∩ B) * ...

where:

- P(A) is the probability of event A
- P(B|A) is the conditional probability of event B given event A has already occurred
- P(C|A ∩ B) is the conditional probability of event C given both events A and B have already occurred, and so on

#### Examples:

**Example 1: Independent Events**

Suppose we have two events:

  - A: It rains today (probability 0.3)
  - B: The bus is late (probability 0.2)

We want to calculate the probability that it rains today and the bus is late.

P(A ∩ B) = P(A) * P(B|A) = 0.3 * 0.2 = 0.06

So, the probability that it rains today and the bus is late is 0.06 or 6%.

#### Example 2: Dependent Events**

Suppose we have three events:

  - A: A customer buys a phone (probability 0.4)
  - B: A customer buys a laptop (probability 0.3)
  - C: A customer buys a tablet (probability 0.2)

We want to calculate the probability that a customer buys all three products.

**Note:** In this scenario, events might be dependent (purchasing a phone might influence the decision to buy a laptop). We'll assume some level of independence for simplicity.

P(A ∩ B ∩ C) = P(A) * P(B|A) * P(C|A ∩ B) = 0.4 * 0.3 * 0.2 = 0.024

**Important:** Be cautious when using the product rule for potentially dependent events. Analyze the problem carefully and consider conditional probabilities if necessary.

So, the probability that a customer buys all three products is 0.024 or 2.4%.

Calculating the probability of intersection of multiple events is a fundamental concept in probability theory. By using the formula and examples provided, you can apply this concept to real-world problems and make informed decisions.

### 8. Product Rule for Independent Events:
- This rule applies to independent events, where the occurrence of one event doesn't affect the probability of the other.
- The probability of the intersection of multiple independent events (A, B, C...) happening together, denoted by P(A ∩ B ∩ C...), is the product of the individual probabilities of each event: P(A ∩ B ∩ C...) = P(A) * P(B) * P(C) * ...

#### Key Points to Remember:
- **Independence is Crucial:** The product rule holds true only for independent events. Dependent events require adjusting probabilities using conditional probabilities.
- **Order Doesn't Matter:** The order of multiplying probabilities doesn't affect the final answer (commutative property).

#### Examples:
- *Flipping Coins (Independent):* Flipping two coins where A = heads on the first coin and B = heads on the second are independent events. P(A ∩ B) = P(A) * P(B) = 1/2 * 1/2 = 1/4.
- *Rolling Dice (Not Independent):* Getting a specific number (e.g., A = 6) and getting an even number (B = even) are dependent events, as getting a 6 automatically fulfills the condition of getting an even number. In such cases, simple product rule cannot be used, and conditional probability is necessary.

#### Additional Points:
- The product rule extends to calculating the probability of intersections for more than three events by multiplying individual probabilities.
- Understand the concept of independence and its critical role in using the product rule.

  
### 9. Conditional Probability

Conditional probability is the probability of an event occurring given that another event has already occurred. It is denoted by \$( P(A|B)$ \), the probability of event A given event B. The formula for conditional probability is given by:

\$[ P(A|B) = \frac{P(A \cap B)}{P(B)} $\]

Where:
- \$( P(A \cap B) \)$ is the probability of both events A and B occurring.
- \$( P(B) \)$ is the probability of event B occurring.

#### Key Points on When to Use Conditional Probability:

- **Non-Independent Events:** The product rule (probability of intersections for independent events) cannot be directly applied to non-independent events. Conditional probability is crucial for these situations.
- **Real-World Scenarios:** Many real-world events are not independent. Understanding conditional probability allows you to reason about these more nuanced situations.
- **Refining Probability Based on New Information:** As you learn more about a situation (e.g., it rained), conditional probability helps update the probability of other events (muddy footprints) based on that new information.

#### Example with Medical Testing:

- **Event A:** Having a disease.
- **Event B:** Testing positive for the disease.
   - A positive test result (B) is more likely if you actually have the disease (A). P(B|A) is high. However, a positive test result can also occur if you don't have the disease (false positive). P(B| not A) is lower than P(B|A).

### 10. Conditional Probability Calculations:
There are different formulas for calculating conditional probability depending on the context. However, the core idea is to consider the probability of the event of interest (B) happening given that another event (A) already occurred.

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/f4cb8a25-a16d-4fb0-ac88-faeadb2bb045)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/4715006b-27c9-4193-88bb-03a17997c62e)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/0c3c74e4-d817-4be1-9cf1-0ac8be361485)

#### Example:

Consider a standard deck of 52 playing cards. What is the probability of drawing a King given that the card drawn is a face card?

- Event A: Drawing a King.
- Event B: Drawing a face card.

There are 12 face cards in a standard deck (4 Kings included). So, $\( P(B) = \frac{12}{52} = \frac{3}{13} \)$.
Among those 12 face cards, there are 4 Kings. So, $\( P(A \cap B) = \frac{4}{52} = \frac{1}{13} \)$.
Using the conditional probability formula:
$\[ P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{1}{13}}{\frac{3}{13}} = \frac{1}{3} \]$

Thus, the probability of drawing a King given that the card drawn is a face card is $\( \frac{1}{3} \)$.

### 11. Profuct Rule (for Independent Events)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/ab58e32c-0aa3-44ab-92c1-ea91a7fa2415)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/2495e6dc-551e-46e6-ba8d-8f05ceae1ea3)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/909dfd0b-f5d9-43b2-8e18-c80720f1af34)

![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/41f29c7d-bd81-4275-8524-741d10e644eb)

### 12. Bayes' Theorem

Bayes' Theorem provides a way to update our beliefs about the probability of an event when new evidence becomes available. It is expressed as:

$\[ P(A|B) = \frac{P(B|A) \times P(A)}{P(B)} \]$

Where:
- $\( P(A|B) \)$ is the posterior probability of event A given evidence B.
- $\( P(B|A) \)$ is the likelihood of evidence B given that A is true.
- $\( P(A) \)$ is the prior probability of event A.
- $\( P(B) \)$ is the probability of evidence B.

#### 12.1 Bayes' Theorem - Prior and Posterior

Bayes' Theorem allows us to update our prior beliefs (prior probability) with new evidence to obtain our posterior beliefs (posterior probability). This process is important in many fields, including machine learning, where it is used for tasks like classification and regression.

#### Example:

Suppose we have a medical test for a rare disease that affects 1 in 10,000 people. The test is 99% accurate (i.e., it correctly identifies a person with the disease 99% of the time) and has a false positive rate of 5% (i.e., it incorrectly identifies a person without the disease as positive 5% of the time). 

If a person tests positive, what is the probability that they actually have the disease?

- Let A be the event that a person has the disease.
- Let B be the event that a person tests positive.
Given:
- $\( P(A) = \frac{1}{10,000} \)$ (prior probability of having the disease)
- $\( P(B|A) = 0.99 \)$ (likelihood of testing positive given that the person has the disease)
- $\( P(B|A') = 0.05 \)$ (likelihood of testing positive given that the person does not have the disease, i.e., false positive rate)

Using Bayes' Theorem:
$\[ P(A|B) = \frac{P(B|A) \times P(A)}{P(B)} \]$

$\[ P(B) = P(B|A) \times P(A) + P(B|A') \times P(A') \]$
$\[ P(B) = (0.99 \times \frac{1}{10,000}) + (0.05 \times \frac{9,999}{10,000}) \]$
$\[ P(B) \approx 0.0504 \]$

$\[ P(A|B) = \frac{0.99 \times \frac{1}{10,000}}{0.0504} \]$
$\[ P(A|B) \approx 0.0196 \]$

Thus, the probability that a person actually has the disease given that they tested positive is approximately 0.0196.


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/35588f31-23a1-46dc-b20d-5f773d3da508)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/56d0ce4b-68d4-447f-b178-466ec996e888)


### 13. Bayes' Theorem - Naive Bayes Model

In machine learning, the Naive Bayes model is a probabilistic classification model based on Bayes' Theorem with the ***"naive" assumption of independence among features.*** Despite its simplicity, Naive Bayes often performs well in practice and is widely used for text classification, spam filtering, and other tasks.

The Naive Bayes classifier predicts the class label of a given instance by calculating the posterior probability of each class given the feature values and selecting the class with the highest probability.

If we have features $\( x_1, x_2, ..., x_n \)$, the class with the highest posterior probability given the features can be calculated as:
![Screenshot 2024-04-08 at 11 11 25 PM](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/a79786e3-9116-48ea-8087-fe758d89a939)

Where:
- $\( \hat{y} \)$ is the predicted class label.
- $\( P(y) \)$ is the prior probability of class $\( y \)$.
- $\( P(x_i|y) \)$ is the likelihood of feature $\( x_i \)$ given class $\( y \)$.

#### Example:

Suppose we have a dataset of emails labeled as spam or not spam, with features representing word frequencies. To classify a new email as spam or not spam using Naive Bayes, we calculate the posterior probability of each class given the word frequencies in the email and select the class with the highest probability.

Given a new email with word frequencies $\( x_1, x_2, ..., x_n \)$, we calculate:

$\[ P(\text{spam}|x_1, x_2, ..., x_n) = \frac{P(\text{spam}) \times \prod_{i=1}^{n} P(x_i|\text{spam})}{P(x_1, x_2, ..., x_n)} \]$

$\[ P(\text{not spam}|x_1, x_2, ..., x_n) = \frac{P(\text{not spam}) \times \prod_{i=1}^{n} P(x_i|\text{not spam})}{P(x_1, x_2, ..., x_n)} \]$

We select the class with the highest posterior probability as the predicted class label for the email.

## Comparison of Bayes' Theorem and Naive Bayes

| Feature                 | Bayes' Theorem                                         | Naive Bayes                                                |
|-------------------------|----------------------------------------------------------|--------------------------------------------------------------|
| Purpose                 | Calculate probability of a hypothesis given evidence     | Classify data points into categories                        |
| Formula                 | Uses Bayes' theorem for classification formula   | Uses Bayes' theorem for classification                     |
| Assumptions             | No assumptions about independence                        | Assumes features are independent given the class label        |
| Complexity              | More complex, can handle dependencies                   | Simpler, computationally efficient                             |
| Applications             | Wider range, including spam filtering, medical diagnosis | Primarily classification tasks, often with text or categorical data |


#### 13.1 Naive Bayes Classifier:
Despite the naive assumption, Naive Bayes is a surprisingly effective classification algorithm. It works by:
1.	Learning the Probability Distribution: It learns the probability distribution of each feature for each class label.
2.	Classification: When presented with a new data point (email), it calculates the probability of each class label given the values of the features in that data point. It then predicts the class with the highest probability.

##### 14.2 Benefits of Naive Bayes:
- Simplicity: It's a relatively simple algorithm to understand and implement.
- Efficiency: It requires less training data compared to some other algorithms.
- Effectiveness: Despite the naive assumption, it can perform well in many real-world classification tasks.

##### 11.3 Limitations of Naive Bayes:
- Feature Independence Assumption: The violation of the independence assumption can affect the accuracy of the classifier.
- Naïve to Feature Relationships: It may not capture complex relationships between features.


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/792111e4-267a-46db-876c-c3d8faba594e)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/32e2abdc-bbee-42b2-800e-d8f6bdaec460)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/b17bb2ca-1837-410c-9737-a38957a8e0a6)


![image](https://github.com/nehakardam/Probability-Statistics-for-Machine-Learning-/assets/70997776/7dc6a08e-db8d-40df-9083-57e8b84696e6)



#### Reference: Pictures taken from  Probability & Statistics for Machine Learning & Data Science course on Coursera.
