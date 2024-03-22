# Instructions.exec()

Executes the formed query and returns the list of Instruction objects.



```python
from glider import *

def query():
  # Fetch a list of instructions
  instructions = Instructions().exec(2)
  
  return instructions
```

Output:

```json
[
  {
    "contract": "0x798AcB51D8FBc97328835eE2027047a8B54533AD",
    "contract_name": "Context",
    "sol_function": "function _msgSender() internal view virtual returns (address) {
          return msg.sender;
      }",
    "sol_instruction": "{
          return msg.sender;
      }"
  },
  {
    "contract": "0x798AcB51D8FBc97328835eE2027047a8B54533AD",
    "contract_name": "Context",
    "sol_function": "function _msgSender() internal view virtual returns (address) {
          return msg.sender;
      }",
    "sol_instruction": "return msg.sender"
  }
]
```
