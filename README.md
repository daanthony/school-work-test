linear regression


## -*- coding: utf-8 -*-
"""
Created on Wed Jun  6 15:05:18 2018

@author: Dylan Anthony
"""

import numpy as np


def warm_up_exercise():
    """
    An example function that returns the 5x5 identity matrix.

    Returns
    -------
    A : ndarray, shape (5, 5)
        A 5x5 identity matrix.
    """
    A = np.eye(5, dtype=int)
    return A

print ("5x5 Identity Matrix:")
print (warm_up_exercise())


data = np.loadtxt(open("ex1data1.txt", "r"), delimiter=",")
X = data[:, 0]
y = data[:, 1]
m = len(y)  # Number of training examples
import matplotlib.pyplot as plot


def plot_data(x, y):
    """
    Plots the data points x and y.

    Parameters
    ----------
    x : array-like
        Data on x axis.
    y : array-like
        Data on y axis.
    """
    plot.plot(x, y, linestyle='', marker='x', color='black', )##label='Training data')
    plot.xlabel('Population of City in 10,000s')
    plot.ylabel('Profit in $10,000s')
    plot.title('linear regression on python')
    plot.figure()
plot_data(X, y)
plot.show()
