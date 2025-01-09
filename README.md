# Kernel Density Estimation (KDE) for Signal Alignment

This repository contains a series of R scripts that demonstrate the application of **Kernel Density Estimation (KDE)** to analyze and align two signals, `true.signal` and `distorted.signal`. The goal is to compare the differences between the two signals and find the optimal transformations to minimize those differences. The methods can be used in various real-world scenarios, such as finance, sports data analysis, and signal processing.

## Overview

### 1. **Kernel Density Estimation (KDE)**
   - KDE is a non-parametric way to estimate the probability density function of a continuous random variable. In this project, we apply 2D KDE to visualize the difference between two signals and calculate the maximum difference between their estimated densities.

### 2. **Loss Function for Signal Comparison**
   - The project involves the calculation of a loss function that measures the sum of squared differences between the KDE of `true.signal` and `distorted.signal`. This helps in quantifying how well the distorted signal matches the true signal.

### 3. **Shifting and Transformation**
   - The code explores methods for shifting the `distorted.signal` along the x and y axes to minimize the difference from the `true.signal`. The objective is to find the optimal shift values that reduce the discrepancy between the signals.
   - Additionally, affine transformations are applied to further optimize alignment.

## Repository Structure

- **`data.RData`**: The dataset containing `true.signal` and `distorted.signal`.
- **`main.R`**: The main script where KDE is computed, loss functions are defined, and optimal shifts are calculated.
- **`README.md`**: Documentation for the repository.
- **`LICENSE`**: The repository's license file.

## Installation

To run the code, you'll need to have R installed on your machine. You can download R from [here](https://cran.r-project.org/).

### Install Dependencies
```R
install.packages("KernSmooth")
