# Markers

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark> \
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

# Markers

You can use the keyword argument `marker` to emphasize each point with a specified marker.

Mark each point with a circle:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, marker = 'o')\
plt.show()
```
![img_matplotlib_marker_o](https://user-images.githubusercontent.com/86244964/197048239-12c17da1-a810-417c-976e-94f2cc772ec2.png)

Mark each point with a star:

```python
...
plt.plot(ypoints, marker = '\*')\
...
```
![img_matplotlib_marker_star](https://user-images.githubusercontent.com/86244964/197048332-48a039c7-3412-4aec-bb58-1243e643786d.png)

# Marker Reference

You can choose any of these markers:

| Marker | Description    |          |
| ------ | -------------- | -------- |
| 'o'    | Circle         | Try it » |
| '\*'   | Star           | Try it » |
| '.'    | Point          | Try it » |
| ','    | Pixel          | Try it » |
| 'x'    | X              | Try it » |
| 'X'    | X (filled)     | Try it » |
| '+'    | Plus           | Try it » |
| 'P'    | Plus (filled)  | Try it » |
| 's'    | Square         | Try it » |
| 'D'    | Diamond        | Try it » |
| 'd'    | Diamond (thin) | Try it » |
| 'p'    | Pentagon       | Try it » |
| 'H'    | Hexagon        | Try it » |
| 'h'    | Hexagon        | Try it » |
| 'v'    | Triangle Down  | Try it » |
| '^'    | Triangle Up    | Try it » |
| '<'    | Triangle Left  | Try it » |
| '>'    | Triangle Right | Try it » |
| '1'    | Tri Down       | Try it » |
| '2'    | Tri Up         | Try it » |
| '3'    | Tri Left       | Try it » |
| '4'    | Tri Right      | Try it » |
| '\|'   | Vline          | Try it » |
| '\_'   | Hline          | Try it » |

# Format Strings `fmt`

You can use also use the _shortcut string notation_ parameter to specify the marker.

This parameter is also called `fmt`, and is written with this syntax:

_`marker`_`|`_`line`_`|`_`color`_

Mark each point with a circle:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, 'o:r')\
plt.show()
```
![img_matplotlib_marker_fmt1](https://user-images.githubusercontent.com/86244964/197048469-ed5dfdf1-db7d-4186-9451-162567e1c7d0.png)

The marker value can be anything from the Marker Reference above.

The line value can be one of the following:

### Line Reference

| Line Syntax | Description        |          |
| ----------- | ------------------ | -------- |
| '-'         | Solid line         | Try it » |
| ':'         | Dotted line        | Try it » |
| '--'        | Dashed line        | Try it » |
| '-.'        | Dashed/dotted line | Try it » |

**Note:** If you leave out the _line_ value in the fmt parameter, no line will be plotted.

The short color value can be one of the following:

### Color Reference

| Color Syntax | Description |          |
| ------------ | ----------- | -------- |
| 'r'          | Red         | Try it » |
| 'g'          | Green       | Try it » |
| 'b'          | Blue        | Try it » |
| 'c'          | Cyan        | Try it » |
| 'm'          | Magenta     | Try it » |
| 'y'          | Yellow      | Try it » |
| 'k'          | Black       | Try it » |
| 'w'          | White       | Try it » |

***

### Marker Size

You can use the keyword argument `markersize` or the shorter version, `ms` to set the size of the markers.

Set the size of the markers to 20:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, marker = 'o', ms = 20)\
plt.show()
```
![img_matplotlib_marker_o_20](https://user-images.githubusercontent.com/86244964/197048606-133ec461-536c-4cff-bbd5-cdf3c1d3b2d1.png)

# Marker Color

You can use the keyword argument `markeredgecolor` or the shorter `mec` to set the color of the _edge_ of the markers.

Set the EDGE color to red:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array([3, 8, 1, 10])

plt.plot(ypoints, marker = 'o', ms = 20, mec = 'r')\
plt.show()
```
![img_matplotlib_marker_o_mec](https://user-images.githubusercontent.com/86244964/197048836-bd02e7fd-858d-4b91-a869-7849b9d23328.png)

You can use the keyword argument `markerfacecolor` or the shorter `mfc` to set the color inside the edge of the markers.

Set the FACE color to red:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, marker = 'o', ms = 20, mfc = 'r')\
plt.show()
```
![img_matplotlib_marker_o_mfc](https://user-images.githubusercontent.com/86244964/197049063-6fde3e58-dfc3-43c4-a7c0-db7b8acc0f1e.png)

Use _both_ the `mec` and `mfc` arguments to color of the entire marker:

Set the color of both the _edge_ and the _face_ to red:

```python
import matplotlib.pyplot as plt\
import numpy as np

ypoints = np.array(\[3, 8, 1, 10])

plt.plot(ypoints, marker = 'o', ms = 20, mec = 'r', mfc = 'r')\
plt.show()
```
![img_matplotlib_marker_o_mec_mfc](https://user-images.githubusercontent.com/86244964/197049176-fdd98e35-067f-4b29-b11e-85b19dc1f94e.png)

You can also use Hexadecimal color values.

Mark each point with a beautiful green color:

```python
...
plt.plot(ypoints, marker = 'o', ms = 20, mec = '#4CAF50', mfc = '#4CAF50')\
...
```

![img_matplotlib_marker_o_hex](https://user-images.githubusercontent.com/86244964/197049256-0d321a25-64c4-4306-b379-d0a19e4cf697.png)

Or any of the 140 supported color names.

Mark each point with the color named "hotpink":

```python
...
plt.plot(ypoints, marker = 'o', ms = 20, mec = 'hotpink', mfc = 'hotpink')\
...
```
![img_matplotlib_marker_hotpink](https://user-images.githubusercontent.com/86244964/197049374-eaa1c062-00e4-4986-8913-d954106951d7.png)


{% hint style="info" %}
### Want to learn more?

Be sure to sign up for <mark style="color:blue;">**The AI Engineer Master Class**</mark> to get more in depth explanations and video tutorials of end-to-end Machine Learning Projects.&#x20;

:arrow\_down::arrow\_down: Click the link below to sign up and stay up-to-date for new releases! :arrow\_down::arrow\_down:
{% endhint %}

{% embed url="https://www.getrevue.co/profile/dankornas" %}
