[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
(https://colab.research.google.com/github/jessehart-crypto/hybrid-gw-detection/blob/main/hybrid_gw_detection_mf_cnn.ipynb)


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

## Limitations
This Study is limited to short (32 s) data segments around known events and a small number of confirmed mergers.
As a result, the estimated false alarm rates are not representative of full observing runs.
Future work would require training on much longer background data and a broader set of waveform morphologies.

## Results
The CNN shows strong agreement with matched filtering in localizing real gravitational-wave
events and generalizes across multiple binary black hole mergers, despite being trained on a limited dataset.

## How to Run

### Option 1: Run in Google Colab (Recommended)
Open the notebook directly in your browser:
https://colab.research.google.com/github/jessehart-crypto/hybrid-gw-detection/blob/main/hybrid_gw_detection_mf_cnn.ipynb

Note: The first run may take several minutes to install dependencies and download LIGO data.

### Option 2: Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/jessehart-crypto/hybrid-gw-detection.git
   cd hybrid-gw-detection
Install dependencies:

2. Install dependencies:
  pip install -r requirements.txt

3.  Launch Jupyter Notebook:
   jupyter notebook
4.  Open and run:
hybrid_gw_detection_mf_cnn.ipynb




## Notes
This project was completed as a final group project for an undergraduate physics course.
