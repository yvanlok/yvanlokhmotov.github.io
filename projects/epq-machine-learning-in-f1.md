---
layout: page
title: "EPQ F1 Predictive Model"
date: 2025-11-15
tags: [machine learning, EPQ, motorsport]
featured: true
summary: "Neural nets and TabNet for race prediction with structured data pipelines and full backtesting."
---

# EPQ F1 Predictive Model

## Overview

This project builds a predictive model for Formula 1 race finishing positions using structured data pipelines, feature engineering and modern machine learning methods. The aim is to test how far neural networks and TabNet can extract patterns from timing, telemetry and historical race information.

## Objectives

- Create a reproducible end to end workflow for F1 prediction
- Develop a clean dataset from raw race, timing and driver data
- Engineer features that capture qualifying performance, stint patterns, track behaviour and race context
- Train neural networks and TabNet models while preventing leakage
- Backtest the workflow to evaluate real world robustness

## Methods

- Data ingestion from timing, results and supplementary race sources
- Preprocessing with pandas to standardise and merge datasets
- Feature engineering including pace deltas, tyre stints, form metrics, driver and team variables and track characteristics
- Model training in PyTorch and TabNet with early stopping and cross validation
- Strict separation between training and target events to avoid leakage
- Backtesting using season by season roll forward evaluation

## Role

- Built the data preparation pipeline
- Designed and trained neural network and TabNet models
- Evaluated performance with multiple metrics and backtesting setups
- Documented the workflow for reproducibility

## Tech stack

Python, PyTorch, TabNet, pandas, NumPy, scikit learn

## Results

Metrics, learning curves and predictions will be added here when full evaluation is completed.
