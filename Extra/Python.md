# Programming in Python Certification
Meta Certification on coursera

## Understaining scopes
 - Local scope: refers to a variable declared inside a function.
 - Enclosing scope: refers to a function inside another function or what is commonly called a nested function.
 - Global scope: is when a variable is declared outside of a function. This means it can be accessed from anywhere.

``` py
# Local scope
def get_total(a, b):
    #local variable declared inside a function
    total = a + b;
    return total

print(get_total(5, 2))
# 7

# Accessing variable outside of the function:
print(total)
NameError: name 'total' is not defined
```

## List
Lists are a sequence of one or more different or similar datatypes. A list in Python is essentially a dynamic array that can hold any datatype.

### Methods 
To add elements:
 - insert(index, element): It puts the element in the index position in the list desired
 - append(element): Not index is needed add the element at the end of the list
 - extend(element): It permits to add one or multiple elements to a list, you can pass a list inclusive

 - ```py
   list1 = [0,1]

   list1.insert(1, 2) #[0,2,1]
   list1.append(2) #[0,1,2]
   list1.extend([2,3,4]) #[0,1,2,3,4]
   ```

To delete elements:
 - pop(index): deletes the element in that index position
 - delete or del list[index]: deletes the element in that index position


## Tuple
They're used as data structures and help to create solid, well performing code. To declare a tuple, I declare a simple variable.

The difference with a list is that a tuple is **inmutable**
```py
my_tuple = (1, "hola", 4.5, True)

#Access elements
print(my_tuple[1]) #"Hola"
print(type(my_tuple)) # "<class 'tuple'>
```

### Methods:
- count("dataType"): It returns the number of occurrences of that value within the tuple
- index(element): It returns the index where the element is in the tuple


## Sets
Sets differ slightly from lists, in that they don't allow duplicate values.
Are declared in curly braces. And sets doesn't contain an ordered index

### Methods:
- remove or discard(element): Deletes that element in the set
- union: Can join two set discarting the duplicated values (set.union or |)
- intersection: The items that match (.intersection or &)
- difference: The first minus the second (-)
- symmetric_diference (^)

```py
my_set = {1, 2, 3, 4, 5}

my_set.remove(2) # {1, 3, 4, 5}
my_set.discard(2)
```

## Dictionaries
Diccionaries access values by keys (key: value), it's faster than using a list. Doesn´t allow duplicated keys
```py
sample_dict = {1: "Cafe", 2: "Tea"}
sample_dict[2] = "Juice" # Change the value

del sample_dict[2]

# Access to the key value pair
for key, value in sample_dict.items():
 print(key + " : " + value)

```

## Args and kargs
When I pass args, I'm allowed to pass as many args as needed
To summarize, with args, you could pass in any amount of non-keyword variables. With the kwargs, you can pass in any amount of keyword arguments. That's a simple intro to both args and kwargs.
```py
def sum_of(a,b):
    return a + b

print(sum_of(4,5)) #9
print(sum_of(4, 5, 6)) # Error

# Handle it
def sum(*args):
    sum = 0
    for x in args:
        sum += x
    retur sum

# Now kwargs?
def sum_of(**kwargs):
    sum = 0
    for k, v in kwargs.items():
        sum += v
    return sum

print(sum_of(coffee = 2.99, cake = 4.55)) 
```

## Which data structure to choose?
There can be many factors to select from, including size, speed and performance. The best way to try and understand which one is more suitable is through an example.

### Example: Employees list
In this example, there's a list of employees that work in a restaurant. You need to be able to find an employee by their employee ID - an integer-based numeric ID. The function get_employee contains a for loop to iterate over the list of employees and returns an employee object if the ID matches.

```py
# The hard way
employee_list = [{"id": 12345, "name": "John", "department": "Kitchen"}, {"id": 12458, "name": "Paul", "department": "House Floor"}]

def get_employee(id): 
    for employee in employee_list:
        if employee['id'] == id:
            return employee

print(get_employee(12458));
## OUTPUT
{'id': 12458, 'name': 'Paul', 'department': 'House Floor'}

# More convinient
employee_dict = {
    12345: {
        "id": "12345",
        "name": "John", 
        "department": "Kitchen"    
    },
    12458: {
        "id": "12458",
        "name": "Paul", 
        "department": "House Floor"    
    }
}

def get_employee_from_dict(id):
    return employee_dict[id];


print(get_employee_from_dict(12458));
## OUTPUT
{'id': 12458, 'name': 'Paul', 'department': 'House Floor'}

```

Notice how, in this code block, if you change the data structure to use a dictionary, it will allow you to find the employee. The main difference is that you no longer need to iterate over the list to locate them. If the list expands to a much larger size, the seek time to find the employee stays the same. 

## Exception Handling
It solves to whow errors in a more user-friendly way.
The try statement will try and execute the code that you added inside it. If an exception occurs, it will trigger the except line and execute any code added underneath the except statement, but Python allows you to make the except statement more specific.
```py
def divide_by(a,b):
   return a / b

print(divide_by(40,0)) # Error

# Solution: try and except blocks
try:
    ans = divide_by(40, 0)
except:
    print("Uppsss, something went wrong")

# Adding the exception
try:
    ans = divide_by(40, 0)
except Exception as e:
    print("Uppsss, something went wrong", e)
    print(e.__class__) # Print the class of the error

# Being more specific in feedback
try:
    ans = divide_by(40, 0)
except ZeroDivisionError as e:
    print(e, "We cannot divide by zero")

# Adding more exception
except Exception as e:
    print("Uppsss, something went wrong", e)
    print(e.__class__) # Print the class of the error
```

### Some Examples
```py
# Index Error
try:
    items = [1,2,3,4,5]
    item = items[6]
    print(item)

except IndexError as e:
    print(e, "Item does not exist in the list")
# list index out of range Item does not exist in the list

# File not found
try:
    with open('file_does_not_exist.txt', 'r') as file:
        print(file.read())

except FileNotFoundError as e:
    print(e, "The file could not be found")

```

## File Handling
- open: Reading, writing and creating files
- close: Close the file
```py
# Can accept two arguments: The Name or the Location
open(fileName, fileLocation, Mode)

# This function closes the file automatically "with"
with open('testing.txt', 'r') as file:

```
About Mode Sets:
- r: Open and read (text format)
- rb: Open and read (binary format)
- r+ : Open for reading and writing
- w: Open for writing
- a: Adding or appending data
  
