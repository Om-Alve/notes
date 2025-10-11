#python 

For writing tests in python we use `pytest`

Install `pytest` with `pip install pytest` / `uv add pytest`
 
Test a function like this:
```python
def func(x):
    return x + 1

def test_answer():
    assert func(3) == 5
```

You can run the tests using the `pytest` command.

`pytest` will run all files of the form test_j*.py or *_test.py in the current directory and its subdirectories.



