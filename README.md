# Language Models for Text Generation and Prediction

# Overview

This project implements and analyzes various language models, including a Neural Network Language Model, an RNN-based Language Model, and a Transformer Decoder-based Language Model, to evaluate their effectiveness in predicting the next word in a sequence. The performance is measured using Perplexity, a metric for assessing the predictive accuracy of language models.

# Models Implemented

# Neural Network Language Model:

Uses a fixed 5-gram context for predictions.

Limited ability to capture long-range dependencies, resulting in higher perplexity (287.54).

# RNN-based Language Model:

Captures sequential dependencies better than a 5-gram model.

Handles variable-length contexts dynamically.

Perplexity reduced to 226.60, but struggles with vanishing gradients on long sequences.

# Transformer Decoder-based Language Model:

Employs self-attention to effectively model long-range dependencies.

Uses positional encoding and parallel processing for superior performance.

Achieved the lowest perplexity (38.14), demonstrating high accuracy and scalability.

# Key Observations

# Perplexity Analysis

Neural Network Model: High perplexity due to limited context and simpler architecture.

RNN Model: Improved perplexity but still faces challenges with long sequences.

Transformer Model: Significantly lower perplexity, showcasing its ability to model complex language structures.

# Hyperparameter Insights

# Hidden Dimensions:

Larger dimensions (>200) improved perplexity on both training and test sets.

Non-linear relationship observed with worst performance around dimension size ~200.

# Optimizer:

Adam outperformed SGD, achieving much lower perplexity.

SGD struggled with generalization, leading to higher perplexity values.

# Dropout Rate:

Lower dropout rates (around 0.1) resulted in the best performance.

Increasing dropout led to higher perplexity on both training and test sets.

# Conclusion

Transformer Decoder-based Model demonstrated the best performance with the lowest perplexity, effectively capturing long-range dependencies and handling complex language patterns.

Optimizing hyperparameters such as hidden dimensions, optimizer, and dropout rates significantly impacts model performance.
