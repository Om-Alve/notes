#python 

Python doesn't support traditional function overloading in the same way as `Java` or `cpp`. 

We can use the `@overload` decorator from the `typing` module to enable type-checking for overloaded functions.

Here's an example:
```python

@overload
def add(a: str, b: str) -> str:
	...

@overload
def add(a: int, b: int) -> int:
	...

# Actual implementation of the function
def add(a, b):
	if isinstance(a, str) and isinstance(b, str):
		return f"{a} + {b}"
	else:
		return a + b
```

Reference:
[typing docs](https://typing.python.org/en/latest/spec/overload.html)