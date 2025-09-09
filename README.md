# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
Date:
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Generate synthetic time series data with trend + noise
np.random.seed(42)
time = np.arange(1, 51)
data = 2*time + np.random.normal(0, 5, 50)   # linear trend with noise

# Original Data Plot
plt.figure(figsize=(10,4))
plt.scatter(time, data, label="Original Data", color="blue")
plt.title("Time Series Data with Trend")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()

# ============================
# A - LINEAR TREND ESTIMATION
# ============================
coeffs_linear = np.polyfit(time, data, 1)  # degree 1 (linear)
linear_trend = np.polyval(coeffs_linear, time)

print("\nA - LINEAR TREND ESTIMATION")
plt.figure(figsize=(10,4))
plt.scatter(time, data, color="blue", label="Original Data")
plt.plot(time, linear_trend, color="red", linewidth=2, label="Linear Trend")
plt.title("Linear Trend Estimation")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()

# =================================
# B - POLYNOMIAL TREND ESTIMATION
# =================================
coeffs_poly = np.polyfit(time, data, 2)  # degree 2 (quadratic)
poly_trend = np.polyval(coeffs_poly, time)

print("\nB - POLYNOMIAL TREND ESTIMATION")
plt.figure(figsize=(10,4))
plt.scatter(time, data, color="blue", label="Original Data")
plt.plot(time, poly_trend, color="green", linewidth=2, label="Polynomial Trend (Quadratic)")
plt.title("Polynomial Trend Estimation")
plt.xlabel("Time")
plt.ylabel("Value")
plt.legend()
plt.show()

```
### OUTPUT
<img width="1069" height="500" alt="image" src="https://github.com/user-attachments/assets/34434937-2b6f-4b1e-9499-35d8f7626f6c" />
<img width="1071" height="517" alt="image" src="https://github.com/user-attachments/assets/164d5e81-9521-4561-8235-6035932718b2" />
<img width="1071" height="528" alt="image" src="https://github.com/user-attachments/assets/23a577a8-0bfb-4017-82c8-505aa2f01cc2" />

### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
