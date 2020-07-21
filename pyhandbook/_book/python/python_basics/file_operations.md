# Working with Files (File IO)

---

```python
with open('abc.txt', 'r') as f:
    f.name
    f.mode # r (read)
    f.closed # False
    f.read(size=n) # after n characers seek to next character
    f.readline() # return first line and seek to start of second line
    f.tell() # current seek position
    f.seek(0) # 0: start; 1: current; 2:end of the file
    for line in f:
        print(line, end='') # print each line

with open('abcd.txt', 'w') as f:
    # w: overwrite; a: append
    f.write('text')
    # if we f.write() again in same open block. text will be appended
          
# copy from one file to other
with open('abc.txt', 'r') as rf:
    with open('abcd.txt', 'w') as wf:
        for line in rf:
            wf.write(line)

# make a copy of image file
with open('abc.jpg', 'rb') as rf:
    with open('abcd.jpg', 'wb') as wf:
        for line in rf:
            wf.write(line)

```

## Here is a list of the different modes of opening a file:
- ```r```\
Opens a file for reading only. The file pointer is placed at the beginning of the file. This is the default mode.

- ```rb``` \
Opens a file for reading only in binary format. The file pointer is placed at the beginning of the file. This is the default mode.

- ```r+```\
Opens a file for both reading and writing. The file pointer will be at the beginning of the file.

- ```rb+```\
Opens a file for both reading and writing in binary format. The file pointer will be at the beginning of the file.

- ```w```\
Opens a file for writing only. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing.

- ```wb```\
Opens a file for writing only in binary format. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing.

- ```w+```\
Opens a file for both writing and reading. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing.

- ```wb+```\
Opens a file for both writing and reading in binary format. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing.

- ```a```\
Opens a file for appending. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing.

- ```ab```\
Opens a file for appending in binary format. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing.

- ```a+```\
Opens a file for both appending and reading. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing.

- ```ab+```\
Opens a file for both appending and reading in binary format. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing.