# Argument.data

Returns the data of the Argument&#x20;

It contains the name, name\_ssa, canonical\_name, type and memory\_type of the Argument.

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
      function["Arguments"].append({"Argument data": arg.data})
      function_with_args.append(function)

  return function_with_args
```

Output:

```json
{
  "Function Name": "transferOwnership",
  "Arguments": [
    {
      "Argument data": {
        "name": "newOwner",
        "name_ssa": "newOwner_0",
        "canonical_name": "Ownable.transferOwnership(address).newOwner",
        "type": "address",
        "memory_type": "memory"
      }
    }
  ]
}
```
