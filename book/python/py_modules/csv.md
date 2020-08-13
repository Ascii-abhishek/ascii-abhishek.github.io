# CSV Module

```py
import csv

with open('abc.csv', 'r') as csv_file:
    csv_reader = csv.reader(csv_file)
    # csv_reader is like file object. we have to work on it
    
    next(csv_reader) # to skip first row after here
    for line in csv_reader:
        print(line)

with open('abc.csv', 'r') as csv_file:
    csv_reader = csv.reader(csv_file)
    
    with open('new_names.csv', 'w') as new_file:
        csv_writer = csv.writer(new_file, delimiter='-')
        csv_writer.writeheader() # first row
        for line in csv_reader: # also print first row
            csv_writer.writerow(line)

with open('abc.csv', 'r') as csv_file:
    csv_reader = csv.DictReader(csv_file)

    with open('new_names.csv', 'w') as new_file:
        fieldnames = ['first', 'second', 'third']

        csv_writer = csv.DictWriter(new_file, fieldnames=fieldnames, delimiter=',')
    
        for line in csv_reader:
            csv_writer.writerow(line)
            # print as a dictionary, first row values as key for each line values
```