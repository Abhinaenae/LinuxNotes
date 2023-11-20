# Sed Basics Notes

sed is a stream editor. A stream editor is used to perform basic text transformations on an input stream (a file or input from a pipeline).  The most common usage of sed involves substituting a pattern or string for another string.

The format for this command is: `sed OPTIONS... [SCRIPT] [INPUTFILE]`

### Examples:
Consider this text file, test.txt, as an input.
```
Hello World!
Hello World!
Hello World!
```

Using the command: `sed 's/Hello/Goodbye' test.txt` will replace the first instance of the word "Hello" with "Goodbye". 

The output will look like this:
```
Goodbye World!
Hello World!
Hello World!
```

To make all the instances of "Hello" turn into "Goodbye", this command will be used: `sed 's/Hello/Goodbye/g test.txt`. 

The substitute flag /g (global replacement) specifies the sed command to replace all the occurrences of the string in the line.
```
Goodbye World!
Goodbye World!
Goodbye World!
```


