# Design and Statistical Evaluation of Hybrid Pseudorandom Number Generators via Algorithm Combination Techniques

A Python framework for constructing, generating, and evaluating hybrid pseudorandom number generators (PRNGs).

This repository accompanies the bachelor's thesis:

> **Design and Evaluation of Pseudorandom Number Generators**

The project implements several widely used PRNGs, multiple hybridization algorithms, and a statistical evaluation framework for comparing the resulting generators with respect to both randomness quality and computational performance.

---

## Features

- Implementation of multiple base PRNGs
  - Mersenne Twister (MT19937)
  - XorShift32
  - PCG64

- Implementation of hybridization techniques
  - Sequential Chaining
  - XOR Combination
  - Weighted Mixing
  - Conditional Interleaving

- Automatic generation of every PRNG/hybridization combination

- Statistical evaluation including
  - Mean
  - Median
  - Variance
  - Standard deviation
  - Minimum and maximum
  - Shannon entropy
  - Chi-squared goodness-of-fit test
  - Kolmogorov–Smirnov test
  - Autocorrelation
  - Bit frequency
  - Bit autocorrelation
  - Monte Carlo π approximation

- Performance evaluation
  - Generation time
  - Time per generated number
  - Throughput

- Automatic generation of
  - CSV result tables
  - Figures
  - Saved random sequences

---

## Implemented PRNGs

| Generator | Description |
|-----------|-------------|
| MT19937 | Mersenne Twister implementation provided by NumPy |
| XorShift32 | Software implementation of Marsaglia's XorShift32 |
| PCG64 | NumPy implementation of the PCG family |

---

## Implemented Hybridization Algorithms

### Sequential Chaining

Uses the output of one PRNG to seed another generator before producing the sequence.

### XOR Combination

Combines corresponding outputs of two generators using the bitwise XOR operation.

### Weighted Mixing

Computes a weighted arithmetic combination of two generator outputs using an adjustable parameter α.

### Conditional Interleaving

Selects one of two generated values according to a predefined parity rule.

---

## Evaluation Methodology

Each generated sequence is evaluated using statistical metrics measuring:

- distribution uniformity
- central tendency
- dispersion
- entropy
- goodness-of-fit
- correlation
- bit-level randomness
- computational efficiency

The framework intentionally evaluates individual statistical properties rather than relying solely on external randomness test suites.

---

## Generated Data

The framework automatically stores

- generated random sequences
- statistical summaries
- grouped comparisons
- generation times
- visualizations

---

## Purpose

The objective of this project is not to design a new pseudorandom number generator.

Instead, it provides a reproducible framework for studying how different hybridization techniques influence the statistical properties and computational performance of existing PRNGs.

---

## Limitations

The framework currently includes only the selected generators and hybridization methods investigated in the accompanying thesis.

The evaluation is based on statistical metrics implemented within the project. Comprehensive external test suites (e.g. NIST STS, Dieharder, or TestU01) are not integrated into the framework.

---

## Author

Mikhail Ermakov

Bachelor's Thesis

University of Europe for Applied Sciences

Germany, Potsdam, Innovation Campus

Business Department, Software Engineering

June 2026
