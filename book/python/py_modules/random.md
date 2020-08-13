# Random Module

---

```import random```

| **Command**                     | **Description**                                             |
| :------------------------------ | :---------------------------------------------------------- |
| ```random.random() ```          | float number [0, 1)                                         |
| ```random.uniform(1, 10)```     | like above, just takes parameters                           |
| ```random.randint(1, 6) ```     | integer numbers [1, 6]                                      |
| ```random.choice(arr)```        | random value from given array 'arr'                         |
| ```random.choices(arr, k=10)``` | list of 10 random values chosen from array, repeated values |
| ```random.shuffle(arr) ```      | same no of elemnts but indexes changed                      |
| ```random.sample(arr, k=5) ```  | 5 unique and random elemnts from arr                        |

```arr = ['red', 'black', 'green']``` <br>
```random.choices(arr, weigths=[18, 18, 2], k=10)``` >>
probabity of red = 18/(18+18+2=38); black = 18/38; green = 2/38 
