---
layout: default
title: 3D-Plotting
permalink: /3D/
3D: active
about: passive
contact: passive
---
```python
from mpl_toolkits import mplot3d
```


```python
%matplotlib inline
import numpy as np
import matplotlib.pyplot as plt
```


```python
fig = plt.figure()
ax = plt.axes(projection='3d')
```


![png](../img/3D-plotting_files/3D-plotting_2_0.png)



```python
ax = plt.axes(projection='3d')

# Data for a 3-D line
zline = np.linspace(0, 15, 1000)
yline = np.sin(zline)
xline = np.cos(zline)
ax.plot3D(xline, yline, zline, 'gray')

# Data for the 3-D scattered points
zdata = 15 * np.random.random(100)
xdata = np.sin(zdata) + 0.1 * np.random.randn(100)
ydata = np.cos(zdata) + 0.1 * np.random.randn(100)
ax.scatter3D(xdata, ydata, zdata, c=zdata, cmap='Greens');
```


![png](../img/3D-plotting_files/3D-plotting_3_0.png)



```python

```
