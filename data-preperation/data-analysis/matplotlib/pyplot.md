# Pyplot

{% embed url="https://www.youtube.com/channel/UC5k0oh-js7XWB9bOZ0cRpCQ" %}
<mark style="color:blue;">**Youtube video explanation Coming Soon!**</mark>\
Be sure to subscribe to stay up-to-date with new releases!
{% endembed %}

## Pyplot

Most of the Matplotlib utilities lies under the `pyplot` submodule, and are usually imported under the `plt` alias:

import matplotlib.pyplot as plt

Now the Pyplot package can be referred to as `plt`.

Draw a line in a diagram from position (0,0) to position (6,250):

```python
import matplotlib.pyplot as plt
import numpy as np

xpoints = np.array([0, 6])
ypoints = np.array([0, 250])

plt.plot(xpoints, ypoints)
plt.show()
```

![img\_matplotlib\_pyplot](https://user-images.githubusercontent.com/86244964/197040813-ace82920-82fc-41ee-abf6-33b37e9d5305.png)
