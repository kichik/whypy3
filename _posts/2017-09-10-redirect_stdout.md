---
title: redirect stdout
repl: https://repl.it/KuF6
---
```python
import io
from contextlib import redirect_stdout

# Easy redirect sys.stdout to another file or file-like object

f = io.StringIO()
with redirect_stdout(f):
    import this
f.getvalue()

# You could easily redirect stdout to a file:

with open('import_this.txt', 'w') as f:
    with redirect_stdout(f):
        import this

# You could also make a custom StringIO with a complex behavior

class CaptureStdOutput(io.StringIO):
    """Captures IO stream and emit a signal."""

    def write(self, text):
        """Do something awesome instead of writing to std."""
        pass

d = CaptureStdOutput()
with redirect_stdout(d):
    import this
d.getvalue()

# In python2 you should overwrite sys.stdout
# and pull it back after redirecting the output
import sys
stdout = sys.stdout
sys.stdout = open('import_this.txt', 'w')
import this
sys.stdout = stdout
```
