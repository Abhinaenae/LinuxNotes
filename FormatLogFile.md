# Awk notes on formatting log files


### Introduction:
Awk is a scripting language used for manipulating data and generating reports. The awk command programming language requires no compiling and allows the user to use variables, numeric functions, string functions, and logical operators. 


### What does Awk do?
  1. Scans a file line by line 
  2. Splits each input line into fields 
  3. Compares input line/fields to pattern 
  4. Performs action(s) on matched lines 

### Use Cases:
  1. Transform data files
  2. Produce formatted reports

### Structure of the awk command?
`awk options 'selection _criteria {action }' input-file > output-file`

### Built-in variables in awk:
- Awk’s built-in variables include the field variables—$1, $2, $3, and so on ($0 is the entire line) — they break a line of text into individual fields. 

- NR: NR command keeps a current count of the number of input records.
- NF: NF command keeps a count of the number of fields within the current input record.
- FS: FS command contains the field separator character which is used to divide fields on the input line. The default is a “white space”, which is space and tab characters.
- RS: RS command stores the current record separator character. The default record separator character is a newline. 
- OFS: OFS command stores the output field separator, which separates the fields when Awk prints them. The default is a blank space.
- ORS: ORS command stores the output record separator, which separates the output lines when Awk prints them. The default is a newline character. print automatically outputs the contents of ORS at the end of whatever it is given to print.

### Examples:
Here, the example log file I will be using is "employees.txt":
```
  abhi developer devops 120000
  james manager devops 180000
  ashlin manager security 200000
  lebron director devops 340000
  tarun developer security 150000
  deepak analyst security 80000
  lily analyst devops 70000
  satvik director marketing 800000
```
#### Example 1:
The default behavior of awk is printing every line of data from the file.
With the command:
 ` $ awk '{print}' employee.txt`

we will get this as the output:
```
  abhi developer devops 120000
  james manager devops 180000
  ashlin manager security 200000
  lebron director devops 340000
  tarun developer security 150000
  deepak analyst security 80000
  lily analyst devops 70000
  satvik director marketing 800000
 ```

#### Example 2:
Another example where we input:
 ` awk '/developer/ {print}' employee.txt `
will print the lines where "developer" matches in.

the output is:
  ```
  abhi developer devops 120000
  tarun developer security 150000
```

#### Example 3:
`awk 'NR==5, NR==8 {print NR,$0}' employee.txt` will print lines 5-8 with a line number.

output:
```
5 tarun developer security 150000
6 deepak analyst security 80000
7 lily analyst devops 70000
8 satvik director marketing 800000
```

#### Example 4:


END(for now)

