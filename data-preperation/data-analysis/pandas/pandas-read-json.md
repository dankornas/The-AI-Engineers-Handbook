# Pandas Read JSON

***

### Read JSON

Big data sets are often stored, or extracted as JSON.

JSON is plain text, but has the format of an object, and is well known in the world of programming, including Pandas.

In our examples we will be using a JSON file called 'data.json'.

Open data.json.

#### Example

Load the JSON file into a DataFrame:

import pandas as pd

df = pd.read\_json('data.json')

print(df.to\_string())&#x20;

Try it Yourself »

**Tip:** use `to_string()` to print the entire DataFrame.

***

### Dictionary as JSON

**JSON = Python Dictionary**

JSON objects have the same format as Python dictionaries.

If your JSON code is not in a file, but in a Python Dictionary, you can load it into a DataFrame directly:

#### Example

Load a Python Dictionary into a DataFrame:

import pandas as pd

data = {\
&#x20; "Duration":{\
&#x20;   "0":60,\
&#x20;   "1":60,\
&#x20;   "2":60,\
&#x20;   "3":45,\
&#x20;   "4":45,\
&#x20;   "5":60\
&#x20; },\
&#x20; "Pulse":{\
&#x20;   "0":110,\
&#x20;   "1":117,\
&#x20;   "2":103,\
&#x20;   "3":109,\
&#x20;   "4":117,\
&#x20;   "5":102\
&#x20; },\
&#x20; "Maxpulse":{\
&#x20;   "0":130,\
&#x20;   "1":145,\
&#x20;   "2":135,\
&#x20;   "3":175,\
&#x20;   "4":148,\
&#x20;   "5":127\
&#x20; },\
&#x20; "Calories":{\
&#x20;   "0":409,\
&#x20;   "1":479,\
&#x20;   "2":340,\
&#x20;   "3":282,\
&#x20;   "4":406,\
&#x20;   "5":300\
&#x20; }\
}

df = pd.DataFrame(data)

print(df)&#x20;

Try it Yourself »

***

***

\
