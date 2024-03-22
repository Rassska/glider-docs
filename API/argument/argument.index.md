# Argument.index

Returns the index of the argument.

```python
def query():
  functions = Functions().exec(100)

  function_with_args = []
  for f in functions:
    # Prepare the object for this function
    function = {"Function Name": f.name(), "Arguments": []}

    # For each of its arguments...
    for arg in f.arguments().list():
      # ...return the data of the argument
      function["Arguments"].append({"Argument Index": arg.index})
      function_with_args.append(function)

  return function_with_args
```

