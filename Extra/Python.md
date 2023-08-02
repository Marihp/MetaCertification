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
Are declared in curly braces

### Methods:
- remove or discard(element): Deletes that element in the set
- union: Can join two set discarting the duplicated values

```py
my_set = {1, 2, 3, 4, 5}

my_set.remove(2) # {1, 3, 4, 5}
my_set.discard(2)
```

