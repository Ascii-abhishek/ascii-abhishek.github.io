# JSON Module

---

## working with json given as a string:

```py
import json
people_string = ''' {
    "people": [
        {   "name": "abhishek pathak",
            "phone": "8377947140",
            "emails": ["abhishek@gmail.com", "abhishek@hotmail.com"],
            "has_license": false
        },
        {   "name": "jane doe",
            "phone": "0120-4096528",
            "emails": null,
            "has_license": true
        } ]
}
'''
data = json.loads(people_string) 
#to convert json into python object

for person in data['people']: #working on json -> python object
    del person['phone']

new_string = json.dumps(data, indent=2, sort_keys=True) 

# to convert python object into json
# indent paramenter will prettify print(new_string) output
# sort_key will sort items alphabetically
```

## Working with json given as a separate file:

```py
import json

with open('states.json') as f:
    data = json.load(f)

for state in data['states']:
    del state['area_codes']

with open('new_states.json', 'w') as f:
    json.dump(data, f, indent=4)
```

The real life example can be: getting the currency conversion rate from web via request library, which always returns a json response and then converting the desired currency to other form
