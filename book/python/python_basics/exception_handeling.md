# Exception Handeling

---

```python
try:
	something
	raise Exception        #throw an exception
except (FileNotFoundError, OtherError, ...) as e:
	print(e)
except Exception as e:     #parent exception
	print(e)
else:
	print("if none of above described error found")
finally:
	print("will run, no matter what")
```
	

**Note:** The codes inside finally will be executed no matter whether there was an exception or not. If there is a "return" or "exit" inside the exception blocks, before returning or existing, the finally codes will still be executed.
