### Conditional Probability

Conditional probability is the probability of an event occurring given that another event has already occurred. It is denoted by \$( P(A|B)$ \), the probability of event A given event B. The formula for conditional probability is given by:

\$[ P(A|B) = \frac{P(A \cap B)}{P(B)} $\]

Where:
- \$( P(A \cap B) \)$ is the probability of both events A and B occurring.
- \$( P(B) \)$ is the probability of event B occurring.

#### Example:

Consider a standard deck of 52 playing cards. What is the probability of drawing a King given that the card drawn is a face card?

- Event A: Drawing a King.
- Event B: Drawing a face card.

There are 12 face cards in a standard deck (4 Kings included). So, $\( P(B) = \frac{12}{52} = \frac{3}{13} \)$.
Among those 12 face cards, there are 4 Kings. So, $\( P(A \cap B) = \frac{4}{52} = \frac{1}{13} \)$.
Using the conditional probability formula:
$\[ P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{1}{13}}{\frac{3}{13}} = \frac{1}{3} \]$

Thus, the probability of drawing a King given that the card drawn is a face card is $\( \frac{1}{3} \)$.

### Bayes' Theorem

Bayes' Theorem provides a way to update our beliefs about the probability of an event when new evidence becomes available. It is expressed as:

$\[ P(A|B) = \frac{P(B|A) \times P(A)}{P(B)} \]$

Where:
- $\( P(A|B) \)$ is the posterior probability of event A given evidence B.
- $\( P(B|A) \)$ is the likelihood of evidence B given that A is true.
- $\( P(A) \)$ is the prior probability of event A.
- $\( P(B) \)$ is the probability of evidence B.

### Bayes' Theorem - Prior and Posterior

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

### Bayes' Theorem - Naive Bayes Model

In machine learning, the Naive Bayes model is a probabilistic classification model based on Bayes' Theorem with the "naive" assumption of independence among features. Despite its simplicity, Naive Bayes often performs well in practice and is widely used for text classification, spam filtering, and other tasks.

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

