#python 

Python generics are type hints in Python that allow you to write functions and classes that can work with any data type.

```python
from typing import TypeVar

T = TypeVar('T')

def add(a: T, b: T) -> T:
	return a + b

print(add(1,2)) #-> 3
print(add("a", "b")) #-> ab
```

You can also bind generic types to certain classes:
```python
from typing import TypeVar
from pydantic import BaseModel

T = TypeVar("T", bound=BaseModel)
# Now T is bound by BaseModel i.e. Any object must be a subtype of BaseModel to be used in place of T.
```

How to make a generic class?

```python
from typing import TypeVar, Generics

T = TypeVar("T")

class Box(Generics[T]):
	def __init__(self, item: T):
		self.item = item
	
	def get_item(self) -> T:
		return self.item
	
box_of_int = Box(1)

print(box_of_int.get_item())

box_of_str = Box("one")

print(box_of_str.get_item())
```
