---
type: concept
title: Financial Functions API
description: Core reference for the mathematical and functional API of numpy-financial, covering cash flow, interest rate, and investment analysis.
tags: [financial, numpy-financial, mathematics]
verified:
  - by: openwiki/0.7.0
    at: 2026-10-04T09:49:17.521Z
sources:
  - id: openwiki-source-23775c3de52f3ab95a13cb8b
    resource: repo://README.md
generated: { by: "openwiki/0.7.0", at: "2026-10-04T09:49:17.521Z" }
---

The `numpy-financial` library (importable as `numpy_financial`) provides a collection of elementary financial functions designed as a standalone replacement for the deprecated financial routines previously included in NumPy.

## Design Philosophy

The library is designed with two primary objectives:
1. **Spreadsheet Compatibility**: The functions are modeled after common spreadsheet financial formulas (e.g., those found in Excel or Google Sheets), ensuring that the API is intuitive for users familiar with traditional financial modeling.
2. **NumPy Integration**: The functions are implemented as universal functions (ufuncs) or behave similarly to them, supporting NumPy's core strengths: broadcasting, vectorized operations, and efficient handling of multi-dimensional arrays.

## Core Financial Functions

The library exports the following primary financial functions:

*   **`fv`**: Calculates the future value of an investment.
*   **`pv`**: Calculates the present value of an investment.
*   **`pmt`**: Calculates the periodic payment against a loan or investment.
*   **`nper`**: Calculates the number of periods for an investment.
*   **`rate`**: Calculates the periodic interest rate.
*   **`ipmt`**: Calculates the interest portion of a payment for a given period.
*   **`ppmt`**: Calculates the principal portion of a payment for a given period.
*   **`npv`**: Calculates the net present value of a cash flow series.
*   **`irr`**: Calculates the internal rate of return for a series of cash flows.
*   **`mirr`**: Calculates the modified internal rate of return.

## Data Input and Vectorization

`numpy-financial` functions are engineered for flexibility in how they handle numeric data:

*   **Input Types**: The functions support scalars, NumPy arrays, and `decimal.Decimal` objects, allowing users to choose the appropriate data type for their precision and performance needs.
*   **Vectorization**: By supporting array inputs, the library enables vectorized financial calculations. Instead of manually looping over datasets, users can pass arrays to these functions to perform bulk computations across multiple financial scenarios simultaneously.
*   **Broadcasting**: The functions leverage NumPy broadcasting rules. If input parameters have different, yet compatible, shapes, the library automatically expands them, allowing for efficient combinations of scalar inputs with arrays of varying dimensions.
