#Hybrid Gravitational-Wave Detection with Matched Filtering and CNN's

This project implements a hybrid gravitational-wave detection pipeline using real LIGO data. 
Classical matched filtering is combined with a convolutional neural network (CNN) trained on 
time-frequency representations of strain data from Hanford and Livingston detectors.

## Features
- Matched filtering with IMRPhenomD templates
- Time-frequency patch construction from real LIGO strain
- CNN-based signal vs noise classification
- Evaluation using ROC, Precision-Recall, and false alarm rates
- Tested on GW150914, GW151226, and GW170104

## Data
Open LIGO data accessed via GWOSC using `gwpy` and `pycbc`.

## Results
The CNN shows strong agreement with matched filtering in localizing real gravitational-wave
events and generalizes across multiple binary black hole mergers.

## Notes
This project was completed as a final group project for an undergraduate physics course.
