# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the required libraries NumPy and Matplotlib.
2. Initialize the input data (X) and output data (Y).
3. Initialize the slope, intercept, learning rate and number of iterations.
4. Calculate the predicted values and error.
5. Update the slope and intercept using the Gradient Descent method.
6. Repeat the process until the specified number of iterations is completed.
7. Predict the profit and plot the regression line.

## Program:
```

import numpy as np
import matplotlib.pyplot as plt

X = np.array([1, 2, 3, 4, 5], dtype=float)
Y = np.array([2, 4, 5, 4, 5], dtype=float)

m = 0
b = 0
learning_rate = 0.01
iterations = 1000
n = len(X)

for i in range(iterations):
    Y_pred = m * X + b

    dm = (-2/n) * np.sum(X * (Y - Y_pred))
    db = (-2/n) * np.sum(Y - Y_pred)

    m = m - learning_rate * dm
    b = b - learning_rate * db

print("Slope:", round(m, 2))
print("Intercept:", round(b, 2))

prediction = m * 6 + b
print("Predicted profit:", round(prediction, 2))

plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, m * X + b, color='red', label='Gradient Descent Line')

plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.grid()
plt.show()

```

## Output:
<img width="748" height="656" alt="image" src="https://github.com/user-attachments/assets/e7ab6724-4537-4dfa-8187-af11afe977cd" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
