# Percision, Recall & F1

Precision, recall, and F1 score are metrics used to evaluate the performance of a machine learning model, especially in classification tasks. These metrics are commonly used in situations where the classes in the data are imbalanced, meaning that one class is much more common than the others.

### Precision

Precision is the proportion of correct positive predictions made by the model. In other words, it is the number of true positive predictions divided by the total number of positive predictions. For example, if a model makes 100 positive predictions and 80 of them are correct, the model's precision is 80%.

```python
import numpy as np
from sklearn.metrics import precision_score

# Calculate the precision
y_true = [0, 1, 1, 0, 1, 0]
y_pred = [0, 1, 0, 0, 0, 1]
precision = precision_score(y_true, y_pred)

# Print the precision
print("Precision:", precision)
```

### Recall

Recall is the proportion of positive cases that the model correctly identifies. In other words, it is the number of true positive predictions divided by the total number of actual positive cases. For example, if there are 100 positive cases in the data and the model correctly identifies 80 of them, the model's recall is 80%.

```python
import numpy as np
from sklearn.metrics import recall_score

# Calculate the recall
y_true = [0, 1, 1, 0, 1, 0]
y_pred = [0, 1, 0, 0, 0, 1]
recall = recall_score(y_true, y_pred)

# Print the recall
print("Recall:", recall)
```

### F1 Score

F1 score is a combination of precision and recall, and is calculated as the harmonic mean of precision and recall. The F1 score is a useful metric because it takes into account both the precision and the recall of the model, and therefore provides a more balanced evaluation of the model's performance.

```python
import numpy as np
from sklearn.metrics import f1_score

# Calculate the F1 score
y_true = [0, 1, 1, 0, 1, 0]
y_pred = [0, 1, 0, 0, 0, 1]
f1 = f1_score(y_true, y_pred)

# Print the F1 score
print("F1 score:", f1)
```

### Summary

In summary, precision, recall, and F1 score are important metrics to consider when evaluating the performance of a machine learning model, especially in classification tasks where the classes are imbalanced. These metrics provide a more complete and nuanced picture of the model's performance than accuracy alone.
