---
type: concept
title: Financial Functions API
description: Core reference for the mathematical and functional API of numpy-financial, covering cash flow, interest rate, and investment analysis.
tags: [financial, numpy-financial, mathematics]
sources:
  - id: openwiki-source-23775c3de52f3ab95a13cb8b
    resource: repo://README.md
generated: { by: "openwiki/0.7.0", at: "2026-10-04T09:15:48.692Z" }
---

The `numpy-financial` library provides a set of standard financial functions implemented to operate on both scalar and array inputs, mirroring the functionality historically found in spreadsheet software.

## Core Financial Functions

The library exports the following primary financial functions:

*   **`fv`**: Calculates the future value of an investment based on periodic, constant payments and a constant interest rate.
*   **`pv`**: Calculates the present value of an investment.
*   **`pmt`**: Calculates the payment against a loan based on constant payments and a constant interest rate.
*   **`nper`**: Calculates the number of periods for an investment based on periodic, constant payments and a constant interest rate.
*   **`rate`**: Calculates the interest rate per period of an investment.
*   **`ipmt`**: Calculates the interest portion of a payment for a given period.
*   **`ppmt`**: Calculates the principal portion of a payment for a given period.
*   **`npv`**: Calculates the net present value of a cash flow series.
*   **`irr`**: Calculates the internal rate of return for a series of cash flows.
*   **`mirr`**: Calculates the modified internal rate of return for a series of cash flows.

## Data Input Patterns

`numpy-financial` functions are designed for flexibility in handling numeric inputs:

*   **Scalars**: Single floating-point values representing rates, cash flows, or time periods.
*   **Arrays**: NumPy arrays allow for vectorized financial calculations, enabling the simultaneous processing of multiple financial scenarios.
*   **Decimal**: Support for `decimal.Decimal` objects is provided to maintain high precision for sensitive financial arithmetic.

## Broadcasting

A key feature of these financial functions is their integration with NumPy's **broadcasting** rules. When inputs are provided as arrays of different shapes, or a mix of scalars and arrays, the functions automatically broadcast the inputs to a compatible shape. This allows users to perform bulk calculations—such as computing the future value for an array of interest rates against a scalar present value—without explicit looping.

In practice, this means that if you provide an array of rates, the output will be an array of the same shape containing the results for each rate.
