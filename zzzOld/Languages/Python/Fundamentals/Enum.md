enums are readable names that are bound to a certain value, this value cannot be changed.
```python
from enum import Enum

class Name(Enum):
	INACTIVE = 0
	ACTIVE = 1

print(Name.ACTIVE.value) #1
print(Name.INACTIVE.value) #0
print(Name(1)) #Name.ACTIVE
print(Name(0)) #Name.INACTIVE
print(Name["ACTIVE"].value) #1
print(list(Name)) #will list what the class Name contains
print(len(Name)) #2 since the class Name only contain two things

```