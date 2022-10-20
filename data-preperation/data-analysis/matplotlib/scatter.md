# Scatter

***

### Creating Scatter Plots

With Pyplot, you can use the `scatter()` function to draw a scatter plot.

The `scatter()` function plots one dot for each observation. It needs two arrays of the same length, one for the values of the x-axis, and one for values on the y-axis:

#### Example

A simple scatter plot:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])

plt.scatter(x, y)\
plt.show()

#### Result:

Try it Yourself »

The observation in the example above is the result of 13 cars passing by.

The X-axis shows how old the car is.

The Y-axis shows the speed of the car when it passes.

Are there any relationships between the observations?

It seems that the newer the car, the faster it drives, but that could be a coincidence, after all we only registered 13 cars.

***

### Compare Plots

In the example above, there seems to be a relationship between speed and age, but what if we plot the observations from another day as well? Will the scatter plot tell us something else?

#### Example

Draw two plots on the same figure:

import matplotlib.pyplot as plt\
import numpy as np

\#day one, the age and speed of 13 cars:\
x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
plt.scatter(x, y)

\#day two, the age and speed of 15 cars:\
x = np.array(\[2,2,8,1,15,8,12,9,7,3,11,4,7,14,12])\
y = np.array(\[100,105,84,105,90,99,90,95,94,100,79,112,91,80,85])\
plt.scatter(x, y)

plt.show()

#### Result:

Try it Yourself »

**Note:** The two plots are plotted with two different colors, by default blue and orange, you will learn how to change colors later in this chapter.

By comparing the two plots, I think it is safe to say that they both gives us the same conclusion: the newer the car, the faster it drives.

***

***

### Colors

You can set your own color for each scatter plot with the `color` or the `c` argument:

#### Example

Set your own color of the markers:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
plt.scatter(x, y, color = 'hotpink')

x = np.array(\[2,2,8,1,15,8,12,9,7,3,11,4,7,14,12])\
y = np.array(\[100,105,84,105,90,99,90,95,94,100,79,112,91,80,85])\
plt.scatter(x, y, color = '#88c999')

plt.show()

#### Result:

Try it Yourself »

***

### Color Each Dot

You can even set a specific color for each dot by using an array of colors as value for the `c` argument:

**Note:** You _cannot_ use the `color` argument for this, only the `c` argument.

#### Example

Set your own color of the markers:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
colors = np.array(\["red","green","blue","yellow","pink","black","orange","purple","beige","brown","gray","cyan","magenta"])

plt.scatter(x, y, c=colors)

plt.show()

#### Result:

Try it Yourself »

***

### ColorMap

The Matplotlib module has a number of available colormaps.

A colormap is like a list of colors, where each color has a value that ranges from 0 to 100.

Here is an example of a colormap:

This colormap is called 'viridis' and as you can see it ranges from 0, which is a purple color, and up to 100, which is a yellow color.

#### How to Use the ColorMap

You can specify the colormap with the keyword argument `cmap` with the value of the colormap, in this case `'viridis'` which is one of the built-in colormaps available in Matplotlib.

In addition you have to create an array with values (from 0 to 100), one value for each of the point in the scatter plot:

#### Example

Create a color array, and specify a colormap in the scatter plot:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
colors = np.array(\[0, 10, 20, 30, 40, 45, 50, 55, 60, 70, 80, 90, 100])

plt.scatter(x, y, c=colors, cmap='viridis')

plt.show()

#### Result:

Try it Yourself »

You can include the colormap in the drawing by including the `plt.colorbar()` statement:

#### Example

Include the actual colormap:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
colors = np.array(\[0, 10, 20, 30, 40, 45, 50, 55, 60, 70, 80, 90, 100])

plt.scatter(x, y, c=colors, cmap='viridis')

plt.colorbar()

plt.show()

#### Result:

Try it Yourself »

#### Available ColorMaps

You can choose any of the built-in colormaps:

