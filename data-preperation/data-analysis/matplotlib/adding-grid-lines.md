# Adding Grid Lines

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark>\
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Add Grid Lines to a Plot

With Pyplot, you can use the `grid()` function to add grid lines to the plot.

Add grid lines to the plot:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)

plt.grid()

plt.show()
```

![img\_matplotlib\_grid](https://user-images.githubusercontent.com/86244964/197054976-37222124-de6e-430c-9f23-154bdde14e4a.png)

## Specify Which Grid Lines to Display

You can use the `axis` parameter in the `grid()` function to specify which grid lines to display.

Legal values are: 'x', 'y', and 'both'. Default value is 'both'.

Display only grid lines for the x-axis:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)

plt.grid(axis = 'x')

plt.show()
```

![img\_matplotlib\_grid\_axisx](https://user-images.githubusercontent.com/86244964/197055076-18e73a70-e36d-4008-b99f-160ba9458b77.png)

Display only grid lines for the y-axis:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)

plt.grid(axis = 'y')

plt.show()
```

![img\_matplotlib\_grid\_axisy](https://user-images.githubusercontent.com/86244964/197055136-2928175c-1e49-4f28-9d76-71100564ebe4.png)

## Set Line Properties for the Grid

You can also set the line properties of the grid, like this: grid(color = '_color_', linestyle = '_linestyle_', linewidth = _number_).

Set the line properties of the grid:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)

plt.grid(color = 'green', linestyle = '--', linewidth = 0.5)

plt.show()
```

![img\_matplotlib\_grid\_kwargs](https://user-images.githubusercontent.com/86244964/197055229-0ab15e10-041a-467e-87ed-ccf73a7e172c.png)
