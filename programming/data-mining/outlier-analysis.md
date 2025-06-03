# Outlier Analysis

Data mining typically looks for general patterns, but can also identify abnormal
patterns or anomalous data points.

Anomalous data points can be errors, but are potentially significant events.

## Types

- Global (differs from entire data set)
- Contextual (differs from local context)
- Collective (group of points differ from local or global context)

## Challenges in detection

- Normal vs. abnormal (no clear definition, varies by application, noisy data)
- Efficiency (latency, scalability, adaptability)
- Interpretability (how to explain the results)

## Detection Methods

- Ground truth label (vetted cases of anomalous activity)

In real world setting you may use semi-supervised learning.

- Assumption of normal vs. abnormal (domain knowledge)

Can also generate "domain knowledge" using formal statistical models.

Identify "normal" with clustering and consider abnormal points using distance
and density measurements.

### Classification

#### Supervised

You need a "large" sample of vetted normal/abnormal classes. You likely will
have more than one class that is considered abnormal and potentially more than
one class that is considered normal.

Challenges:

- Class imbalance
- New patterns (ex: new type of security attack)

#### Unsupervised Clustering

Leverages the assumption of majority vs minority clusters to identify what is
anomalous. Typically have multiple clusters for normal and multiple clusters for
abnormal.

This approach is fairly general to different applications.
