# lstm-for-jena-dataset
🌡️ Climate LSTM Predictor
Deep learning model for temperature prediction using LSTM neural networks.

📋 Overview
This project implements an LSTM-based regression model to predict temperature (T (degC)) from climate features like pressure, humidity, wind speed, and dew point.

🛠️ Requirements
pip install numpy pandas matplotlib torch scikit-learn

📊 Features Used
Feature         | Description          
----------------+----------------------
`p (mbar)`      | Pressure             
`rh (%)`        | Relative humidity    
`wv (m/s)`      | Wind velocity        
`max. wv (m/s)` | Max wind velocity    
`wd (deg)`      | Wind direction       
`Tdew (degC)`   | Dew point temperature
`VPact (mbar)`  | Vapor pressure       
`rho (g/m**3)`  | Air density          
⚙️ Hyperparameters
SEQ_LENGTH = 24      # Input sequence length (hours)
BATCH_SIZE = 64
EPOCHS = 30
LEARNING_RATE = 0.001
HIDDEN_SIZE = 64
NUM_LAYERS = 2
DROPOUT = 0.2

🚀 Usage
python train.py

📁 Project Structure
├── jena.csv          # Climate dataset
├── train.py          # Training script
├── README.md         # This file
└── models/           # Saved models

📈 Data Split
• Train: 70%
• Validation: 15%
• Test: 15%

🔧 Model Architecture
LSTM (input_size=8, hidden=64, layers=2)
    → ReLU
