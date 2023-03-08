# Subplot

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark>\
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Display Multiple Plots

With the `subplot()` function you can draw multiple plots in one figure.

Draw 2 plots:

```python
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)

plt.show()
```

![img\_matplotlib\_subplots1](https://user-images.githubusercontent.com/86244964/197056245-71ee53c9-26df-4d0b-bb3a-eddb8041c1b6.png)

## The subplot() Function

The `subplot()` function takes three arguments that describes the layout of the figure.

The layout is organized in rows and columns, which are represented by the _first_ and _second_ argument.

The third argument represents the index of the current plot.

```python
plt.subplot(1, 2, 1)
#the figure has 1 row, 2 columns, and this plot is the _first_ plot.
```

```python
plt.subplot(1, 2, 2)
#the figure has 1 row, 2 columns, and this plot is the _second_ plot.
```

So, if we want a figure with 2 rows an 1 column (meaning that the two plots will be displayed on top of each other instead of side-by-side), we can write the syntax like this:

Draw 2 plots on top of each other:

```python
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(2, 1, 1)
plt.plot(x,y)

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(2, 1, 2)
plt.plot(x,y)

plt.show()
```

![img\_matplotlib\_subplots2](https://user-images.githubusercontent.com/86244964/197056429-dd7cefe3-7c05-4eda-96e9-3d298020bbfe.png)

You can draw as many plots you like on one figure, just descibe the number of rows, columns, and the index of the plot.

Draw 6 plots:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(2, 3, 1)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(2, 3, 2)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(2, 3, 3)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(2, 3, 4)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(2, 3, 5)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(2, 3, 6)
plt.plot(x,y)

plt.show()
```

![img\_matplotlib\_subplots3](https://user-images.githubusercontent.com/86244964/197056527-0031d13a-70b3-42a5-a792-586635323702.png)

## Title

You can add a title to each plot with the `title()` function:

2 plots, with titles:

```python
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)
plt.title("SALES")

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)
plt.title("INCOME")

plt.show()
```

![img\_matplotlib\_subplots4](https://user-images.githubusercontent.com/86244964/197056603-3e281177-bcab-4895-9c8b-f94fde0f8d31.png)

## Super Title

You can add a title to the entire figure with the `suptitle()` function:

Add a title for the entire figure:

```python
import matplotlib.pyplot as plt
import numpy as np

#plot 1:
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(1, 2, 1)
plt.plot(x,y)
plt.title("SALES")

#plot 2:
x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(1, 2, 2)
plt.plot(x,y)
plt.title("INCOME")

plt.suptitle("MY SHOP")
plt.show()
```

![img\_matplotlib\_subplots5](https://user-images.githubusercontent.com/86244964/197056695-63a2abb5-0192-4768-84d3-90756888de38.png)
