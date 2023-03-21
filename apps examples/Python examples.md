# Examples of Python Apps

## Expressions

Some Python expressions are similar to those in languages such as C and Java, while some are not:
```
Addition, subtraction, and multiplication are the same, but the behavior of division differs. 
There are two types of divisions in Python: 
floor division (or integer division) // and floating-point/division. 
Python also uses the ** operator for exponentiation.
```

```py
The @ infix operator. It is intended to be used by libraries such as NumPy for matrix multiplication.
The syntax :=, called the "walrus operator", was introduced in Python 3.8. 
It assigns values to variables as part of a larger expression.
``` 
```py
In Python, == compares by value, versus Java, which compares numerics by value and objects by reference. 
Pythons is operator may be used to compare object identities (comparison by reference), 
and comparisons may be chained—for example, a <= b <= c.

```py
Python uses and, or, and not as boolean operators rather than the symbolic &&, ||, ! in Java and C.

Python has a type of expression called a list comprehension, as well 
as a more general expression called a generator expression.

Anonymous functions are implemented using lambda expressions; however, 
there may be only one expression in each body.

Conditional expressions are written as x if c else y 
(different in order of operands from the c ? x : y operator common to many other languages).
```

```py
Python makes a distinction between lists and tuples. Lists are written as [1, 2, 3], are mutable, 
and cannot be used as the keys of dictionaries (dictionary keys must be immutable in Python). 
Tuples, written as (1, 2, 3), are immutable and thus can be used as keys of dictionaries, 
provided all of the tuple elements are immutable. The + operator can be used to concatenate two tuples, 
which does not directly modify their contents, but produces a new tuple containing the elements of both. 
Thus, given the variable t initially equal to (1, 2, 3), 
executing t = t + (4, 5) first evaluates t + (4, 5), which yields (1, 2, 3, 4, 5), 
which is then assigned back to t—thereby effectively "modifying the contents" of t 
while conforming to the immutable nature of tuple objects. Parentheses are optional 
for tuples in unambiguous contexts.
```

```
Python features sequence unpacking where multiple expressions, each evaluating to anything that can be assigned 
(to a variable, writable property, etc.) are associated in an identical manner to that forming tuple literals—and, 
as a whole, are put on the left-hand side of the equal sign in an assignment statement. The statement expects an 
iterable object on the right-hand side of the equal sign that produces the same number of values as the provided 
writable expressions; when iterated through them, it assigns each of the produced values to the corresponding 
expression on the left.
```

```py
Python has a "string format" operator % that functions analogously to printf format strings in C 
e.g. "spam=%s eggs=%d" % ("blah", 2) evaluates to "spam=blah eggs=2". 
In Python 2.6+ and 3+, this was supplemented by the format() method of the str class, 
e.g. "spam={0} eggs={1}".format("blah", 2). 
Python 3.6 added "f-strings": spam = "blah"; eggs = 2; f'spam={spam} eggs={eggs}'.

Strings in Python can be concatenated by "adding" them (with the same operator as for adding integers and floats), 
e.g. "spam" + "eggs" returns "spameggs". 
If strings contain numbers, they are added as strings rather than integers, e.g. "2" + "2" returns "22".
```


## Variables

```py
apples = 20             # type integer
price = 19.95           # type float
is_fruit = True         # type boolean
first_name = "Ethan"    # type String
print(apples)
print(price)
```

## Receiving Input

```py
apples = input("How many apples do you have ?")

print("You have " + apples + " apples!")
```

## Type Conversion

```py
date = input("Enter the year you were born? ")
# input will return a string
age = 2021 - int(date)  # convert the variable to an integer before doing the arithmetic

print(age)
```

## Strings

```py
planet_name = 'jupiter'

print(planet_name.upper()) # Only returns a new string
print(planet_name)

print(planet_name.find('t')) # returns the index of the character

# print(planet_name.replace('x', 9))  # does not exists, nothing happens
print(planet_name.replace('t', "T"))  # returns a new string
print(planet_name)

# Another way to check if string exists
print("ter" in planet_name)
```

## Arithmetic Operators

```py
# classics: +, -, *, /
print(10 / 3)

print(10 // 3)

# Try finding the differences between / and //

# Modulus
print(10 % 3)

# Exponent
print(10 ** 3)

# Increment with augmented assignment operator
x = 10
x += 7      # It's the same as x = x + 7
```

## Operator Precedence

```py
# Precedence is the same as in Maths
x = 10 + 3 * 2
print(x)

# Python can also use parentheses
x = (10 + 3) * 2
print(x)
```

## Comparison Operators

```py
x = 5 > 8  # creates a boolean value
print(x)

# Also have <, >=, <= or == (equality)
# Can also have not equal to using !

x = 5 != 8  # 5 is not equal to 8
print(x)
```

## Logical Operators

```py
# It can also be combined using 'and'/'or'
Mercury = 1
Venus = 2
Earth = 3
print(Venus > Mercury and Venus < Earth)  # and == both condition needs to be True

print(Venus > Mercury or Mercury > Earth)  # or == at least one condition needs to be True

# You can also use the not operator
print(Venus > Earth)   # returns False
print(not Venus > Earth) # returns True
```

## If Statements

```py
temperature = 25

# Python only uses indentation
if temperature > 30:
    print("It's too hot for me")   # note on the quotes
    print("Drink more water")
elif temperature > 20:
    print("It's alright")
elif temperature > 10:
    print("It's a bit cold")
else:
    print ("It's freezing")
print("Done")
```

## Exercise

- Knowing that 5 apples equals to 1 kg:
- Input the amount of apples
- Ask if weight needs to be in (k)kg or (l)lbs
- Calculate the weight of all apples

### Example Solution

```py
apple_weight = 1 / 5
apples = input("Amount of apples: ")
unit = input("(K)g or (L)bs: ")

if (unit.upper() == "K"):
    total = apple_weight * float(apples)
    print("Weight in Kgs: " + str(total))
elif(unit.upper() == "L"):
    total = (apple_weight * 0.45) * float(apples)
    print("Weight in Lbs: " + str(total))
else:
    print("Please specify (K)g or (L)bs only")
```

## Dictionaries

```py
distance_from_sun = {
    "Mercury": 0.4,
    "Venus": 0.7,
    "Earth": 1,
    "Mars": 1.5
}

my_dict = {
    "Mercury" : 
        { 
            "moons" : 0,
            "atmosphere": False 
        },
    "Venus" :
        { 
            "moons" : 0,
            "atmosphere": True
        },
    "Earth" :
        { 
            "moons" : 1,
            "atmosphere": True
        },
    "Mars" : 
        { 
            "moons" : 2,
            "atmosphere": True
        },
}


print(distance_from_sun["Mercury"])
print(distance_from_sun["Earth"])
```

## Loop through dictionaries

```py
distance_from_sun = {
    "Mercury": 0.4,
    "Venus": 0.7,
    "Earth": 1,
    "Mars": 1.5
}

# iterate through the keys
for planet in distance_from_sun:
    print(planet + " --> " + str(distance_from_sun[planet]))

# iterate through the item with key, value pair
for planet, distance in distance_from_sun.items():
    print(planet + " --> " + str(distance))
```
