# List and Dictionary

---

## List

| **Command**                                                       | **Description**                                                                       |
| :---------------------------------------------------------------- | :------------------------------------------------------------------------------------ |
| ``` mylist.append('x') ```                                        | Add single item at last of list (changes original list)                               |
| ``` mylist.extend(list2) ```                                      | Append whole list at last of list (changes original list)                             |
| ``` mylist.insert(pos, elem) ```                                  | Insert elem at pos of list1                                                           |
| ``` mylist.remove(elem) ```                                       | Removes first found elem from list1; gives error if not found                         |
| ``` mylist.index(elem)  ```                                       | Returns index of elem                                                                 |
| ``` mylist.index(elem, i, j) ```                                  | Searches and returns index of elem from mylist[i: j]                                  |
| ``` mylist.pop(index) ```                                         | Removes elem at position index, else removes last item if index not given             |
| ``` mylist.count(elem) ```                                        | Returns count of elem in the list                                                     |
| ``` mylist.sort(key, reverse=True/False)  ```                     | Key is optional user defined function                                                 |
| ``` new_list = sorted(mylist, reverse=False, key=method_name) ``` | unlike sort method, it returns a new                                                  |
| ``` mylist2 = mylist1.copy()        ```                           | Copy list1 to list2                                                                   |
| ``` mylist.clear()                  ```                           | same as del mylist\[:]                                                                |
| ``` mylist.reverse()                ```                           | reverse all items of mylist                                                           |
| ``` filter(method, mylist)          ```                           | Returns iterable for each item of list1 for which 'method' returns true               |
| ``` zip(mylist, mylist2)            ```                           | Zip both lists upto shorter list                                                      |
| ``` max(mylist)                     ```                           | Returns max valued item of mylist                                                     |
| ``` min(mylist)                     ```                           | Returns min valued item of the list                                                   |
| ``` any(mylist)                     ```                           | True if any one of the list item is true; in case of dict, it considers keys only     |
| ``` all(mylist)                     ```                           | True if any all of the list items are true; in case of dict, it considers keys   only |
| ``` enumerate(mylist, start) ``` <br><br> ``` mylist = [1, 2, 55, 52, 23] ``` <br> ``` for key, val in enumerate(mylist, 5):``` <br> &nbsp;&nbsp;&nbsp;&nbsp; ```print(key, val) ``` | 5 1 <br> 6 2 <br> 7 55 <br> 8 52 <br> 9 23 |

## Dictionary

| **Command**                           | **Description**                                                              |
| :------------------------------------ | :--------------------------------------------------------------------------- |
| ``` dict.fromkeys(mylist) ```         | New dictionary with 'list_items: None' key value pair                        |
| ``` mydict.get(key, value2) ```       | Return value of given key, and if key not found, returns value2              |
| ``` mydict.popitem() ```              | Returns and remove arbitrary key: value pair                                 |
| ``` mydict.pop(key) ```               | Remove key: value                                                            |
| ``` mydict.keys() ```                 | List of all keys of mydict                                                   |
| ``` mydict.values() ```               | List of all values of mydict                                                 |
| ``` mydict.update(k2=v2, k3=v3..) ``` | Updating dictionary, if key present update value else add new key:value pair |
| ``` new_dict = sorted(mydict)	```     | Sorted by keys                                                               |
