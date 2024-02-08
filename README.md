# Python-Random-Password-Generator

## Random

```pyhton
import random
```

```pyhton
mealChoice = ["Pad Thai","Krapow","Noodle"]
random.choice(mealChoice)
```

```python
mealChoice = ["Pad Thai", "Krapow","Noodle","Sushi","Steak"]
random.sample(mealChoice,3)
```

## String Module

```python
import string
```

```pyhton
result = string.ascii_lowercase
print(result)
```

```pyhton
result = string.ascii_uppercase
print(result)
```

```python
result = string.ascii_letters
print(result)
```

```python
result = string.digits
print(result)
```

```python
result = string.punctuation
print(result)
```

## Random Password Generator

1. Get length of the preferred password
2. Get the password choice
    A. Digits only
    B. Letters only (lowercase+uppercase)
    C. Letters and Digits
    D. Letters, Digits, and Punctuations
3. Generate a password of the user's choice and length
4. Display the generated password

```python
import random
import string

length = int(input("Please enter length: "))
choice = int(input("Please enter choice (1: digits only, 2: letters only, 3: digits + letters, 4: digits + letters + punctuations)"))

if choice == 1:
    character = string.digits
    password = random.sample(character, length)
    password = "".join(password)
    
elif choice == 2:
    character = string.ascii__letters
    password = random.sample(character, length)
    password = "".join(password)
    
elif choice == 3:
    character = string.digits + string.ascii_letters
    password = random.sample(character, length)
    password = "".join(password)
    
elif choice == 4:
    character = string.digits + string.ascii_letters + string.punctuation
    password = random.sample(character, length)
    password = "".join(password)
    
else:
    print("Wrong choice")
    password = None

print("The generated password: ", password)
```

## Create a function to handle Password Generating

```pyhton
import string
import random

def passwordGenerator(length,choice):
    if choice == 1:
        character = string.digits
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 2:
        character = string.ascii__letters
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 3:
        character = string.digits + string.ascii_letters
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 4:
        character = string.digits + string.ascii_letters + string.punctuation
        password = random.sample(character, length)
        password = "".join(password)
    
    else:
        print("Wrong choice")
        password = None
    return password

length = int(input("Please enter length: "))
choice = int(input("Please enter choice (1: digits only, 2: letters only, 3: digits + letters, 4: digits + letters + punctuations)"))
generatedPassword = passwordGenerator(length,choice)
print("Generated password: ", generatedPassword)
```

Keep asking the user to generate another password until they press "n"

```python
import string
import random

def passwordGenerator(length,choice):
    if choice == 1:
        character = string.digits
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 2:
        character = string.ascii__letters
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 3:
        character = string.digits + string.ascii_letters
        password = random.sample(character, length)
        password = "".join(password)
    
    elif choice == 4:
        character = string.digits + string.ascii_letters + string.punctuation
        password = random.sample(character, length)
        password = "".join(password)
    
    else:
        print("Wrong choice")
        password = None
    return password

while(True):
    length = int(input("Please enter length: "))
    choice = int(input("Please enter choice (1: digits only, 2: letters only, 3: digits + letters, 4: digits + letters + punctuations): "))
    generatedPassword = passwordGenerator(length,choice)
    print("Generated password: ", generatedPassword)
    checker = input("Try again? (y/n): ")
    if checker == "n":
        break
```
