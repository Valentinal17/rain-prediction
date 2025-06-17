# Rainfall Prediction Using Simple RNN
This project uses a Recurrent Neural Network (RNN) to predict monthly average rainfall based on historical data from different Indian subdivisions, specifically using the `BIHAR` dataset.
---
## Dataset
- **Source**: Indian Rainfall Dataset (1901-2015)
- **Format**: CSV
- **Content**: Monthly rainfall data for various subdivisions over the years.
- **Target Column**: `avg_rainfall` (extracted and transformed from monthly values)
---
## Model
- **Model Type**: Simple RNN (Recurrent Neural Network)
- **Framework**: TensorFlow / Keras
- **Libraries Used**:
  - `tensorflow.keras` for RNN layers
  - `pandas`, `numpy` for data manipulation
  - `scikit-learn` for scaling
  - `matplotlib` for data visualization
---
## Workflow
### 1. Data Preprocessing
- Load the dataset and filter for the subdivision `BIHAR`.
- Melt and reshape the data to have `YEAR`, `Month`, and `avg_rainfall`.
- Convert month names to numerical values.
- Generate datetime feature from `YEAR` and `Month`.
- Normalize the `avg_rainfall` values.
### 2. Model Creation
- Build a Sequential model with:
  - `SimpleRNN` layer
  - `Dense` output layer
- Compile and train the model on time-series rainfall data.
### 3. Evaluation
- Use Mean Squared Error (MSE) to evaluate model performance.
- Visualize predictions vs. actual values.
---
## Output
The model predicts monthly average rainfall. Visualization includes comparison plots of predicted vs. actual rainfall trends.
---
## File Structure
```
├── rainfall_prediction_rnn.ipynb     # Jupyter Notebook with all code
├── rainfall in india 1901-2015.csv   # Dataset used
├── README.md                         # Project documentation
```
---
## Requirements
Install the following dependencies:
```bash
pip install pandas numpy matplotlib scikit-learn tensorflow
---
## Remarks
- Developed as a simple RNN-based time series prediction project for rainfall trends in Indian regions.