| Name              |          |   | Reverse              |          |
| ----------------- | -------- | - | -------------------- | -------- |
| Accent            | Try it » |   | Accent\_r            | Try it » |
| Blues             | Try it » |   | Blues\_r             | Try it » |
| BrBG              | Try it » |   | BrBG\_r              | Try it » |
| BuGn              | Try it » |   | BuGn\_r              | Try it » |
| BuPu              | Try it » |   | BuPu\_r              | Try it » |
| CMRmap            | Try it » |   | CMRmap\_r            | Try it » |
| Dark2             | Try it » |   | Dark2\_r             | Try it » |
| GnBu              | Try it » |   | GnBu\_r              | Try it » |
| Greens            | Try it » |   | Greens\_r            | Try it » |
| Greys             | Try it » |   | Greys\_r             | Try it » |
| OrRd              | Try it » |   | OrRd\_r              | Try it » |
| Oranges           | Try it » |   | Oranges\_r           | Try it » |
| PRGn              | Try it » |   | PRGn\_r              | Try it » |
| Paired            | Try it » |   | Paired\_r            | Try it » |
| Pastel1           | Try it » |   | Pastel1\_r           | Try it » |
| Pastel2           | Try it » |   | Pastel2\_r           | Try it » |
| PiYG              | Try it » |   | PiYG\_r              | Try it » |
| PuBu              | Try it » |   | PuBu\_r              | Try it » |
| PuBuGn            | Try it » |   | PuBuGn\_r            | Try it » |
| PuOr              | Try it » |   | PuOr\_r              | Try it » |
| PuRd              | Try it » |   | PuRd\_r              | Try it » |
| Purples           | Try it » |   | Purples\_r           | Try it » |
| RdBu              | Try it » |   | RdBu\_r              | Try it » |
| RdGy              | Try it » |   | RdGy\_r              | Try it » |
| RdPu              | Try it » |   | RdPu\_r              | Try it » |
| RdYlBu            | Try it » |   | RdYlBu\_r            | Try it » |
| RdYlGn            | Try it » |   | RdYlGn\_r            | Try it » |
| Reds              | Try it » |   | Reds\_r              | Try it » |
| Set1              | Try it » |   | Set1\_r              | Try it » |
| Set2              | Try it » |   | Set2\_r              | Try it » |
| Set3              | Try it » |   | Set3\_r              | Try it » |
| Spectral          | Try it » |   | Spectral\_r          | Try it » |
| Wistia            | Try it » |   | Wistia\_r            | Try it » |
| YlGn              | Try it » |   | YlGn\_r              | Try it » |
| YlGnBu            | Try it » |   | YlGnBu\_r            | Try it » |
| YlOrBr            | Try it » |   | YlOrBr\_r            | Try it » |
| YlOrRd            | Try it » |   | YlOrRd\_r            | Try it » |
| afmhot            | Try it » |   | afmhot\_r            | Try it » |
| autumn            | Try it » |   | autumn\_r            | Try it » |
| binary            | Try it » |   | binary\_r            | Try it » |
| bone              | Try it » |   | bone\_r              | Try it » |
| brg               | Try it » |   | brg\_r               | Try it » |
| bwr               | Try it » |   | bwr\_r               | Try it » |
| cividis           | Try it » |   | cividis\_r           | Try it » |
| cool              | Try it » |   | cool\_r              | Try it » |
| coolwarm          | Try it » |   | coolwarm\_r          | Try it » |
| copper            | Try it » |   | copper\_r            | Try it » |
| cubehelix         | Try it » |   | cubehelix\_r         | Try it » |
| flag              | Try it » |   | flag\_r              | Try it » |
| gist\_earth       | Try it » |   | gist\_earth\_r       | Try it » |
| gist\_gray        | Try it » |   | gist\_gray\_r        | Try it » |
| gist\_heat        | Try it » |   | gist\_heat\_r        | Try it » |
| gist\_ncar        | Try it » |   | gist\_ncar\_r        | Try it » |
| gist\_rainbow     | Try it » |   | gist\_rainbow\_r     | Try it » |
| gist\_stern       | Try it » |   | gist\_stern\_r       | Try it » |
| gist\_yarg        | Try it » |   | gist\_yarg\_r        | Try it » |
| gnuplot           | Try it » |   | gnuplot\_r           | Try it » |
| gnuplot2          | Try it » |   | gnuplot2\_r          | Try it » |
| gray              | Try it » |   | gray\_r              | Try it » |
| hot               | Try it » |   | hot\_r               | Try it » |
| hsv               | Try it » |   | hsv\_r               | Try it » |
| inferno           | Try it » |   | inferno\_r           | Try it » |
| jet               | Try it » |   | jet\_r               | Try it » |
| magma             | Try it » |   | magma\_r             | Try it » |
| nipy\_spectral    | Try it » |   | nipy\_spectral\_r    | Try it » |
| ocean             | Try it » |   | ocean\_r             | Try it » |
| pink              | Try it » |   | pink\_r              | Try it » |
| plasma            | Try it » |   | plasma\_r            | Try it » |
| prism             | Try it » |   | prism\_r             | Try it » |
| rainbow           | Try it » |   | rainbow\_r           | Try it » |
| seismic           | Try it » |   | seismic\_r           | Try it » |
| spring            | Try it » |   | spring\_r            | Try it » |
| summer            | Try it » |   | summer\_r            | Try it » |
| tab10             | Try it » |   | tab10\_r             | Try it » |
| tab20             | Try it » |   | tab20\_r             | Try it » |
| tab20b            | Try it » |   | tab20b\_r            | Try it » |
| tab20c            | Try it » |   | tab20c\_r            | Try it » |
| terrain           | Try it » |   | terrain\_r           | Try it » |
| twilight          | Try it » |   | twilight\_r          | Try it » |
| twilight\_shifted | Try it » |   | twilight\_shifted\_r | Try it » |
| viridis           | Try it » |   | viridis\_r           | Try it » |
| winter            | Try it » |   | winter\_r            | Try it » |

