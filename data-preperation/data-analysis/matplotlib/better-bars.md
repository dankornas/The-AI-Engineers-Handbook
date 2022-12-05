# Better Bars

One of the most common types of plots that people create with matplotlib is the bar chart.

### Simple bar charts

To create a bar chart in matplotlib, you can use the `bar()` function. This function takes two required arguments: the x-coordinates of the bars, and the heights of the bars. Here is an example of how to use the `bar()` function to create a simple bar chart:

```python
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# create bar chart
plt.bar(x, y)

# show the plot
plt.show()
```

This code will create a bar chart with three bars, corresponding to the values in the `x` and `y` arrays. The bars will be placed at the x-coordinates 1, 2, and 3, and their heights will be 10, 20, and 30, respectively.

### Customizing the appearance of the bars

The `bar()` function has several optional parameters that you can use to customize the appearance of the bars. For example, you can specify the width of the bars using the `width` parameter, the color of the bars using the `color` parameter, and the edge color and thickness using the `edgecolor` and `linewidth` parameters.

Here is an example of how to use these parameters to customize the appearance of the bars:

```python
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# create bar chart with custom width, color, and edge properties
plt.bar(x, y, width=0.5, color="green", edgecolor="black", linewidth=2)

# show the plot
plt.show()
```

This code will create the same bar chart as before, but the bars will be narrower, green, and have black edges with a thickness of 2 pixels.

### Creating horizontal bars

In addition to vertical bars, you can also create horizontal bars in matplotlib using the `barh()` function. This function works in the same way as the `bar()` function, but it creates horizontal bars instead of vertical bars.

Here is an example of how to use the `barh()` function to create a horizontal bar chart:

```python
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# create horizontal bar chart
plt.barh(x, y)

# show the plot
plt.show()
```

This code will create a horizontal bar chart with three bars, placed at the y-coordinates 1, 2, and 3, and with heights of 10, 20, and 30, respectively.

### Changing the bar colors

By default, the bars in a matplotlib bar chart are blue. However, you can change the color of the bars by using the `color` parameter of the `bar()` function. This parameter accepts a single color value, or a list of colors with one color for each bar.

Here is an example of how to use the `color` parameter to change the colors of the bars in a bar chart:

```python
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# create bar chart with custom colors
plt.bar(x, y, color=["red", "green", "blue"])

# show the plot
plt.show()
```

This code will create a bar chart with three bars, and the colors of the bars will be red, green, and blue, respectively.

### Changing the bar heights

The heights of the bars in a bar chart are determined by the values in the `y` array that you pass to the `bar()` function. If you want to change the heights of the bars, you can simply modify the values in this array.

Here is an example of how to change the heights of the bars in a bar chart:

```makefile
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# change the heights of the bars
y = [15, 25, 35]

# create bar chart
plt.bar(x, y)

# show the plot
plt.show()
```

This code will create the same bar chart as before, but the heights of the bars will be 15, 25, and 35, instead of 10, 20, and 30.

### Changing the bar widths

The width of the bars in a bar chart is determined by the `width` parameter of the `bar()` function. By default, this parameter is set to 0.8, which means that the bars will be 80% of the distance between the x-coordinates of the bars.

You can change the width of the bars by modifying the value of the `width` parameter. For example, if you set this parameter to 0.5, the bars will be half as wide as they were before.

Here is an example of how to change the width of the bars in a bar chart:

```python
Copy code# import matplotlib
import matplotlib.pyplot as plt

# data to plot
x = [1, 2, 3]
y = [10, 20, 30]

# create bar chart with custom width
plt.bar(x, y, width=0.5)

# show the plot
plt.show()
```

This code will create a bar chart with three bars, and the bars will be half as wide as they were in the previous examples.
