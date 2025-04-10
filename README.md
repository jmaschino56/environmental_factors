# Atmospheric Movement Analysis

This project investigates how different atmospheric conditions—namely temperature, elevation, relative humidity, and barometric pressure—influence the total movement of air. In this context, "movement" is assumed to be proportional to air density changes. The code calculates the density for dry and humid air and quantifies the percent changes from a defined baseline, outputting results via plots and a sample calculation.

## Overview

The analysis is divided into four main sections:

1. **Temperature Effect:**  
   Calculates the change in air density by varying temperature from 30°F to 100°F (with a baseline of 74°F) and plots the percentage change in movement relative to the baseline.

2. **Elevation Effect:**  
   Considers how changing elevation (from sea level up to 5000 ft) affects pressure, and therefore density, at a constant temperature. It adjusts the effective pressure using an exponential decay model based on a scale height.

3. **Humidity Effect:**  
   Uses the Tetens formula to compute saturation vapor pressure and then calculates the density of humid air across a range of relative humidity values (0% to 100%) with a baseline at 50% RH.

4. **Pressure Effect:**  
   Studies the impact of varying barometric pressure (converted from Pascals to inches of Hg) on air density.

Additionally, a function `calculate_movement_change` is provided to compute the percent change in total movement (density) for arbitrary conditions relative to a defined baseline:
- Temperature: 74°F  
- Elevation: 0 ft  
- Relative Humidity: 50%  
- Pressure: 29.92 in Hg

## Dependencies

- [NumPy](https://numpy.org/) – for numerical computations.
- [Matplotlib](https://matplotlib.org/) – for plotting graphs.
- Python 3.6+ is recommended.

You can install the required libraries via pip:

```bash
pip install numpy matplotlib
