# CallGraph.name\_suffix()

Returns a list of call nodes whose corresponding function name has the specified suffix.

```python
from glider import *

def query():
  # Fetch the first contract
  contracts = Contracts().exec(1)
  
  # Get call nodes of functions ending with "Sender" 
  call_nodes = contracts[0].call_graph().name_suffix("Sender")
  for node in call_nodes:
    print(node.function_name())
  return []
```

Output:

```json
{
  "print_output": [
    "_msgSender"
  ]
}
```
