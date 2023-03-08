# Bars

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark>\
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Creating Bars

With Pyplot, you can use the `bar()` function to draw bar graphs.

Draw 4 bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x,y)
plt.show()
```

![img\_matplotlib\_bars1](https://user-images.githubusercontent.com/86244964/197151345-0f2afe65-264f-4259-88fc-4ef3978f1798.png)

The `bar()` function takes arguments that describes the layout of the bars.

The categories and their values represented by the _first_ and _second_ argument as arrays.

## Horizontal Bars

If you want the bars to be displayed horizontally instead of vertically, use the `barh()` function.

Draw 4 horizontal bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.barh(x, y)
plt.show()
```

![img\_matplotlib\_bars2](https://user-images.githubusercontent.com/86244964/197151470-9b49c945-b74c-4b3f-aaef-c68482888c13.png)

## Bar Color

The `bar()` and `barh()` takes the keyword argument `color` to set the color of the bars.

Draw 4 red bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x, y, color = "red")
plt.show()
```

![img\_matplotlib\_bars\_red](https://user-images.githubusercontent.com/86244964/197151557-bc9274a0-9033-4931-aad5-e36acb335e30.png)

### Color Names

You can use any of the 140 supported color names.

Draw 4 "hot pink" bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x, y, color = "hotpink")
plt.show()
```

![img\_matplotlib\_bars\_hotpink](https://user-images.githubusercontent.com/86244964/197151630-934bb7e8-aabf-4844-b58c-070899e40c5d.png)

## Color Hex

Or you can use Hexadecimal color values.

Draw 4 bars with a beautiful green color:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x, y, color = "#4CAF50")
plt.show()
```

![img\_matplotlib\_bars\_green](https://user-images.githubusercontent.com/86244964/197151797-37449c75-60b9-4987-8c08-04cf93083022.png)

## Bar Width

The `bar()` takes the keyword argument `width` to set the width of the bars.

Draw 4 very thin bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x, y, width = 0.1)
plt.show()
```

![img\_matplotlib\_bars\_thin](https://user-images.githubusercontent.com/86244964/197151919-baa54e88-aadb-449d-95d4-ab44014c7a5a.png)

The default width value is 0.8

**Note:** For horizontal bars, use `height` instead of `width`.

## Bar Height

The `barh()` takes the keyword argument `height` to set the height of the bars.

Draw 4 very thin bars:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.barh(x, y, height = 0.1)
plt.show()
```

![img\_matplotlib\_barh\_height](https://user-images.githubusercontent.com/86244964/197151997-c3b180a8-d383-44bc-96b1-fd76b8947271.png)

The default height value is 0.8
