# Python List and Dictionary

___

## List

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-7btt{font-weight:bold;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-amwm{font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-lrah{font-size:13px;font-family:"Lucida Console", Monaco, monospace !important;;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-7btt">Command</th>
    <th class="tg-amwm">Description</th>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.append('x')</td>
    <td class="tg-0lax">Add single item at last of list (changes original list)</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.extend(list2)</td>
    <td class="tg-0lax">Append whole list at last of list (changes original list)</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.insert(pos, elem)</td>
    <td class="tg-0lax">Insert&nbsp;&nbsp;elem at pos of list1</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.remove(elem)</td>
    <td class="tg-0lax">Removes first found elem from list1; gives error if not found</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.index(elem)</td>
    <td class="tg-0lax">Returns index of elem, if i and j are given then search in list[i: j]</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.index(elem, i, j)</td>
    <td class="tg-0lax">Make a requirement text file for project export</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.pop(index)</td>
    <td class="tg-0lax">Removes elem at position index, else removes last item if index not given</td>
  </tr>
  <tr>
    <td class="tg-lrah">mylist.count(elem)</td>
    <td class="tg-0lax">Returns count of elem in the list</td>
  </tr>
</table>

___

## Dictionary

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-8jda{font-size:13px;font-family:"Lucida Console", Monaco, monospace !important;;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-7btt{font-weight:bold;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-7btt">Command</th>
    <th class="tg-7btt">Description</th>
  </tr>
  <tr>
    <td class="tg-8jda">dict.fromkeys(mylist)</td>
    <td class="tg-0pky">New dictionary with 'list_items: None' key-value pair</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.get(key, value2)</td>
    <td class="tg-0pky">Return value of given key, and if key not found, returns value2</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.popitem()</td>
    <td class="tg-0pky">Returns and remove arbitrary key: value pair</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.pop(key)</td>
    <td class="tg-0pky">Remove key: value</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.keys()</td>
    <td class="tg-0pky">List of all keys of mydict</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.values()</td>
    <td class="tg-0pky">List of all values of mydict</td>
  </tr>
  <tr>
    <td class="tg-8jda">mydict.update(k2=v2, k3=v3..)</td>
    <td class="tg-0pky">Updating dictionary, if key present update value else add new key:value pair</td>
  </tr>
  <tr>
    <td class="tg-8jda">new_dict = sorted(mydict)</td>
    <td class="tg-0pky">Returns mydict after sorting by keys<br>  </td>
  </tr>
</table>
<br>