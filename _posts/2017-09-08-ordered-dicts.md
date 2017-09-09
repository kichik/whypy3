---
title: ordered dictionaries
repl: https://repl.it/KruF/0
---
```python
# Dictionaries maintain their order and use 20 - 25% less memory

my_dict = {'one': 1, 'two': 2, 'three': 3, 'four': 4,
           'five': 5, 'six': 6, 'seven': 7, 'eight': 8,
           'nine': 9, 'ten': 10}

print(my_dict)
# {'one': 1, 'two': 2, 'three': 3, 'four': 4,
# 'five': 5, 'six': 6, 'seven': 7, 'eight': 8,
# 'nine': 9, 'ten': 10}

from sys import getsizeof
print(getsizeof(my_dict)) # 368

# in python2 the order is not preserved and the memory footprint is greater
# https://repl.it/KruM/0

print(my_dict)
# {'four': 4, 'seven': 7, 'five': 5, 'three': 3,
# 'ten': 10, 'eight': 8, 'nine': 9, 'six': 6,
# 'two': 2, 'one': 1}

print(getsizeof(my_dict)) # 664
```
