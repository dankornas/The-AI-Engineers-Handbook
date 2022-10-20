# Plotting

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

# Plotting x and y points

The `plot()` function is used to draw points (markers) in a diagram.

By default, the `plot()` function draws a line from point to point.

The function takes parameters for specifying points in the diagram.

Parameter 1 is an array containing the points on the **x-axis**.

Parameter 2 is an array containing the points on the **y-axis**.

If we need to plot a line from (1, 3) to (8, 10), we have to pass two arrays \[1, 8] and \[3, 10] to the plot function.

Draw a line in a diagram from position (1, 3) to position (8, 10):

```python
import matplotlib.pyplot as plt\
import numpy as np

xpoints = np.array(\[1, 8])\
ypoints = np.array(\[3, 10])

plt.plot(xpoints, ypoints)\
plt.show()
```
![img_matplotlib_plotting1](https://user-images.githubusercontent.com/86244964/197047956-2b141f56-3192-4490-9dba-241935a4802e.png)

The **x-axis** is the horizontal axis.

The **y-axis** is the vertical axis.


# Plotting Without Line

To plot only the markers, you can use _shortcut string notation_ parameter 'o', which means 'rings'.

Draw two points in the diagram, one at position (1, 3) and one in position (8, 10):

```python
import matplotlib.pyplot as plt\
import numpy as np

xpoints = np.array(\[1, 8])\
ypoints = np.array(\[3, 10])

plt.plot(xpoints, ypoints, 'o')\
plt.show()
```
![img_matplotlib_plot_o](https://user-images.githubusercontent.com/86244964/197048000-2617856a-3331-4cea-a403-3fa57c236006.png)

# Multiple Points

You can plot as many points as you like, just make sure you have the same number of points in both axis.

Draw a line in a diagram from position (1, 3) to (2, 8) then to (6, 1) and finally to position (8, 10):

```python
import matplotlib.pyplot as plt\
import numpy as np

xpoints = np.array(\[1, 2, 6, 8])\
ypoints = np.array(\[3, 8, 1, 10])

plt.plot(xpoints, ypoints)\
plt.show()
```
![img_matplotlib_plotting2](https://user-images.githubusercontent.com/86244964/197048022-f90e240f-1162-4d6f-8dc6-1e0efef6b029.png)

# Default X-Points

If we do not specify the points in the x-axis, they will get the default values 0, 1, 2, 3, (etc. depending on the length of the y-points.

So, if we take the same example as above, and leave out the x-points, the diagram will look like this.

Plotting without x-points:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10, 5, 7])

plt.plot(ypoints)\
plt.show()
```
![img_matplotlib_plotting4](https://user-images.githubusercontent.com/86244964/197048042-74f53d07-3d19-4670-a22d-de81226b2a40.png)

The **x-points** in the example above is \[0, 1, 2, 3, 4, 5].

{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
