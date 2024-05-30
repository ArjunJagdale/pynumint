# pynumint: A Numerical Integration Library

pynumint is a Python library for numerical integration methods.
pynumint offers a wide range of numerical integration methods, including trapezoidal rule, Simpson's rule, midpoint rule, Boole's rule, Romberg integration, Gauss-Legendre quadrature, Gauss-Chebyshev quadrature, Gauss-Laguerre quadrature, Gauss-Hermite quadrature, adaptive Simpson's rule, Monte Carlo integration, and double integrals. Users can choose the most suitable method based on the characteristics of the function and the desired level of accuracy.

## Installation

```bash
pip install pynumint


```

## Usage
```bash

from pynumint import trapezoidal_rule, simpsons_rule, midpoint_rule, booles_rule, romberg_integration, gauss_legendre_quadrature, gauss_chebyshev_quadrature, gauss_laguerre_quadrature, gauss_hermite_quadrature, adaptive_simpsons_rule, monte_carlo_integration, double_integral, simpsons_rule_with_error
import numpy as np

# Define your functions to be integrated
def f1(x):
    return x**2

def f2(x):
    return np.sin(x)

def f3(x):
    return np.exp(-x**2)

def f4(x, y):
    return x * y

# Define integration limits and number of intervals
a = 0
b = 10
n = 1000

# Example usage of numerical integration methods
result_trapezoidal = trapezoidal_rule(f1, a, b, n)
result_simpsons = simpsons_rule(f2, a, b, n)
result_midpoint = midpoint_rule(f3, a, b, n)
result_booles = booles_rule(f1, a, b, n)
result_romberg = romberg_integration(f2, a, b)
result_gauss_legendre = gauss_legendre_quadrature(f3, a, b, 5)
result_gauss_chebyshev = gauss_chebyshev_quadrature(f3, 5)
result_gauss_laguerre = gauss_laguerre_quadrature(f3, 5)
result_gauss_hermite = gauss_hermite_quadrature(f3, 5)
result_adaptive_simpsons = adaptive_simpsons_rule(f3, a, b, 1e-6)
result_monte_carlo = monte_carlo_integration(f3, a, b)
result_double_integral = double_integral(f4, 0, 1, 0, 1)
result_simpsons_error, error_estimate = simpsons_rule_with_error(f2, a, b, n)

print("Results:")
print(f"Trapezoidal Rule: {result_trapezoidal}")
print(f"Simpson's Rule: {result_simpsons}")
print(f"Midpoint Rule: {result_midpoint}")
print(f"Boole's Rule: {result_booles}")
print(f"Romberg Integration: {result_romberg}")
print(f"Gauss-Legendre Quadrature: {result_gauss_legendre}")
print(f"Gauss-Chebyshev Quadrature: {result_gauss_chebyshev}")
print(f"Gauss-Laguerre Quadrature: {result_gauss_laguerre}")
print(f"Gauss-Hermite Quadrature: {result_gauss_hermite}")
print(f"Adaptive Simpson's Rule: {result_adaptive_simpsons}")
print(f"Monte Carlo Integration: {result_monte_carlo}")
print(f"Double Integral: {result_double_integral}")
print(f"Simpson's Rule with Error Estimation: {result_simpsons_error} with an error estimate of {error_estimate}")



```

## Output
```bash 

Results:
Trapezoidal Rule: 333.33350000000013
Simpson's Rule: 1.8390715291786217
Midpoint Rule: 0.8862269254527569
Boole's Rule: 333.3333333333334
Romberg Integration: 1.839071529076259
Gauss-Legendre Quadrature: 0.9622861833849173
Gauss-Chebyshev Quadrature: 2.026469405000093
Gauss-Laguerre Quadrature: 0.5408201719540809
Gauss-Hermite Quadrature: 1.260069748687603
Adaptive Simpson's Rule: 0.443113467730597
Monte Carlo Integration: 0.7746479690195586
Double Integral: 0.25507601265177027
Simpson's Rule with Error Estimation: 1.8390715291786217 with an error estimate of 5.555553794065748e-06

```
