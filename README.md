# ED Fire Module — Offline Python Implementation

## Overview
This project implements the ED v3.0 fire submodule offline in Python.
It computes global fire risk from 2001 to 2016 using climate data and vegetation biomass.

## Data
- **Climate**: CRUJRA v3.5 (temperature and precipitation)
- **Vegetation**: TRENDY ED v3.0 cVeg (carbon in vegetation)

## Methods
1. Thornthwaite PET computed from monthly temperature
2. ED dryness index (D_bar) computed from PET and precipitation
3. Fire risk computed from aboveground biomass and dryness index

## Key Findings
- ED original parameters (normalization=30000, exponent=10) were calibrated for internal pot_soil_evap
- Thornthwaite PET operates at a different scale requiring recalibration
- Recalibrated parameters: normalization=2294 (95th percentile of D_bar), exponent=3

## Author
Richard Owusu-Ansah
University of Maryland