***

### Size

You can change the size of the dots with the `s` argument.

Just like colors, make sure the array for sizes has the same length as the arrays for the x- and y-axis:

#### Example

Set your own size for the markers:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
sizes = np.array(\[20,50,100,200,500,1000,60,90,10,300,600,800,75])

plt.scatter(x, y, s=sizes)

plt.show()

#### Result:

Try it Yourself »

***

### Alpha

You can adjust the transparency of the dots with the `alpha` argument.

Just like colors, make sure the array for sizes has the same length as the arrays for the x- and y-axis:

#### Example

Set your own size for the markers:

import matplotlib.pyplot as plt\
import numpy as np

x = np.array(\[5,7,8,7,2,17,2,9,4,11,12,9,6])\
y = np.array(\[99,86,87,88,111,86,103,87,94,78,77,85,86])\
sizes = np.array(\[20,50,100,200,500,1000,60,90,10,300,600,800,75])

plt.scatter(x, y, s=sizes, alpha=0.5)

plt.show()

#### Result:

Try it Yourself »

***

### Combine Color Size and Alpha

You can combine a colormap with different sizes on the dots. This is best visualized if the dots are transparent:

#### Example

Create random arrays with 100 values for x-points, y-points, colors and sizes:

import matplotlib.pyplot as plt\
import numpy as np

x = np.random.randint(100, size=(100))\
y = np.random.randint(100, size=(100))\
colors = np.random.randint(100, size=(100))\
sizes = 10 \* np.random.randint(100, size=(100))

plt.scatter(x, y, c=colors, s=sizes, alpha=0.5, cmap='nipy\_spectral')

plt.colorbar()

plt.show()

#### Result:

Try it Yourself »

***

\
