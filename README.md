# LSTM for Predicting River Levels Using Log-Signature Features
This project uses Long Short-Term Memory (LSTM) neural networks with log-signature features from time-series sensor data to forecast river level readings in York.

Developed as part of a university dissertation focused on time-series modelling of hydrological data using log-signature methods.
## External Data Files

Due to file size and repository constraints, the following dataset files are hosted externally. You can download them via the link below and place them in the `data/` directory.
https://drive.google.com/drive/folders/1PHAVZBzzgnn9M_Drx8a6hEdfq6D5bbqv?usp=sharing
## Project Structure
LSTM_for_predicting_river_levels/
├── data/ # Folder for input CSV files (not included due to size)
├── models/ # Saved models (.h5)
├── outputs/ # Predictions CSV outputs
├── Script # Main LSTM training script
├── requirements.txt # Python dependencies
└── README.md # This file

## Getting Started
## Model details
Input: x-hour window of river level and flow readings from 13 upstream locations (x is decided by the user)

Output: River level prediction at Viking Recorder station, y hours ahead (y is decided by the user)

Feature Engineering: Log-signatures of order n calculated using the esig library (n is decided by the user)

Model: Two-layer LSTM with 256 and 64 units respectively, using the Adam optimizer and mean squared error loss

##  Outputs
After running the script, you will find:
models/RNN_YYYY-MM-DD_HH-MM-SS.h5 — Trained model saved with timestamp
outputs/predictions_YYYY-MM-DD_HH-MM-SS.csv — CSV containing actual and predicted values
outputs/plot_YYYY-MM-DD_HH-MM-SS.png — Plot image showing predicted vs actual river levels

###  Clone the repository
```bash
git clone https://github.com/lookali-code/LSTM_for_predicting_river_levels.git
cd LSTM_for_predicting_river_levels
