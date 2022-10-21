{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

# Creating Pie Charts

With Pyplot, you can use the `pie()` function to draw pie charts.

A simple pie chart:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])

plt.pie(y)\
plt.show()&#x20;
```
![img_matplotlib_pie1](https://user-images.githubusercontent.com/86244964/197153590-231a7d0e-afa8-469b-b7cb-d6f22a57d060.png)

As you can see the pie chart draws one piece (called a wedge) for each value in the array (in this case [35, 25, 25, 15]).

**Note:** The size of each wedge is determined by comparing the value with all the other values, by using this formula:

The value divided by the sum of all values: `x/sum(x)`

# Labels

Add labels to the pie chart with the `label` parameter.

The `label` parameter must be an array with one label for each wedge.

A simple pie chart:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)\
plt.show()&#x20;
```
![img_matplotlib_pie_labels](https://user-images.githubusercontent.com/86244964/197153857-776d3eb8-a314-4581-995a-9ee6d9819b43.png)

# Start Angle

As mentioned the default start angle is at the x-axis, but you can change the start angle by specifying a `startangle` parameter.

The `startangle` parameter is defined with an angle in degrees, default angle is 0.

Start the first wedge at 90 degrees:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels, startangle = 90)\
plt.show()&#x20;
```
![img_matplotlib_pie_angles](https://user-images.githubusercontent.com/86244964/197153962-a32de2c2-5aea-43a6-8bca-3b4a3f27ad68.png)

# Explode

Maybe you want one of the wedges to stand out? The `explode` parameter allows you to do that.

The `explode` parameter, if specified, and not `None`, must be an array with one value for each wedge.

Each value represents how far from the center each wedge is displayed.

Pull the "Apples" wedge 0.2 from the center of the pie:
```python
import matplotlib.pyplot as plt
import numpy as np

y = np.array(\[35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
myexplode = [0.2, 0, 0, 0]

plt.pie(y, labels = mylabels, explode = myexplode)
plt.show()&#x20;
```

![img_matplotlib_pie_explode](https://user-images.githubusercontent.com/86244964/197154105-71c2679a-add7-4df3-86b4-c0ac05206357.png)

# Shadow

Add a shadow to the pie chart by setting the `shadows` parameter to `True`.

Add a shadow:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]\
myexplode = \[0.2, 0, 0, 0]

plt.pie(y, labels = mylabels, explode = myexplode, shadow = True)\
plt.show()&#x20;
```

![img_matplotlib_pie_shadow](https://user-images.githubusercontent.com/86244964/197154178-c3355119-7fff-4286-a19b-7a872411392f.png)

# Colors

You can set the color of each wedge with the `colors` parameter.

The `colors` parameter, if specified, must be an array with one value for each wedge.

Specify a new color for each wedge:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]\
mycolors = \["black", "hotpink", "b", "#4CAF50"]

plt.pie(y, labels = mylabels, colors = mycolors)\
plt.show()&#x20;
```
![img_matplotlib_pie_color](https://user-images.githubusercontent.com/86244964/197154255-386f4533-6576-48d3-a3f6-984df649c104.png)

You can use Hexadecimal color values, any of the 140 supported color names, or one of these shortcuts:

`'r'` - Red\
`'g'` - Green\
`'b'` - Blue\
`'c'` - Cyan\
`'m'` - Magenta\
`'y'` - Yellow\
`'k'` - Black\
`'w'` - White\

# Legend

To add a list of explanation for each wedge, use the `legend()` function.

Add a legend:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)\
plt.legend()\
plt.show()&#x20;
```
![img_matplotlib_pie_legend](https://user-images.githubusercontent.com/86244964/197154353-f2edfd93-7c0a-4ca8-b6d5-626cc73ca595.png)

# Legend With Header

To add a header to the legend, add the `title` parameter to the `legend` function.

Add a legend with a header:
```python
import matplotlib.pyplot as plt\
import numpy as np

y = np.array(\[35, 25, 25, 15])\
mylabels = \["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)\
plt.legend(title = "Four Fruits:")\
plt.show()&#x20;
```
![img_matplotlib_pie_legend_title](https://user-images.githubusercontent.com/86244964/197154437-f70a7e4d-cfbd-40ab-b620-4dce9a3f53ec.png)


{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
