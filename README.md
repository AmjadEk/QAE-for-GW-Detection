# Quantum Autoencoder for Gravitational Wave Detection in LIGO Time Series

This project explores the application of **Quantum Autoencoders (QAE)** for detecting gravitational waves within **LIGO time series data**. It tests two different variational circuits adapted from two research papers. The second variational quantum circuit achieved an accuracy of 88% in detecting gravitational waves when they were present in the sample, and 92% in recognizing samples without gravitational waves as such. By training the 

## Table of Contents
- [Introduction](#introduction)
- [Methodology](#methodology)
- [Dataset](#dataset)


## Introduction
I wanted to explore the possibility of using quantum machine learning principles for anomaly-detection by applying quantum autoencoders. They aim to compress high-dimensional data in a manner retaining critical information, to be able to accurately reconstruct it using a decoder. By training the quantum autoencoder only on data where there are no gravitational waves, it should perform poorly in reconstructing data featuring gravitational waves : by measuring the reconstruction error and comparing it to a chosen threshold, it is possible to classify the samples and determine if gravitational waves are present.

## Methodology
1. **Data processing**: Importing the LIGO time series data, denoising and analyzing it.
2. **Feature selection**: Extracting relevant features and converting them to quantum data using angle embedding method
3. **Quantum Autoencoder Design**:
   - Adapting QAE architecture from research papers with Qiskit and configuring circuits for state preparation.
   - Training QAE to compress the time series data.
4. **Detection Analysis**:
   - Analyzing the QAE output to detect gravitational waves and compare the two QAE architectures used.
     
## Dataset
The project uses **publicly available LIGO time series data** available at gwosc.org. It uses a dataset of all the recorded major events (gravitational waves detections) of the LIGO experiment, as well as time series data accessed through an API.


