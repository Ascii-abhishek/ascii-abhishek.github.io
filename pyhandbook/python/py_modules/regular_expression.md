# RE (Regular Expression) Module

---

| **Command**         | **Description**                                                                                                    |
| :------------------ | :----------------------------------------------------------------------------------------------------------------- |
| .                   | Any character   except new line                                                                                    |
| \d                  | Digit (0 - 9)                                                                                                      |
| \D                  | Not a Digit                                                                                                        |
| \w                  | Word character (a-z, A-Z, 0-9, _)                                                                                  |
| \W                  | Not a word character                                                                                               |
| \s                  | Whitespace (space,   tab, newline)                                                                                 |
| \S                  | Not whitespace                                                                                                     |
| \b                  | Word boundary #\bha means space or nothing before 'ha'                                                             |
| \B                  | Not a word boundary                                                                                                |
| ^                   | Beginning of a string                                                                                              |
| $                   | End of a string                                                                                                    |
| []                  | Matches characters in bracket, no need for \ inside in case of escape characters,```[1-7] == [1234567] != [-17]``` |
| `[^ ]`              | Matches characters not in bracket, ```[^a-c]``` == all letters except a,b,c                                        |
| &#124;              | Either Or                                                                                                          |
| ()                  | Group                                                                                                              |
|                     |                                                                                                                    |
| **Quantifiers**     |                                                                                                                    |
| *                   | 0 or more                                                                                                          |
| +                   | 1 or more                                                                                                          |
| ?                   | 0 or 1                                                                                                             |
| {3}                 | Exact number                                                                                                       |
| {3, 4}              | Range of numbers (minimum, maximum)                                                                                |
| **Meta Characters** |                                                                                                                    |
| .[{()\^$?*+         | need to be escaped by \ (back slash)                                                                               |
<br>

| Text                                                                                     | Regular Expression                                                 |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| abcdefghijklmnopqurtuvwxyz <br> ABCDEFGHIJKLMNOPQRSTUVWXYZ <br> 1234567890               |                                                                    |
| Ha <br> HaHa                                                                             | ``` \bHa (using word boundary)                    ```              |
| abhishekpathak.com                                                                       | ``` \w+\.com                                      ```              |
| 321-555-4321 <br>     123.555.1234                                                       | ``` \b{3}[-.]\b\{3}[-.]\b{4}                      ```              |
| Mr. Schafer<br>Mr Smith<br>Ms David<br>Mrs. Robinson<br>Mr. T                            | <code> M(r\&#124;s\&#124;rs)\.?\s[A-Z]\w*    </code>               |
| cat<br>mat<br>pat<br>bat                                                                 | ``` [^b]at                                        ```              |
| CoreyMSchafer@gmail.com<br>corey.schafer@university.edu<br>corey-321-schafer@my-work.net | <code> [a-zA-Z0-9.-]+@[a-zA-Z-]+\.(com\&#124;edu\&#124;net)</code> |
| All kind of email addresses                                                              | ``` [a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+```              |

```python
# raw string: print("\tTab"): ____Tab ; print(r"\tTab"): \tTab
import re
search_in_text = """
			   abcdefghijklmnopqurtuvwxyz
			   ABCDEFGHIJKLMNOPQRSTUVWXYZ
			   1234567890
			   """
pattern = re.compile(r'regular_expression_here')
searches = pattern.finditer(search_in_text)
for search in searches:
    print(search)```