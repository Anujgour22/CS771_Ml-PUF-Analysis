# CS771_ML-PUF-Analysis

## Overview

This project addresses two problems related to Physical Unclonable Functions (PUFs) as part of the CS771 course group assignment:

- **Problem 1.1:** Predicting responses of a Multi-Level PUF (ML-PUF) using linear models despite the XOR-based complexity introduced by the architecture.

- **Problem 1.2:** Recovering valid non-negative delay parameters from a given linear model of a 64-bit Arbiter PUF.

## Data Details

### Problem 1.1: ML-PUF Challenge-Response Data

- The ML-PUF dataset contains challenge-response pairs (CRPs) with 8-bit challenges and a single-bit response.
- The training set has 6400 CRPs; the test set has 1600 CRPs.
- Each row has 9 bits: the first 8 bits represent the challenge, and the last bit is the XORed final response (XOR of Response0 and Response1 from two arbiter PUFs).
- Your goal is to engineer a suitable feature vector from the 8-bit challenge that allows a linear model to accurately predict the final response.

### Problem 1.2: Arbiter PUF Delay Recovery Data

- Provided are 10 linear models, each represented by 65 real numbers (64 weights and 1 bias term).
- Each weight and bias lies between -1 and +1.
- The task is to find 256 non-negative delay parameters (pi, qi, ri, si for i=0 to 63) that reproduce the given linear model exactly.
- Multiple valid solutions exist; any valid set of non-negative delays is acceptable.

## How to Run

- The `solution.py` script loads and processes the data, trains models, performs predictions, and recovers delays.
- Run the script using Python 3:

```bash
python Project/solution.py



