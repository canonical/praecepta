This example should result in two warnings.

# The heading should be ignored

This line that contain # and // in the middle should also be ignored.

```python
# This line should be flagged
print("Hello, world!")  # This line should be ignored
```

```
 # This line should be ignored
$> This line should be flagged
% > This line should be flagged
print("Hello, world!") // This line should be ignored
```

> This line should be ignored
