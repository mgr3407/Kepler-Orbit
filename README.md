# Kepler Orbits: Numerical Methods for ODEs

## Project Description

This repository contains Python implementations and developments of numerical methods for solving first-order Initial Value Problems (IVPs) in Ordinary Differential Equations (ODEs).

The main goal of this work is to conduct a scalar comparative study regarding the precision and performance of different numerical schemes (Euler's method and the fourth-order Runge-Kutta method), using the exact analytical solution as a reference. This analysis serves as the preliminary phase before adapting the algorithms to vector-valued functions for simulating Keplerian orbit problems.

## Contents and Implemented Methods

### 1. Analytical Reference Solution
* **Module `EDO(f, x0, y0)`**: Uses the symbolic mathematics library SymPy (`sp.dsolve`) to solve the differential equation analytically with its initial conditions. It provides the exact reference value to evaluate the errors introduced by the numerical methods.

### 2. Euler's Method
* **Module `Euler(f, x0, y0, n, xf)`**: An explicit first-order method that approximates the solution over an interval divided into $n$ partitions with a step size of $h = \frac{x_f - x_0}{n}$.
* **Module `error_Euler(f, x0, y0, n, xf)`**: Calculates the percentage relative error at the endpoint of the interval compared to the exact analytical solution.

### 3. Fourth-Order Runge-Kutta Method (RK4)
* **Module `RK4(f, x0, y0, xf)`**: A higher-precision numerical scheme that evaluates four intermediate slopes ($k_1, k_2, k_3, k_4$) to approximate the function's value at the end of the interval.
* **Module `error_RK4(f, x0, y0, xf)`**: Calculates the percentage relative error of the RK4 method against the exact analytical solution.

### 4. Performance Comparison and Analysis
* Comparative evaluation of error percentage convergence versus the number of subintervals or partitions ($n$).
* Graphical representation of error variation generated using the Matplotlib library.
