# Objective
Students will learn the intermediate techniques and structures of Python so that they can begin learning web development or data analytics/science, in a self-directed fashion should they so choose.

# Agenda
0. Welcome
1. Jupyter Notebook Setup
2. Warm Up Exercise
3. Using The Random Library
4. For Loops vs List Comprehensions
4. Break
5. Sorting & Lambda Functions
6. Try/Except
6. Break
7. Using the CSV Library
8. Debugging Code (Optional, if time permits)
9. Final Project

## Jupyter Notebook Setup
0. Open the Terminal (if on Mac) or Command Prompt (if on PC) application
1. Type `jupyter notebook` and then press Enter.
2. The notebook should open in your default browser.
3. Let's walk through how to use the notebook.

## Warm Up Exercise
Write a function called `only_evens` that takes two arguments `start` and `end` and prints out all of the even numbers between start and end, inclusive.

When you use it, e.g. `only_evens(1, 7)` should print the following

```python
2
4
6
```

HINT: Do you remember the `range` function?

## Using the Random Library
### Some questions for discussion
0. What is documentation?
1. When should you use documentation?
2. When is it unnecessary?
3. How do you know if documentation is good?

### Exercises with a Partner
0. Find the Python documentation for the `random` library
1. Explain to each other how the `randint` function works
2. Use the `randint` function.

### Solo Exercise
Suppose we have a list of restaurants:
```python
RESTAURANTS = [
    'Chipotle', 'Philly Bar and Grill', 'AAA Ichiban', 'Hummus and Pita',
    'Medina Cafe', 'Chambar', 'Chambers St Pub'
]
```

Using the `random` library documentation, write a function `pick_lunch_spot` that randomly returns one of the restaurants in the list above.

## For Loops and List Comprehensions
### The For Loop Way
```python
names = ["John", "Mary", "Xuefan", "Lisa", "Esteban", "Casey", "Sven", "Jovanna"]

e_names = []
for name in names:
    if "e" in name:
        e_names.append(name)
```

### The List Comprehension Way
```python
e_names = [name for name in names if "e" in name]
```

### Solo Exercises Using List Comprehensions
0. Filter the list of names to just those that are longer than 4 characters and call that `long_names`.
1. Filter the list of names to those that are longer than 4 characters AND contain the letter `s` call it `long_s_names`

## Sorting (Part 1)
### Solo Exercise
0. With Google as your friend, sort the list of names alphabetically.
1. Sort them reverse alphabetically.

## Lambda functions
```python
def contains_e(name):
    return "e" in name



has_e = lambda name: "e" in name
```

### Try It
0. Call `contains_e` on any name
1. Call `has_e` on any name
2. Do we call them any differently?
3. Is there any difference in the output?

## Sorting (Part 1)
Let's checkout the `sorted` documentation

## Intro to Classes
0. What is an object?
1. What is a blueprint?

### Declaring a Class
```python
class Person(object):
    def __init__(self, name):
        self.name = name
```

### Instantiating an Object
```python
jon = Person("Jon Hunstman")

print(jon.name)
```

### Writing Class Methods
```python
...
    def speak(self, message):
        print(message)
```

### Exercises with a Partner
0. Modify the `__init__` to take first name, last name and save those as attributes.
1. Create a function called `get_full_name` that returns (not prints) the person's full name.
2. Check that it works by instantiating a `Person`!

### Inheritance
```python
class Student(Person):
    def __init__(self, first_name, last_name):
        self.first_name = first_name
        self.last_name =  last_name
        self.subjects = []

    def speak(self, message):
        print("I am a student. " + message)
```
### Solo Exercises
0. Confirm that a Student can speak and can get the full name.
1. Write a function called `learn` that takes a subject name and adds it to the student's list of subjects.

## Try/Except
### Pre-Exercise
Write a function called `divide` that takes two arguments `a`, `b` and returns the result of the division.

When we expect that certain input edge-cases will result in errors, we can preemptively catch those.

```python
try:
    # Do something that might be risky
except:
    # In case something goes awry, do this
else:
    # If nothing bad happened, continue as planned
```

### Exercise
Write a function called `dict_get` that takes two arguments `some_dict` (a dictionary) and `key` (any string) and returns the dictionary value if it exists and if not, it prints an error message `"Sorry, this dictionary does not contain that key!"`.

You can of course implement this without `try/except` but use that structure for practice.

When you use the function, it should work like this:

With `person_dict = {"name": "John"}`

- `dict_get(person_dict, "name")` returns "John"
- `dict_get(person_dict, "age")` returns "Sorry, this dictionary does not contain that key!"


## Using the CSV Library
0. Download [this](https://drive.google.com/file/d/0Byveb6yWfKu2ZThzYno2RV9uSHc/view) CSV to the same directory as your Jupyter notebook.
1. Let's open the file together in Python.


### Exercise with Partner
0. Using your next-level documentation skills, read in the csv file using `csv.DictReader`.
1. Save the rows into a list called `rows`.

## Final Project: Movie Recommender (Partner Optional)
0. Create a class called `Movie` that takes in `genres`, `imdb_score`, and `movie_title` and so is a simplified blueprint for what a movie is.
1. Write a function on the class called `is_high_score` that returns True` if the `imdb_score` is greater than 8.
2. Write a function on the class called `get_genres` that takes the `genres` field and returns a list of the genres instead of the `|` (pipe)-separated string it is in the raw data.
3. Write a class called `Recommender` that takes as an argument in its `__init__` a list of `Movie` objects.
4. Write a function of `Recommender` called `pick_random_movie` that randomly returns one of the movies.
5. Write a function of `Recommender` called `pick_random_genre_movie` that takes a genre name and returns a random movie that belongs to that genre.

# Next Steps
0. Web development
1. Data analysis
2. [DataInstitute.NYC](https://datainstitute.nyc)
3. Side-projects

# Questions
Any questions?

# Keep In Touch!
suneel@simplefractal.com


