# Context Manager

---

```python
with open('sample.txt', 'w') as f:
    f.write('Testing')
```	
## What is happening behind (using class):

```python
class Open_file():
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode

    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file

    def __exit__(self, exc_type, exc_val, traceback):
        self.file.close()


with Open_file('sample.txt', 'w') as f:
    f.write('Testing')

```

## What is happening behind (using method):

```python
from contextlib import contextmanager

@contextmanager
def open_file(file, mode):
    try:
        f = open(file, mode)
        yield f
    finally:
        f.close()

with open_file('sample.txt', 'w') as f:
    f.write('Testing')
	
```
	
In a similar way (using method) we can create our own context managers so that some specific task will execute for sure even if we forget to execute that explicitly
