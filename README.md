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

### Normal Distibution

In data science, one curve seems to appear almost everywhere — the Normal Distribution, also known as the Gaussian Distribution or the Bell Curve. 

It’s called normal because so many natural, social, and experimental phenomena follow this shape — heights, exam scores, blood pressure, errors in measurements, even IQs.

***So what is it?*** Normal distribution is a continuous probability distribution shaped like a bell curve — symmetrical around its mean. This curve is highest at the mean, and it tapers off symmetrically on both sides.

The shape depends only on two things: 

A normal distribution is centered around its mean, so the distribution is not skewed. This doesn't mean that normal distributions cannot appear in different shapes and forms. How exactly the distribution behaves depends on the 2 key parameters, as specified before:

- ***μ (mean)*** shifts the curve left or right and ***σ (standard deviation)*** controls how wide or narrow it is.(spread/width) (refer to image above)

All of these distributions(normal.plt) have the following properties in common:

- They are symmetric around the mean,
- They have relatively higher densities of values at the center of the distribution and relatively lower density in the tails

### Some More Characteristics of the Normal Distribution

- Normal distributions are symmetric around their mean
- The mean, median, and mode of a normal distribution are equal
- The area under the bell curve is equal to 1.0
- Normal distributions are denser in the center and less dense in the tails
- Normal distributions are defined by two parameters, the mean (μ) and the standard deviation (σ).
- Around 68% of the area of a normal distribution is within one standard deviation of the mean
- Approximately 95% of the area of a normal distribution is within two standard deviations of the mean

The last two characteristics refer to a rule called the ***empirical rule*** :- Refer to image(normal_sd)

68% values of a normal distribution are within 1 standard deviation of the mean, 95% within 2 standard deviations and 99.7 % within 3 standard deviations. Normally distributed data is considered ideal for analysis due to this simplicity of description. Values in the extreme of tails (more than 3 standard deviations) can be considered "interesting events" as their probability of occurrence is very low. In other cases, you'll consider them as outliers due to noise or error of measurement. It all depends on your analysis question

### Managing Uncertainty When Reporting Numbers(Inferential statistics)

Managing numbers in inferential statistics involves a process of estimation and hypothesis testing, built upon key foundational concepts:

1. Sampling: Since analyzing an entire population is often impossible, you select a sample, a representative subset of the population. The quality of your inference is directly tied to how well your sample represents the population (e.g., using random sampling).

2. Estimation: Using sample statistics (like the sample mean, $\bar{x}$) to estimate unknown population parameters (like the population mean, $\mu$).

- Point Estimate: A single best guess (e.g., the sample mean).
- Interval Estimate (Confidence Interval): A range of values likely to contain the true population parameter.

3. Hypothesis Testing: A formal procedure to check if a claim (hypothesis) about a population parameter is supported by the sample data. This often involves calculating a test statistic (like a $z$-score or $t$-score) and a p-value to decide whether to reject or fail to reject the null hypothesis ($H_0$).

### Central Limit THeorem

it's a key confidence booster when doing inferential statistics. It states that

When you take many random samples from a population and calculate their means, the distribution of those sample means will be approximately normal (bell-shaped) — even if the population itself is not normal — as long as the sample size is large enough.

The population can be weird or skewed. But the averages of many samples will form a normal curve.
That’s why we can use the normal distribution to make inferences and build confidence intervals.

### Sampling Error

Sampling error quantifies the natural variability that arises when you use a sample instead of the whole population. It's the difference between a sample statistic  and the true population parameter. This error occurs because a sample is not a perfect emulation of the population.

The standard deviation of the sampling distribution of the mean is called the Standard Error (SE). The CLT provides the formula for the Standard Error:$$SE = \frac{\sigma}{\sqrt{n}}$$where $\sigma$ is the population standard deviation and $n$ is the sample size.

The CLT shows that as the sample size ($n$) increases, the Standard Error ($SE$) decreases. This means the sampling distribution gets narrower (less spread), and the sample mean becomes a more precise estimate of the population mean, thereby reducing sampling error.


### Confidence Interval (CI)

A Confidence Interval (CI) is an estimated range of values which is likely to include the true population parameter, with a specified degree of certainty (the confidence level).

The $SE$ (derived from the CLT) is used to calculate the Margin of Error. For a 95% CI, if you repeated the sampling process many times, 95% of the constructed CIs would contain the true population mean.

### T-distribution

When you have a small sample (like 30 or 50 people) and don’t know the population’s true standard deviation,
you use the t-distribution instead of the normal (z) distribution.

The t-distribution has wider tails, meaning it gives you a slightly wider confidence interval to account for more uncertainty.

As your sample gets larger, the t-distribution becomes almost the same as the normal one