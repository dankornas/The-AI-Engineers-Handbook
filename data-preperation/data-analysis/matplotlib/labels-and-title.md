# Labels and Title

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark>\
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Create Labels for a Plot

With Pyplot, you can use the `xlabel()` and `ylabel()` functions to set a label for the x- and y-axis.

Add labels to the x- and y-axis:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.plot(x, y)

plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.show()
```

![img\_matplotlib\_labels](https://user-images.githubusercontent.com/86244964/197054360-4315acbf-b676-425a-852d-d10984d45078.png)

## Create a Title for a Plot

With Pyplot, you can use the `title()` function to set a title for the plot.

Add a plot title and labels for the x- and y-axis:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.plot(x, y)

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.show()
```

![img\_matplotlib\_title](https://user-images.githubusercontent.com/86244964/197054461-eb79f644-cc2b-44b2-9882-dba7584b531b.png)

## Set Font Properties for Title and Labels

You can use the `fontdict` parameter in `xlabel()`, `ylabel()`, and `title()` to set font properties for the title and labels.

Set font properties for the title and labels:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

font1 = {'family':'serif','color':'blue','size':20}
font2 = {'family':'serif','color':'darkred','size':15}

plt.title("Sports Watch Data", fontdict = font1)
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y)
plt.show()
```

![img\_matplotlib\_title\_fontdict](https://user-images.githubusercontent.com/86244964/197054588-d31a0b28-367b-4724-8fcd-e97b8afa5774.png)

## Position the Title

You can use the `loc` parameter in `title()` to position the title.

Legal values are: 'left', 'right', and 'center'. Default value is 'center'.

Position the title to the left:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data", loc = 'left')
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)
plt.show()
```

![img\_matplotlib\_title\_loc](https://user-images.githubusercontent.com/86244964/197054664-791d675c-086e-488c-9e31-e9b907e25cd9.png)
