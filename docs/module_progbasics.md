# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!

#its purpose is to store data/variables. It has the append(), remove(), sort(), count() methods that are for adding a new element to the list, remove an element from the list, sort the list by its elements value, and count the elements in the list that satisfies the input criteria

#### What is the difference between a list/array and a set?

#while a list/array stores the values we add in automaticly the set only adds a value to the set if that value is not already in the set. It ignores if we add in a duplicate.

#### What is the purpose and methods of a dictionary/map data structure?

### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
#### How do you find a max value in a list/array if you can’t use any built-in functions?

#### How do you find the average of values in a list/array if you can’t use any built-in functions?
#### What do we call an *in-place* sort?
#### Explain an algorithm which sorts a list!

### Programming paradigms - procedural

#### What is the call stack?
#### What is “Stack overflow”?
#### What are the main parts of a function?

### Programming languages - Python  
#### How do you use a dictionary in Python?
# you can iterate it by dictionary = dict()
# you can add keys to it by dictionary["key"] = value or the update(method)
# you can add to its values by +=
# you can search in it by key dictionary["key"] but not by index
# you can remove tfrom it by the pop("key") method
# you can iterate through its keys, values, or both

#### What does it mean that an object is immutable in Python?

# it means that the objects values cannot be changed. I.e: tuple

#### What is conditional expression in Python?

# it is an expression that can control what happens if a condition meets its criteria

#### What are different types of arguments in Python?
#### What is variable shadowing? (context: variable scope)
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
#### What type of elements can a list contain in Python?
#### What is slice operator in Python and how to use?
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
#### What is the purpose of the in and not in membership operators in Python?
#### What does the + operator mean when used with strings in Python?
#### Explain f strings in Python?

#  it is a string that can include variable names and change it's characters accordingly


#### Name 4 iterable types in Python!
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
#### Does the order of the function definitions matter in Python? Why?
#### What does unpacking mean in Python?
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
#### What does step over, step into and step out mean while using the debugger?
#### How can you start to debug a program from a certain line using the debugger?

### Version control

#### What are the advantages of using a version control system?
#### What is the difference between the working directory, the staging area and the repository in git?
#### What are remote repositories in git?
#### Why does a merge conflict occur?
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
#### What does it mean atomic commits and descriptive commit messages?
#### What’s the difference between git and GitHub?

## Software design

### Clean code

#### What does clean code mean?

# clean code means: 
# - there are no duplications in the code
# - there is no dead code in the code
# - the variable and function names are meaningful and well organized
# - there are no lines in the code that could have been obviously substituted by an expression
# - the code is well structured and the functions are simple and understandable, no functions do more than one or two things

#### What steps do we usually do during a clean code refactoring?

# - we realize what lines of the code smell
# - we make an effort to make the code clean
# - we test it that the functionality of the code didn't change and the program works the same as before
# - (optional) commit the changes

### Error handling

#### What is exception handling?

# It is when the program would normally crash and the programmer tries to prevent it and finally handle it while the program is still running, by incorporating proper lines in the code


#### What are the basics of exception handling in Python?

# it has a syntax: 
# try:
#     piece of code
# except: TypeOfError
#	code when error occurs
# and it has an order: the line at which the error occurs, and the lines after that(but inside the try statement) don't run, the lines inside the except statement will run instead.
# after the except we should give a type of error, if we don't we we'll handle all of the errors

#### In which case should we catch an exception? Why?

# we should catch and exception if we know what to do with it. Otherwise the code will be unmaintainable, and logically unordered

#### What can/should we do with an exception in the ‘except’ block?

# we can catch it inside or outside the except block as well.


#### What does the else and finally statement do in a try-except block in Python?

# the else block will run if there are no exception raised in the try block, the finally will run regardless if there were any exceptions raised.

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

## Programming environment

### Unix

#### What is UNIX and what is Linux?
#### What do we call the shell in Linux?
#### What does root means in a Linux environment?
#### How do you access your personal files in Linux?
#### How can you install an application in Linux?
#### What is package management in Linux, what are repositories?
#### How do you navigate in the filesystem with the command line?
#### What does the following commands do: mkdir, rm, cat, cp, touch?
#### How can you look up what does a command do in Linux if you have no internet connection?
#### What does the following commands do: head, tail, more, less?
#### How do you download a file from internet using the terminal?
