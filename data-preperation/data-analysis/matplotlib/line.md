{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

# Linestyle

You can use the keyword argument `linestyle`, or shorter `ls`, to change the style of the plotted line.

Use a dotted line:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, linestyle = 'dotted')\
plt.show()
```
![img_matplotlib_line_dotted](https://user-images.githubusercontent.com/86244964/197049815-55d2985f-af19-45f3-b78b-bda007d1489b.png)

Use a dashed line:
```python
plt.plot(ypoints, linestyle = 'dashed')
```
![img_matplotlib_line_dashed](https://user-images.githubusercontent.com/86244964/197049893-0a9ff850-8c89-4f1f-ba84-7a20a2999b80.png)

# Shorter Syntax

The line style can be written in a shorter syntax:

`linestyle` can be written as `ls`.

`dotted` can be written as `:`.

`dashed` can be written as `--`.

```python
plt.plot(ypoints, ls = ':')
```
![img_matplotlib_line_dotted](https://user-images.githubusercontent.com/86244964/197050120-0b5fe084-a3f5-41a0-a244-e97eb5623575.png)

### Line Styles

You can choose any of these styles:

| Style             | Or        |          |
| ----------------- | --------- | -------- |
| 'solid' (default) | '-'       | Try it » |
| 'dotted'          | ':'       | Try it » |
| 'dashed'          | '--'      | Try it » |
| 'dashdot'         | '-.'      | Try it » |
| 'None'            | '' or ' ' | Try it » |

# Line Color

You can use the keyword argument `color` or the shorter `c` to set the color of the line.

Set the line color to red.
```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, color = 'r')\
plt.show()
```
![img_matplotlib_line_red](https://user-images.githubusercontent.com/86244964/197050246-29f95def-ff0c-4489-8664-db6b3c4e17fd.png)

You can also use Hexadecimal color values.

Plot with a beautiful green line:

```python
...
plt.plot(ypoints, c = '#4CAF50')
...
```
![img_matplotlib_line_hex](https://user-images.githubusercontent.com/86244964/197050380-3bdca488-53e4-4070-b388-041c90fac3a9.png)

Or any of the 140 supported color names.

Plot with the color named "hotpink".

```python
...\
plt.plot(ypoints, c = 'hotpink')\
...
```
![img_matplotlib_line_hotpink](https://user-images.githubusercontent.com/86244964/197050462-7396584b-bee8-4174-897e-bff02c094e62.png)

# Line Width

You can use the keyword argument `linewidth` or the shorter `lw` to change the width of the line.

The value is a floating number, in points.

Plot with a 20.5pt wide line:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, linewidth = '20.5')\
plt.show()
```
![img_matplotlib_line_lw](https://user-images.githubusercontent.com/86244964/197050549-d9e7882e-3699-49a1-8d99-40aff253c6a0.png)

# Multiple Lines

You can plot as many lines as you like by simply adding more `plt.plot()` functions.

Draw two lines by specifying a `plt.plot()` function for each line:

```python
import matplotlib.pyplot as plt\
import numpy as np

y1 = np.array(\[3, 8, 1, 10])\
y2 = np.array(\[6, 2, 7, 11])

plt.plot(y1)\
plt.plot(y2)

plt.show()
```
![img_matplotlib_line_two](https://user-images.githubusercontent.com/86244964/197050633-9d656597-8ca6-4966-996f-840e89f7095a.png)

You can also plot many lines by adding the points for the x- and y-axis for each line in the same `plt.plot()` function.

(In the examples above we only specified the points on the y-axis, meaning that the points on the x-axis got the the default values (0, 1, 2, 3).)

The x- and y- values come in pairs.

Draw two lines by specifiyng the x- and y-point values for both lines:

```python
import matplotlib.pyplot as plt\
import numpy as np

x1 = np.array(\[0, 1, 2, 3])\
y1 = np.array(\[3, 8, 1, 10])\
x2 = np.array(\[0, 1, 2, 3])\
y2 = np.array(\[6, 2, 7, 11])

plt.plot(x1, y1, x2, y2)\
plt.show()
```
![img_matplotlib_line_two](https://user-images.githubusercontent.com/86244964/197050729-e5fda45c-7783-4375-93b3-6fbf0e86d6a7.png)

{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}

