# Polarization-Analysis-2.0
This Repository contains the Polarization Analysis Codes of P and S waves that determines the P, S wave Azimuth, Back-Azimuth and Inclinations. The code has been modified and debugged to match the latest python versions.

## Introduction
This package uses seismic data and applyies a polarisation analysis to obtain a back azimuth based on an arriving wave.
Originally used for Martian seismic data from the InSight mission, it can also be applied to earthquake data or synthetics.

A detailed description of the method and resulting plot can be found in [BSSA](https://pubs.geoscienceworld.org/ssa/bssa/article/112/4/1787/613988/Low-Frequency-Marsquakes-and-Where-to-Find-Them), or, in the absence of institutional access, [arXiv](https://arxiv.org/abs/2204.12959).

## Reference
Géraldine Zenhäusern, Simon C. Stähler, John F. Clinton, Domenico Giardini, Savas Ceylan, Raphaël F. Garcia; Low‐Frequency Marsquakes and Where to Find Them: Back Azimuth Determination Using a Polarization Analysis Approach. *Bulletin of the Seismological Society of America* **2022**; 112 (4): 1787–1805. doi: https://doi.org/10.1785/0120220019

## Code Changes
The original codebase was developed using Python 2. It has since been refactored and updated to ensure compatibility with Python 3 and to integrate the latest library dependencies. The following code changes was implemented:
1. scipy.signal.hanning library has become obsolete thus it has been replaced with scipy.signal.windows.hann. Scripts containing this change: polarisation_calculation.py
2. The string literal 'f'' this is a test {variable'} word' is incorrect and will not execute as intended. To properly format it as an f-string in Python, ensuring that the variable is correctly embedded within the string, it should be written as f'this is a test {variable} word'. This properly allows for the insertion of the variable's value within the string. More about python string literals can be found in [Python String Literals](https://realpython.com/python-raw-strings/). Scripts containing this change: polarisation_calculation.py, polarisation_plot.py

## License
This project is licensed under the terms of the GPLv3 license.

Copyright (C) 2022  Géraldine Zenhäusern (geraldine@zenhausern.net), Simon Stähler (mail@simonstaehler.com), Martin van Driel (Martin@vanDriel.de)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
 any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see [here](https://www.gnu.org/licenses/).
