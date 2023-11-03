# Proactive Review

## Terminology

TODO: Define terms at the end of chapters

- tuple: immutable ordered sequence of elements
    tuple_ex = (1,2,3)
- iterable object: object you can go through (like a list or tuple or set) --> like range
    - used in a for loop to return sequence of elements one at a time
- list: mutable object
    [1,2,3]
- mutable type: can be changed after it's been created
- immutable type: can't be changed after it's been created
- id function: returns unique integer identifier for an object --> lets you know if 2 objects are the same
- object equality: when objects have the same ID (exact same object basically)
- aliasing: different name for same thing, 2 paths lead to same object
- shallow copy: creates new list and inserts original objects of list
- deep copy: creates new list and inserts copy of the objects in the list
- value None: null value, no 0 or anything at all
- type NoneType: type for None object which is an object that indicates no value
- list comprehension: provides concise way to apply operation to sequence values by iterating over iterable value
    `expr for elem in iterable if test`
    `squared_numbers = [i**2 for i in numbers if i % 2 == 0]`
        basically creates a list and function all in one line
        # creates a list of random numbers between 0 and max for size of list
        `my_list = [random.randrange(0, maximum) for i in range(0, size)]`
- higher-order function: function that takes a function as an argument
- set: mutable kind of collection type --> all objects in set must be hashable
    sex_ex = {1,2,3}
- hashable type: means it's immutable
- dictionary: mutable type, list but indexed with keys instead of numbers
    dict_ex = {key: value}
- dictionary keys: index for values in dict
- dictionary values
- Access dictionary values

- recursion: when a function references itself in the body of the function (function that calls itself)
- base case: specifies result for special case
- recursive case: defines answer in terms of the answer to question on some other input
- progression of input
- global variable: can be modified or read in wide variety of places, not specific to one function

- module: .py file containing definitions and statements
- python package: basically a collection of a bunch of modules
- import statement: used to get access to modules
- `from package import file` --> imports the file with all the functions inside
    have to use dot notation to access the functions in the file --> ex = file.function()

- `from file import function` --> imports specific function from a file
- fully qualified names: dot notation thing (file.function)
- standard Python library: collection of modules that are built in (think len and abs and stuff I think)
- isort: Python library/utility that sorts imports alphabetically and into sections by type
- `poetry run isort .`

- testing: process of running a program to try and find if it works
- pytest: 
- debugging: process of trying to fix a program that you already know doesn't work
- test suite: collection of inpputs that has high likelihood of finding bugs
- partition of inputs: divides set into collection of subsets such that each element of original set belongs in exactly one subset
- glass-box testing: exploring paths through code (looking at code itself)
- black-box testing: exploring paths through specification (constructed without looking at code)
- path-complete testing: testing that explores all potential paths through a program
- overt bug: obvious bug
- covert bug: not obvious bug
- persistent bug: bug that happens every time
- intermittent bug: bug that only happens sometimes
- static semantic error: code you wrote doesn't mean what you want it to mean
- profilers
- code coverage

- exceptions: something that doesn't conform to norm (a problem)
- raising an exception: python error message that occurs
- unhandled exception: exception that causes program to end
- handled exception: problem that doesn't end program
- try-except construct
    ```python
    try:
        code here
    except:
        code here
    ```
- `except Error as message:`
- catch (an exception): to find an error?
- polymorphic functions: functions that work for arguments of many different types
- raise statement assertions: forces specific exception to occur
- types of errors to raise

- object-oriented programming: thinking of objects as collections of both data and methods that operate on said data
- abstract data type: set of objects and the operators on these objects
- class: specifically created type
- class definition: defines a class --> must include `__init__` function
    ```python
    class Class()
    ```
- method attribute: 
- class attributes: defined in class definition
- class instance: 
- \_\_ methods: makes methods private? --> `__salary`
- magic (dunder) methods: set of predefined methods in Python in Python that provide special syntactic features --> `__init__`
- data attribute: 
- instance variable: when data attributes are associated with an instance
- inheritance: when an object gets attributes from superclass
- subclass: class inside a class
    ex. sub(superclass)
- superclass: class with another class inside
    super() means it's a superclass
- isinstance
- encapsulation: describes idea of wrapping data and methods that work on said data within one unit --> used to restrict access to methods and variables
- information hiding: used to defend access to specific users in the application --> done by outting 2 underscores in front of name
    ```python
    class Employee:
        def __init__(self, name, salary):
            self.name = name # public (accessible within or outiside of class)
            self._project = project # protected (accessible within class and subclass)
            self.__salary = salary # private (accessible only within class)
    ```
- linting: finds syntax errors and stylistic problems in source code

## Technical Review

### Review the Python functions from assignments and notes

TODO: To assist in studying, it is recommended to:

