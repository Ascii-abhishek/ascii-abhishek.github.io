# Strings and Numbers

---

## Strings

``` import string as s ```

| **Command**              | **Description**                                                                                                |
| :----------------------- | :------------------------------------------------------------------------------------------------------------- |
| ```s.ascii_letters ```   | abc...zABC....Z                                                                                                |
| ```S.ascii_lowercase ``` | abc.....z                                                                                                      |
| ```S.ascii_uppercase ``` | ABCD....Z                                                                                                      |
| ```S.digits ```          | 0123456789                                                                                                     |
| ```S.hexdigits ```       | 0123456789abcdefABCDEF                                                                                         |
| ```S.octdigits ```       | 01234567                                                                                                       |
| ```S.punctutaion ```     | !"#$%&'()*+,-./:;<=>?@\[\\]^_`{}~                                                                              |
| ```S.whitespace ```      | Space, tab, return                                                                                             |
| ```S.printable ```       | 0123456789 <br>abcdefghijklmnopqrstuvwxyz <br>ABCDEFGHIJKLMNOPQRSTUVWXYZ <br> !"#$%&'()*+,-./:;<=>?@\[\]^_`{}~ |
	
	 
``` mystr = "Abhishek" ```

| **Command**                                                    | **Description**                                                                                    |
| :------------------------------------------------------------- | :------------------------------------------------------------------------------------------------- |
| ``` mystr.capitalize()  ```                                    | Abhishek                                                                                           |
| ``` mystr.count(substr, start, end) ```                        | Count number of substr present in mystr[start: end]                                                |
| ``` mystr.encode(encoding='utf-8')  ```                        | b'abhishek'                                                                                        |
| ``` mystr.find(substr, start, end) ```<br>```mystr.rfind() ``` | Returns index of substring if found <br>rfind finds substring from right side of mystr             |
| ``` mystr.index('shek') ```                                    | 4;<br>Just like find(), but it gives error if substring not found                                  |
| ``` mystr.islower()    ```                                     | True                                                                                               |
| ``` mystr.partition('s')    ```                                | ('abhi', 's', 'hek')                                                                               |
| ``` mystr.replace(old, new, count)   ```                       | Replces old substring with new upto count number of times                                          |
| ``` mystr.startswith('abhi')  ```                              | True                                                                                               |
| ``` mystr.strip('abc')   ```                                   | Strips a, b, c from both sides of the string                                                       |
| ``` mystr.zfill(width)   ```                                   | Fill each side of mystr with 0 to obtain 'width' length                                            |
| ``` mystr.join(mystr2)   ```                                   | better than mystr + mystr2 because + make a third new string resulting in a quadratic runtime cost |
| ``` mystr.swapcase()   ```                                     | return   string after changing cases of each character                                             |
| ``` mystr.title()   ```                                        | 'Hello   dev'.title() ==> Hello Dev                                                                |
| ```mystr.endswith(('abc', 'xyz', 'pqr'))```                    | False |
| ``` mystr.```<br>```isalpha()```<br>```isdecimal() ```<br>```isdigit()```<br>```isidentifier()```<br>```isnumeric()```<br>```isspace()```<br>```istitle() ``` | Self explainatory |
| ``` mystr.```<br>``` center(length,   fillchar) ```<br>```ljust(length,   fillchar)```<br>```rjust(length,   fillchar) ```<br>```lstrip('chars')``` | Fill  both sides of string by 'fillchar' upto given length<br>lstrip: The chars argument is a string specifying the set of characters to be removed |

### String Formatting

| **Command**                       | **Description**                 |
| :-------------------------------- | :------------------------------ |
| ``` "{!r}".format(mystr) ```      | repr(mystr)                     |
| ``` "{!s}".format(mystr) ```      | str(mystr)                      |
| ``` "{0:d}".format(42) ```        | 42 (decimal)                    |
| ``` "{0:x}".format(42) ```        | 2a (hexdecimal)                 |
| ``` "{0:o}".format(42) ```        | 52 (octal)                      |
| ``` "{0:b}".format(42) ```        | 101010                          |
| ``` "{:,}".format(1234567890) ``` | 1,234,567,890                   |
| ``` "{:.2f}".format(12.3456) ```  | 12.34 (upto two decimal points) |

## Numbers

| **Command**            | **Description**                 |
| :--------------------- | :------------------------------ |
| ```abs(num)```         | absolute value                  |
| ```round(num, upto)``` | rounded up number upto decimals |
| ```int(num)```         | cast to integer                 |
