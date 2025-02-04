# Returns the secret to beautiful code

def secretToCoding1():
print ("")
print ("Beautiful code is both ELEGANT and EFFICIENT")
print (" ELEGANT: concise, easy to read, easy to understand, easy to maintain, easy to modify")
print (" EFFICIENT: minimal CPU operations, minimal memory/storage requirements")
print ("")

# Returns the secret to beautiful code

def secretToCoding2():
print ("\nBeautiful code is both ELEGANT and EFFICIENT\n ELEGANT: concise, easy to read, easy to understand, easy to maintain, easy to modify\n EFFICIENT: minimal CPU operations, minimal memory/storage requirements\n")

# Which code is more beautiful: secretToCoding1() or secretToCoding2()?

import math
import random
import time
from datetime import datetime

animals = ['Duck', 'Jackal', 'Hippo', 'Aardvark', 'Cat', 'Flamingo', 'Iguana', 'Giraffe', 'Elephant', 'Bear']

##########

# O(1)

##########

# Return the name of all animals

def getAnimals():
return animals

##########

# O(n)

##########

# Returns the number of animals

def countAnimals():
num_animals = 0
for animal in animals:
num_animals += 1
return num_animals

# Returns each animal with all letters lowercase

def getLowercaseAnimals():
lowercase_animals = animals
animal_index = 0
for animal in animals:
lowercase_animals[animal_index] = lowercase_animals[animal_index].lower()
animal_index += 1
return lowercase_animals

# Given the name of a animal,

# Return True if that animal is in the list, False otherwise

def hasAnimal(animal_name):
num_comparisons = 0
for animal in animals:
num_comparisons += 1
print(f"comparisons: {num_comparisons}")
if animal == animal_name:
return True
return False

# Given the name of a animal,

# Return the animal's index if that animal is in the list, -1 otherwise

def findAnimal(animal_name):
animal_index = 0
for animal in animals:
if animal == animal_name:
return animal_index
animal_index += 1
return -1

# Shuffle the order of the stored animals

def shuffleAnimals():
num_animals = countAnimals()
for i in range(num_animals):
random_i = random.randrange(num_animals)
temp_storage = animals[i]
animals[i] = animals[random_i]
animals[random_i] = temp_storage

##########

# O(n^2)

##########

animals = ['Duck', 'Jackal', 'Hippo', 'Aardvark', 'Cat', 'Flamingo', 'Iguana', 'Giraffe', 'Elephant', 'Bear']

# Print a list of all possible animal pairs

def printAnimalPairs():
num_operations = 0
for animal1 in animals:
for animal2 in animals:
num_operations += 1
print (f"{num_operations}: {animal1} - {animal2}")

##########

# O(n^3)

##########

# Print a list of all possible animal triples

def printAnimalTriples():
num_operations = 0
for animal1 in animals:
for animal2 in animals:
for animal3 in animals:
num_operations += 1
print (f"{num_operations}: {animal1} - {animal2} - {animal3}")

##########

# O(2^n)

##########

# Given a list,

# Return a list of all possible combination of animals

def getListOfAnimalCombos(l):
list_length = len(l)
if list_length == 0:
return [ [] ]
else:
animalCombos = []
previousCombos = getListOfAnimalCombos( l[1:] )
for combo in previousCombos:
animalCombos.append( combo )
animalCombos.append( combo + [l[0]] )
return animalCombos

##########

# O(n!)

##########

# Given a list,

# Return a list of all possible arrangements of list items

def getAllArrangements(l):
list_length = len(l)
if list_length <= 1:
return [l]
else:
arrangements = []
previousArrangements = getAllArrangements( l[1:] )
for previousArrangement in previousArrangements:
for i in range(len(previousArrangement) + 1):
arrangements.append( previousArrangement[i:] + [l[0]] + previousArrangement[:i] )
return arrangements

# Given a list,

# Return the list's length

# O(n)

def getLengthOfList(l):
list_length = 0
for i in l:
list_length += 1
return list_length

# Given a list,

# Return the list's length

# O(1)

def betterGetLengthOfList(l):
return len(l)

# This can be used to time the runtime of various functions

def printFunctionRuntime():
start_time = datetime.now()
x = getAllArrangements(animals) # x = getAllArrangements(animals_10 + ["Kangaroo"])
end_time = datetime.now()
print (end_time - start_time)

# num_animals = 9

# num_arrangements = 362,880

# runtime = 1.2 seconds

# num_animals = 10

# num_arrangements = 3,628,800

# runtime = 9.6 seconds

# num_animals = 11

# num_arrangements = 39,916,800

# runtime = 2 minutes 40.7 seconds

animals_1 = ["Aardvark"]
animals_2 = ["Aardvark", "Bear"]
animals_3 = ["Aardvark", "Bear", "Cat"]
animals_4 = ["Aardvark", "Bear", "Cat", "Duck"]
animals_5 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant"]
animals_6 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo"]
animals_7 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe"]
animals_8 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe", "Hippo"]
animals_9 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe", "Hippo", "Iguana"]
animals_10 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe", "Hippo", "Iguana", "Jackal"]
animals_11 = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe", "Hippo", "Iguana", "Jackal", "Kangaroo"]

animals_sorted = ["Aardvark", "Bear", "Cat", "Duck", "Elephant", "Flamingo", "Giraffe", "Hippo", "Iguana", "Jackal"]

## Recursion

```
factorial(5) => 5 * 4 * 3 * 2 * 1 = 120
factorial(4) => 4 * 3 * 2 * 1 = 24
factorial(3) => 3 * 2 * 1 = 6
factorial(2) => 2 * 1 = 2
factorial(1) => 1 = 1

def factorial(num):
    total = 1
    for n in range(2, num + 1):
        total *= n
    return total



def factorial(num):
    if num <=1:  #base case
        return 1
    return num * factorial(num - 1) #recursive call


# Quick Sort

1. Select a pivot. Often times this is the first or last element in a set. It can also be the middle.
2. Move all elements smaller than the pivot to the left.
3. Move all elements greater than the pivot to the right.
4. While LHS and RHS are greater than 1, repeat steps 1-3 on each side.

pivot is 4

[3, 5, 1, 6, 8 , 9, 2, 4]

[3, 1, 2,      4,       5, 6, 8, 9]

[1, 2, 3, 4, 5, 6, 8, 9]

def partition(data):
    left = []
    pivot = data[0]
    right = []
    for v in data[1:]:
        if v <= pivot:
            left.append(v)
        else:
            right.append(v)
    return left, pivot, right
def quicksort(data):
    if data == []:
        return data
    left, pivot, right = partition(data)
    return quicksort(left) + [pivot] + quicksort(right)



def quick_sort_A( books, low, high ):
    print(books)
    # base case
    if low >= high:
        return books
        # recursive case
    else:
        # divide
        pivot_index = low
        # for each element in subarray
        for i in range(low, high):
            if books[i] < books[pivot_index]:
                # double swap to move smaller elements to correct index
                # move current element to the right of pivot
                temp = books[pivot_index+1]
                books[pivot_index+1] = books[i]
                books[i] = temp
                # swap pivot with element on its right
                temp = books[pivot_index]
                books[pivot_index] = books[pivot_index+1]
                books[pivot_index+1] = temp
                pivot_index += 1
        # conquer
        # Quick Sort everything left of the pivot
        books = quick_sort_A(books, low, pivot_index)
        # Quick Sort everything right of the pivot
        books = quick_sort_A(books, pivot_index+1, high)
        return books


```
