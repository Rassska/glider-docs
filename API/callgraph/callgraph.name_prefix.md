# CallGraph.name\_prefix()

Returns a list of call nodes whose corresponding function name has the specified prefix.

<pre class="language-python"><code class="lang-python">from glider import *

def query():
<strong>  # Fetch the first contract
</strong>  contracts = Contracts().exec(1)
  
  # Get call nodes of functions starting with "_msgSend" 
  call_nodes = contracts[0].call_graph().name_prefix("_msgSend")
  for node in call_nodes:
    print(node.function_name())
  return []
</code></pre>

Output:

```json
{
  "print_output": [
    "_msgSender"
  ]
}
```
