---
title: ExitStack
repl: https://repl.it/Km22/0
---
```python
from contextlib import ExitStack

with ExitStack() as stack:
  files = [stack.enter_context(open(fname)) for fname in ['/etc/hosts', 'nosuchfile']]
  # All opened files will automatically be closed at the end of
  # the with statement, even if attempts to open files later
  # in the list raise an exception
```
