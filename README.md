# FICO Score Quantization Project

## Project Overview

This project focuses on developing a generalized approach for quantizing FICO scores into predefined buckets to effectively represent credit risk data. The quantization aims to map FICO scores to a credit rating system, where a lower rating indicates a better credit score.

## Methods

Two primary quantization methods are used to determine the optimal bucket boundaries that best summarize the data:

### 1. Mean Squared Error (MSE) Minimization

This method approaches the problem as an approximation task, where the goal is to map all entries in a bucket to one representative value, minimizing the squared error within each bucket. This method is ideal for ensuring that each bucket accurately represents the FICO scores it contains by minimizing variance.

### 2. Log-Likelihood Maximization

This sophisticated method aims to maximize the log-likelihood function, which measures how well the distribution of defaults matches with the bucketed predictions of default probabilities. This function considers both the roughness of the discretization and the density of defaults within each bucket, enhancing the precision of the bucket definitions.

## Implementation

The implementation involves:
- Data analysis to understand the distribution of FICO scores and default rates.
- Application of clustering techniques for MSE Minimization.
- Use of dynamic programming for Log-Likelihood Maximization.
- Validation of the models to ensure effective predictive accuracy.
