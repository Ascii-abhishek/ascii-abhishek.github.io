# Python Basics

___

## Common Methods and Description

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg .tg-34fe{background-color:#404040;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-zlqz{font-weight:bold;background-color:#404040;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-5nj1{font-family:"Lucida Console", Monaco, monospace !important;;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-zlqz">Method</th>
    <th class="tg-34fe"><span style="font-weight:bold">Description</span></th>
  </tr>
  <tr>
    <td class="tg-5nj1">type(obj)</td>
    <td class="tg-0pky">Returns class type of argument</td>
  </tr>
  <tr>
    <td class="tg-5nj1">id(obj)</td>
    <td class="tg-0pky">Retuens unique id associated with object</td>
  </tr>
  <tr>
    <td class="tg-5nj1">dir(class / module)</td>
    <td class="tg-0pky">Returns all methods available</td>
  </tr>
  <tr>
    <td class="tg-5nj1">sys.path</td>
    <td class="tg-0pky">List of locations where python looks for modules to import</td>
  </tr>
  <tr>
    <td class="tg-5nj1">abc.__doc__</td>
    <td class="tg-0pky">Print class or method documentation</td>
  </tr>
  <tr>
    <td class="tg-5nj1">def function():<br>&nbsp;&nbsp;&nbsp;&nbsp;"""documentation"""<br></td>
    <td class="tg-0pky">Documentation about method to show in __doc__ method</td>
  </tr>
  <tr>
    <td class="tg-5nj1">map(lambda t: t*2, mylist)</td>
    <td class="tg-0pky">Map each item of mylist to lambda function</td>
  </tr>
  <tr>
    <td class="tg-5nj1">FALSE,<br>None,<br>0,<br>" ", ( ), [ ], { }<br></td>
    <td class="tg-0pky">All evelutes to false</td>
  </tr>
  <tr>
    <td class="tg-5nj1">len(iterable)</td>
    <td class="tg-0pky">Returns length of iterable object</td>
  </tr>
  <tr>
    <td class="tg-5nj1">def function(*args, **kwargs):<br>&nbsp;&nbsp;&nbsp;&nbsp;print(args)<br>&nbsp;&nbsp;&nbsp;&nbsp;print(kwargs)<br></td>
    <td class="tg-0pky"><br>function('math', 'art', name='dev', age=20)<br><br>args = positional arguments =&gt; ('math', 'art')<br>kwargs = keyword arguments =&gt; {'name': 'dev', 'age': 20}</td>
  </tr>
  <tr>
    <td class="tg-5nj1">python -m http.server<br># localhost:8000<br>python -m http.server 7800<br># localhost:7800</td>
    <td class="tg-0pky">Run a local test server</td>
  </tr>
  <tr>
    <td class="tg-5nj1">python -m pydoc -p 1234<br># localhost:1234</td>
    <td class="tg-0pky">Open python documentation on local server</td>
  </tr>
  <tr>
    <td class="tg-5nj1">import timeit<br>timeit.timeit(my_func())</td>
    <td class="tg-0pky">Measure execution time</td>
  </tr>
  <tr>
    <td class="tg-5nj1">__bool__():<br>&nbsp;&nbsp;&nbsp;&nbsp;return False<br><br>__len__():<br>&nbsp;&nbsp;&nbsp;&nbsp;return 0</td>
    <td class="tg-0pky">Only cases when object is considered false if its defines any of these methods, else its always considered true</td>
  </tr>
</table>
<br>

## Duck Typing

Duck typing is a concept that says that the “type” of the object is a matter of concern only at runtime and you don’t need to to explicitly mention the type of the object before you perform any kind of operation on that object. The following example can help in understanding this concept -

```python
def calc(a,b):
    return a+b
```

Now, Python says that for the above function I don’t need to be concerned about the “type” of the objects ‘a’ & ‘b’ and that the type will be taken care of during runtime as long as the objects support the ‘+’ . So, keeping this in mind the above function will work for any “type” of object which supports the operator + i.e. it will return valid values for a string, list or Integer.
