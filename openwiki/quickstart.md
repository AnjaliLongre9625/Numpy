---
type: concept
title: Quickstart
description: A starting guide for new contributors to navigate the repository, understand the architecture, and effectively use the financial functions library.
tags: [introduction, navigation, architecture]
verified:
  - by: openwiki/0.7.2
    at: 2026-10-23T13:03:36.359Z
sources:
  - id: openwiki-source-4e5f802aed16234a2248d448
    resource: repo://numpy_financial/_cfinancial.pyx
  - id: openwiki-source-29546a0fa3bd3395fbde36d1
    resource: repo://numpy_financial/_financial.py
generated: { by: "openwiki/0.7.2", at: "2026-10-23T13:03:36.359Z" }
---

# Quickstart

Welcome to `numpy-financial`, a library providing a collection of spreadsheet-style financial functions. This library is designed to perform common financial calculations while maintaining compatibility with NumPy's broadcasting rules, allowing operations on both scalar and array inputs.

## Repository Overview

The core logic of the library resides in the `numpy_financial/` directory:

- `numpy_financial/_financial.py`: The main entry point containing the public financial functions (such as `fv`, `pmt`, `pv`, `irr`, etc.) and core logic.
- `numpy_financial/_cfinancial.pyx`: A Cython module containing performance-critical financial implementations, which are imported and exposed by `_financial.py`.
- `numpy_financial/tests/`: Comprehensive test suites verifying the accuracy of financial calculations.

## Architectural Structure

The library is designed to mimic standard spreadsheet behaviors while providing robust numerical support:

- **Broadcasting**: Functions are built to leverage NumPy's broadcasting capabilities, allowing them to handle various input shapes.
- **Data Types**: Supports both `float` and `decimal.Decimal` types, enabling precision-sensitive calculations.
- **Error Handling**: Custom exceptions like `NoRealSolutionError` and `IterationsExceededError` are defined to handle edge cases in numerical solvers.

## Documentation Navigation

To better understand the library, explore the following documentation pages:

- [Financial Functions](architecture/financial-functions.md): In-depth details on the mathematical core and function signatures.
- [Implementation Details](architecture/implementation-details.md): Insights into how broadcasting, input validation, and performance are handled, including the integration between `_financial.py` and `_cfinancial.pyx`.
- [Testing Strategy](testing/testing-strategy.md): Guidelines for writing tests and verifying the integrity of the financial library.

## Getting Started

1. **Install dependencies**: Ensure you have the necessary build environment and `numpy` installed.
2. **Explore the codebase**: Start by reviewing `numpy_financial/_financial.py` to understand how public functions are exposed and how they delegate performance-critical operations to `numpy_financial/_cfinancial.pyx`.
3. **Run tests**: Execute the test suite in `numpy_financial/tests/` to verify your environment and ensure stability.

```bash
# Example command to run tests
pytest numpy_financial/tests/
```
