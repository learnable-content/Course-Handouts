![](headings/2.6.png)

# How To Do File I/O in Python

Now we're going to see how to do **file input-output** in Python.

For starters I have a file called *file_io.txt* with the following contents:

```
John Doe;
350 5th Ave
|
Jane Doe;
100 7th Ave
|
Joe Daniels;
11 1st Ave
```

Open up IDLE since we're working with the local file system.

First of all, we have to open our file:

```py
fileOutput = open('/users/brettromero/test/file_io.txt', 'wt')
```

`open` accepts two parameters: a path to the file and an method of opening it (`wt` means that we want to be able to write to the file).

Writing something to the file is easy:

```py
fileOutput.write('John Doe;\n350 5th Ave\n|\nJane Doe;\n100 7th Ave\n|\nJoe Daniels;\n11 1st Ave\n')
fileOutput.close()
```

`\n` is a new line special character, which basically creates a new file.

Note that after working with the file, it has to be closed using `close()` function.

# 'fileInput'

Now let's open the same file, but only for reading and get its contents:

```py
fileInput = open('/users/brettromero/test/file_io.txt', 'rt')
fileInput.read()
file.close()
```

Using `read()` you basically fetch file's contents. Once again, don't forget to close your files when you are done working with them.