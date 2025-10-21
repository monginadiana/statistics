## Descriptive statistics

Descriptive statistics is used to summarize and describe the main features of a dataset. These help us understand what our data looks like.

#### Examples

**Mean (Average)**: The sum of all values divided by the number of values. ***Example***: The average test score of 5 students is 
(80+70+90+100+60)/5=80.

***Median***: The middle value when all data points are arranged in order. ***Example***: For scores [60, 70, 80, 90, 100], the median is 80.

***Variance***: Measures how far data points spread out from the mean. ***A small variance*** = data points are close to the mean; ***a large variance***= data points are more spread out.

***Standard Deviation (SD)***: The square root of variance; it gives spread in the same units as the data ***Example***: 

## Inferential statisticss

In real-world data science, we rarely have data for the entire population.
Instead, we have a sample, and we want to infer what’s true about the population from that sample. That’s where inferential statistics come in — we use probability to make educated guesses (inferences) about the population, such as estimating averages, testing hypotheses, or predicting outcomes.

To make these inferences, we need to understand how data is distributed — that is, how often different values occur.

### Discreate / Continious Data(the basis)| Type               

Discrete Data is countable values  : e.g Number of customers in shop, Number of students in a class. **(PMF)Probablity mass Function**(It gives the probability of each possible value.)

*** Example ***  A dice roll has a probability of rolling 6 times
The PMF gives the probability of each side (1–6):
P(X = 1) = P(X = 2) = ... = P(X = 6) = 1/6.

Continious Data is Measurable, can take any value within a range e.g Heights, weights, time

**Probability Density Function (PDF)**

Since continuous data can take infinitely many values, the probability of one exact value is 0. Instead, the area under the curve between two points represents the probability of the variable falling in that range. 

**Example** If people’s heights follow a Normal Distribution, then the ***PDF*** can tell us the probability that someone’s height is between 165 cm and 175 cm.

### Cumulative Distribution Function (CDF)
Used for both discrete and continuous variables. It tells us the probability that a random variable is less than or equal to a certain value.

*** Example ***:
If X is the height of a person, the **CDF** can tell us the probability that someone is shorter than 170 cm.

## Additional 

### Common Distributions

- Bernoulli Distribution (Discrete):Has only two outcomes — success (1) or failure (0).
**Example: Flipping a coin (Heads = 1, Tails = 0).**

- Binomial Distribution (Discrete):Repeated Bernoulli trials.
**Example: Number of heads in 10 coin flips.**

- The Poisson distribution is a discrete probability distribution used to model the number of times an event occurs in a fixed interval of time, space, distance, or area, given that he events occur independently, The average rate (λ) of occurrence is constant, Two events cannot happen at exactly the same instant.

*** Example: The number of calls received by a call center per day.**

- Normal Distribution (Continuous): A bell-shaped curve, symmetric around the mean.
**Example: Heights, IQ scores, and exam marks often follow this pattern.**

### Skewness and Kurtosis
Skewness measures how asymmetric a distribution is. Positive skew = tail on the right Negative skew = tail on the left

Kurtosis measures how ***peaked*** or ***flat*** the distribution is compared to a normal curve.

### Sampling?

In the real world, we rarely have access to data about an entire population.

Think about these scenarios:

- Measuring the average income of people in Kenya.

- Finding the average age of Netflix users.

You can’t measure everyone. So instead, you collect a sample — a smaller subset — and use it to make inferences about the larger population.

A census studies every member of a population.
A sample studies only a few, and uses those to estimate what’s true for all.

### Sampling Notation
For population : Number in Population (N), Mean (μ (Mu)) and SD is (σ (Sigma))
For sample : Number in Sample (n), Mean (xˉ (X-bar)) and SD is (sigma (s))


Statistical measures such as measures of central tendency (e.g. mean, median) and measures of spread (e.g. absolute deviation, standard deviation) are used to describe the distribution of a given collection of data points. We also use visualizations such as histograms and box plots to understand the shape of distributions.
These descriptive statistics can apply to populations or samples. When they are applied to populations they are called population statistics, and when they are applied to samples they are called point estimates.


PMD 

A Probability Mass Function (PMF) gives the probability that a discrete random variable takes on a specific value.
It’s written as:

f(x)=P(X=x)

That means — for every possible value of 𝑋X, we assign the probability that 𝑋 X equals that value.