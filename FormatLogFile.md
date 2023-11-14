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
awk options 'selection _criteria {action }' input-file > output-file

### Examples:
Here, the example log file I will be using is "employees.txt":
`
  abhi developer devops 120000
  james manager devops 180000
  ashlin manager security 200000
  lebron director devops 340000
  tarun developer security 150000
  deepak analyst security 80000
  lily analyst devops 70000
  satvik director marketing 800000
`
#### Example 1:
The default behavior of awk is printing every line of data from the file.
With the command:
 ` $ awk '{print}' employee.txt`

we will get this as the output:
` abhi developer devops 120000
  james manager devops 180000
  ashlin manager security 200000
  lebron director devops 340000
  tarun developer security 150000
  deepak analyst security 80000
  lily analyst devops 70000
  satvik director marketing 800000 `

#### Example 2:
Another example where we input:
 ` awk '/developer/ {print}' employee.txt `
will print the lines where "developer" matches in.

the output is:
  `abhi developer devops 120000
  tarun developer security 150000`


END(for now)