- Review chapters 5-10
- Review course [notes in course-materials repo](https://github.com/allegheny-college-cmpsc-101-fall-2023/course-materials/blob/main/Schedule.md)
- Review [Proactive Programmers Slides](https://proactiveprogrammers.com/data-abstraction/schedule-data-abstraction/)
- Hand write definitions to terminology
- Hand write short code snippets that exemplify terminology 
- Ask questions if you have them on Discord in the #data-abstraction channel

#### Provide the first recursive Python function that you can write on your own without assistance

```python
def factorial(number):
    # base case
    if number == 1:
        return number
    # recursive case
    else:
        return number*factorial(number-1)
```

#### Provide the second recursive Python function that you can write on your own without assistance

```python
```

#### Provide the third recursive Python function that you can write on your own without assistance

```python
```

#### Using a previously provided function, provide Python code to show how to call it

```python
```

#### Write two test functions for a function above

```python
```

#### Write a function that directly modifies a list

```python
def square_list(numbers: []) -> List:
    squared_numbers = []
    for number in my_list:
        if number % 2 == 0:
            squared = numbers ** 2
            squared_numbers.append(squared)
```

#### Write a list comprehension

```python
my_list = [random.randrange(0, maximum) for i in range(0, size)]
squared_numbers = [i**2 for i in numbers if (i % 2 == 0)]
```

#### Write an import statement from a package

`from package import module`
`from tyer import List`

#### Add a counter to a recursive function

#### Create simple class

```python
class Cat():
    def __init__(self, name: str, age: int) -> None:
        self.name = name
        self.age = age
```

## Learning Objectives

TODO: Review the learning objectives at [Learning Objectives for Data
Abstraction
structures](https://proactiveprogrammers.com/data-abstraction/learning-objectives-data-abstraction/)
and then use the following instructions to complete the next questions.

### Record three learning objectives for which you judge you can demonstrate mastery of the technical knowledge or skill

Data Analysis, Version Control, Effective Learning

#### Restate the first learning objective and then explain how you know that you have mastered it

Data Analysis: I think I have mastered the data analysis learning objective because I can effectively analyze statistical data to draw conclusions about the performance of an algorithm or program.

#### Restate the second learning objective and then explain how you know that you have mastered it

Version Control: I think I have mastered the version control learning objective because I can effectively use the GitHub platform to clone repositories, create commit messages and commit changes, use branches, discuss potential issues with the code, and submit completed projects that have a passing build.

#### Restate the third learning objective and then explain how you know that you have mastered it

Effective Learning: I think I have mastered the effective learning objective because I can detect an error in a Python program by using tools like GatorGrader and Pytest, explore what the cause of the problem is, and search the iternet for possible solutions. Additionally, I can use Discord and other forms of communication, like Github, to effectively communicate and ask any potential questions.

### Give a learning objective that you have improved on since the last module of the course

TODO: Retype the learning objective and then explain what you did to improve your knowledge
TODO: When you are writing your response to this question, please follow this template:

When I was working on `fill in the name of a project`, I made a mistake when I
`explain details about the mistake`. I did not understand `explain what you did
not understand`. Now I know `explain what you know`. I revealed the gap in my
understanding by `explain what steps you took to identify the gap`. Now I know
`explain what you now know`. To demonstrate my improved understanding, I will
`explain what steps you will take now that you understand the learning
objective`.

### Give a learning objective that connects to covered material but for which you must continue to work

TODO: Retype the learning objective and the explain what work you need to
complete so as to ensure that you can develop a mastery of the stated technical skill

## Review Checklist

TODO: Please create a filled checkbox for each review task that you completed:

- [] Re-read all of the content in the covered chapters of the course textbooks
- [] Studied and executed all of the Python source code in the Jupyter notebooks
- [] Correctly answered all of the summary questions in the Jupyter notebooks
- [] Reviewed and understood all of the technical content in the course slides
- [x] Completed all source code surveys, programming projects, and engineering efforts
- [x] Confirmed that you have a passing build in all of the aforementioned projects
- [] Answered all of the questions in the proactive review document

TODO: If you have questions or concerns about content in this module that you
could not resolve after completing the proactive review, you should take these steps:

- [] Post questions to a public channel in Discord for any unresolved issues
- [] Schedule office hours with the course instructor to discuss any unresolved issues

## Professional Evaluation

### On a scale from 1 to 5, please respond to this assertion from your perspective: "I was challenged intellectually by the content and activities during this module"

TODO: Please create a filled checkbox for the level that best describes your perspective

- [] 1: Strongly Disagree
- [] 2: Disagree
- [] 3: Neutral
- [] 4: Agree
- [] 5: Strongly Agree

### On a scale from 1 to 5, please respond to this assertion from your perspective: "I had plenty of support from my professor, my classmates, the student technical leaders, and the course software as I worked during this module"

TODO: Please create a filled checkbox for the level that best describes your perspective

- [] 1: Strongly Disagree
- [] 2: Disagree
- [] 3: Neutral
- [] 4: Agree
- [] 5: Strongly Agree

### On a scale from 1 to 5, please respond to this assertion from your perspective: "I am closer to mastering the technical and scientific concepts of the course now than I was at the start of this module"

TODO: Please create a filled checkbox for the level that best describes your perspective

- [] 1: Strongly Disagree
- [] 2: Disagree
- [] 3: Neutral
- [] 4: Agree
- [] 5: Strongly Agree

### On a scale from 1 to 5, please respond to this assertion from your perspective: "I felt that I was a part of a community of computer scientists during the past week"

TODO: Please create a filled checkbox for the level that best describes your perspective

- [] 1: Strongly Disagree
- [] 2: Disagree
- [] 3: Neutral
- [] 4: Agree
- [] 5: Strongly Agree

### On a scale from 1 to 5, please respond to this assertion from your perspective: "During the past module I made progress in mastering the technical knowledge and skills in computer science because of my own efforts and choices"

TODO: Please create a filled checkbox for the level that best describes your perspective

- [] 1: Strongly Disagree
- [] 2: Disagree
- [] 3: Neutral
- [] 4: Agree
- [] 5: Strongly Agree

## Professional Reflection and Action

### What is one way in which you think this course will be the same in five years? Why?

TODO: Please answer this question with at least one paragraph consisting of at least three sentences

### What is one way in which you think this course will be the different in five years? Why?

TODO: Please answer this question with at least one paragraph consisting of at least three sentences
