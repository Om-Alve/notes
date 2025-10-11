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
# Now T is bound by BaseModel i.e. Any object should inherit from BaseModel to be considered as type T.
```


