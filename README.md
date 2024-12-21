# 2DOF Helicopter LSTM

## Overview
This project models the nonlinear dynamics of a 2-DOF helicopter system using a Long Short-Term Memory (LSTM) neural network. The model predicts the system's behavior based on sequential input variables (voltage and motor currents) to output pitch and yaw angles.

## Colab Link
You can access the Google Colab notebook for this project: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1wuFwobEzw4O4ZzDRWYuvBQDBBPzS_zHA?usp=sharing)


## Data Used
The model is trained and validated using real sequential data representing the helicopter's behavior:
- **Input Variables**:
  - `V`: Voltage applied to the motors (constant for both motors).
  - `I_pitch`: Current for the pitch motor.
  - `I_yaw`: Current for the yaw motor.
- **Output Variables**:
  - `pitch_angle (θ)`: The pitch angle of the helicopter.
  - `yaw_angle (ψ)`: The yaw angle of the helicopter.

### Data Format
The input and output data are stored in separate CSV files:
- [`inputs.csv`](inputs.csv): Contains columns `V`, `I_pitch`, `I_yaw`.
- [`outputs.csv`](outputs.csv): Contains columns `pitch_angle`, `yaw_angle`.


### Using the Trained Model
- Ensure the trained model file [`2dof_helicopter_model.h5`](2dof_helicopter_model.h5) is available in your working directory or uploaded to Colab.
- Use the model to make predictions:
   ```python
   # Define new input (1 timestep, 3 features: V, I_pitch, I_yaw)
   new_inputs = [[15, 2, 2]]  # Example input
   ```
