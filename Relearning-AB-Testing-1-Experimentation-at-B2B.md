# Relearning A/B Testing, 1: Experimentation at B2B

This is a note and take away which came from after watched the wonderful talk [Unlocking A/B Testing for B2B - YouTube](https://www.youtube.com/watch?v=f4seZseaeSM&list=LL&index=3&t=49s) by Timothy Chan @Statsig at Data Council.

<img width="485" height="293" alt="image" src="https://github.com/user-attachments/assets/b019a8a1-abec-4f4f-b040-61e033e163de" />


## 0. Experimentation is as valuable and important in B2B as it is in B2C.

Large-scale A/B testing in the B2C internet industry is a privilege of having massive traffic and data.

In the pharmaceutical industry, researchers have relied on hundreds (or even just dozens) of samples  to find statistical evidence for almost a century.

In that light, B2B can certainly conduct scientific and effective experiments, and uncover valuable insights as well.


## 1. Challenges at B2B Testing

B2B experiments face a complex set of unique challenges. 

These challenges mainly come from the nature of B2B transactions, the fat-tailed distribution of companies, and the slow movement of business

### Organizational-level randomization

In B2B SaaS, we need to **randomize by organization** rather than by individual user level.
Since coworkers collaborate and share screens, assigning different versions to people in the same office leads to 'spillover' (group contamination) and a mismatch between experimental and analytical units.

And for non-SaaS B2B, data is typically only available at the account level.

<img width="372" height="167" alt="image" src="https://github.com/user-attachments/assets/3572fedb-7959-4fc7-98d1-663ad476522b" />

**Both scenarios inevitably lead to small sample size experiments, which further presents two challenges following: *group imbalance and underpowered experiments.***

### Imbalanced randomization

In small-sample B2B experiments, simple random assignment is highly prone to imbalance. For example, there  is a high chance of assigning the only two super-large ‘whale’ accounts to the same group, creating a massive data skew.

<img width="518" height="264" alt="image" src="https://github.com/user-attachments/assets/37448e8a-c81d-42b1-bad2-dd710420955d" />


To counter this, stratified sampling is recommended. By **grouping accounts by company size/revenue or industry before assignment**, we ensure that the experimental arms are truly comparable.

<img width="518" height="264" alt="image" src="https://github.com/user-attachments/assets/228af113-247b-4f5b-905a-ad24b3cd7d69" />


### Statistical underpowering

We may recall the positive relationship between statistical power and sample size. 

However, given the limited sample size in B2B, it becomes harder to detect even meaningful improvements. The experiment may end up 'underpowered,' meaning we **might miss a successful feature** just because the data is too “noisy“.

In such cases, it is essential to return to basics, prioritizing **Power Analysis** (covered next), and **advanced methods like CUPED** could be helpful (covered in the following section).
By reducing metric variance (noise), CUPED allows us to achieve statistical power even when our sample size is limited.


### Low-Sensitivity metrics: Sparse and Lagging

### Right-skewed distribution: Fat-tailed



## 2. Remember the Experimentation Fundamentals

### Good metrics

Select the right metrics:

* **Start with operational metrics**: Use basics like Button CTR as a starting point. It helps verify that the experiment is set up correctly and users are actually interacting with the new features.
* **Expand to business and North Star metrics**: Further move toward core business metrics. It’s better to select a balanced set of metrics across the entire business chain.
* **Use proxy metrics for sensitivity**: Sensitive proxy metrics provide faster feedback. Things like Feature Activation Rate / Time to First Value rather than lagging metrics like Retention / Renewal Rate.
* **Allow for "Directional" checks**: If the core metric (like revenue) hasn't reached significance, look at whether it directionally aligns with proxy metrics to confirm we're on the right track.


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

<img width="609" height="307" alt="image" src="https://github.com/user-attachments/assets/5601e6ea-0233-47c8-b6a2-27260e9dab13" />

Consequently, CUPED helps us decrease the required sample size by reducing variance.

There are also other techniques available to reduce variance.

### Bayes

Using a Bayesian perspective to avoid the trade-off debate between significance levels and statistical power is a viable choice that applies well to B2B contexts.

To learn more about Bayesian Experimentation, catch this other talk [Going Bayes: Shifting our Testing Methods to Reflect our Priorities](https://youtu.be/CdPHfj0bHcQ?si=SppZ3Z5LvD11u6tG) from the Data Council.

### Quasi-experimentation

* Geo-Lift

* Synthetic control

### Heterogeneous reporting
