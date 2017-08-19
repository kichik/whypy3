---
title: Annotations
repl: https://repl.it/KGI3/2
---
```python
# add type annotations to variables, arguments and functions
# you can later access those programmatically

# you can also use mypy to check for type errors
# http://mypy-lang.org/

def my_add(a: int, b: int) -> int:
    return a + b

print(my_add(40, 2))  # 42
print(my_add.__annotations__)  # {'a': <class 'int'>, 'b': <class 'int'>, 'return': <class 'int'>}
```
