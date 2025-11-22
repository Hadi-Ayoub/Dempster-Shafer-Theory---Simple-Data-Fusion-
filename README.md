# Data Fusion with Dempster-Shafer Theory

A Python implementation of Dempster-Shafer theory for combining evidence from multiple sensors in a grid-based environment.

## Overview

This project demonstrates the practical application of Dempster-Shafer theory to fuse information from different sensors monitoring a grid area. The system helps determine the most likely location of a target by combining uncertain evidence from various sources.

## Project Structure

- **bpaGrid.py**: Core module containing:
  - `bpa` class: Represents Basic Probability Assignments
  - `CapteurCol`, `CapteurLigne`: Simple column and line sensors
  - `CapteurColFull`, `CapteurLigneFull`: Advanced sensors with margin parameters
  - Grid utilities and visualization functions

- **fusion.ipynb**: Jupyter notebook with implementation examples and tests

## Core Concepts

### Basic Probability Assignment (BPA)
A BPA represents uncertain evidence as a set of focal elements (grid areas) with associated probability masses.

### Grid Representation
The system uses 2D boolean arrays to represent grid areas, where:
- `True` indicates the cell is included in the area
- `False` indicates the cell is excluded

### Sensor Models
- **Column Sensor**: Detects targets in a specific column with uncertainty
- **Line Sensor**: Detects targets in a specific row with uncertainty
- Each sensor returns a BPA with focal elements and their probabilities

## Key Functions

### Evidence Combination
```python
fusion(m1, m2)  # Combines two BPAs using Dempster's rule
