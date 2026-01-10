# Relearning A/B Testing, 1: Experimentation at B2B

This is a note and take away which came from after watched the wonderful talk [Unlocking A/B Testing for B2B - YouTube](https://www.youtube.com/watch?v=f4seZseaeSM&list=LL&index=3&t=49s) by Timothy Chan @Statsig at Data Council.

<img width="485" height="293" alt="image" src="https://github.com/user-attachments/assets/b019a8a1-abec-4f4f-b040-61e033e163de" />


## 0. Experimentation is as valuable and important in B2B as it is in B2C.

## 1. Organizational-level randomization

   Smaller sample sizes

   Group matching

   right-skewed metrics

   sparse and lagging metrics

## 2. Remember the Experimentation Fundamentals

### Good metrics

It is better to use fundamental feature metrics, leading metrics, or upper-funnel metrics instead of lagging indicators like ARR or retention rate.

### Power analysis

Power analysis is crucial and should not be overlooked in experimental design.
We use power analysis to help estimate effect sizes and determine the required sample size.

There are several excellent tools for sample size calculation; inspired by them, I generated a [chart](https://github.com/bchaoss/Power-Analysis-viz/tree/main) to visualize the relationship between statistical power, sample size, and other metrics.

<img width="402.5" height="242.5" alt="image" src="https://github.com/user-attachments/assets/f4a3830d-e12c-46f3-943e-d436faebdc20" />

However, B2B has its own limitations regarding sample size, which may lead us to other approaches to increase statistical power, such as the variance reduction techniques discussed in the next section.

### Hypothesis

## 3. Advanced techniques

There are some advanced techniques that may be applied more effectively in B2B environments:

### Value of CUPED: Variance Reduction

CUPED might be more effective in B2B because B2B users/organizations exhibit more consistent behavior than B2C, making a linear relationship between pre-test and testing metrics more likely.

Consequently, CUPED helps us decrease the required sample size by reducing variance.

There are also other techniques available to reduce variance.

### Bayes

Using a Bayesian perspective to avoid the trade-off debate between significance levels and statistical power is a viable choice that applies well to B2B contexts.

### Stratified sampling

### Quasi-experimentation

* Geo-Lift

* Synthetic control

### Heterogeneous reporting
