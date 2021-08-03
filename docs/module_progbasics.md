# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!

<<<<<<< HEAD
its purpose is to store data/variables. It has the append(), remove(), sort(), count() methods that are for adding a new element to the list, remove an element from the list, sort the list by its elements value, and count the elements in the list that satisfies the input criteria
=======
 its porpuse is to store data/variables. It has the append(), remove(), sort(), count() methods that are for adding a new element to the list, remove an element from the list, sort the list by its elements value, and count the elements in the list that satisfies the input criteria

>>>>>>> 6449c592a5d8032e2071bc7a6a8ef299bf1373d9

#### What is the difference between a list/array and a set?

 while a list/array stores the values we add in automaticly the set only adds a value to the set if that value is not already in the set. It ignores if we add in a duplicate.


#### What is the purpose and methods of a dictionary/map data structure?

 They hold key-value pairs to store data. It cannot be indexed, but it is ordered and it is fairly simple to search for any key
 Methods like : .get(), del, .pop(), and they all expect indexes 


### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.

function Fibonacci(number):
    if number <= 1 then
       return number
    else then
       return Fibonacci(number - 1) + Fibonacci(number - 2) 
    end
f   end


#### How do you find a max value in a list/array if you can’t use any built-in functions?

I would first check if that array has any values in it, then if so I would create a designated variable (max) to store the value of the first element. Then I would create a loop that iterates over the whole array/list and checks if the indexed element is higher than the one in the max variable. If so, I overwrite max with the indexed value, then outside the loop I would return the designate variable (max)


#### How do you find the average of values in a list/array if you can’t use any built-in functions?

I would create a variable (sum) that keeps track of the list/array's sum, and a count that keeps count of the number of elements. I would iterate over the list and add together the elements in this variable and at the same time I would increment the count variable by one. Then I would return sum / count.


#### What do we call an *in-place* sort?

It is a form of sort where we don't use auxiliary variables to store data, but we solve the sortition "in-place" by overwriting elements


#### Explain an algorithm which sorts a list!

simple switch sort: it iterates over the list, checking if the next element is lower than the indexed one, if so it switches the two elements (It uses a temporary variable). It does this as many times as mathematically the worst case scenario.


### Programming paradigms - procedural

#### What is the call stack?

 It is a line of commands that the interpreter keeps track of. Modern day programming languages automate the procedures that "control" the call stack, meaning it is intuitive for the machine which method does it call and when/how.


#### What is “Stack overflow”?

 It is a handy tool for a programmer on the internet to look for answers. 
 As well as a type of error, which indicates that the program attempted to use more memory than we have and has crashed. 


#### What are the main parts of a function?

name, parameters, the actual code/body


### Programming languages - Python
#### How do you use a dictionary in Python?
<<<<<<< HEAD
you can iterate it by dictionary = dict()
 you can add keys to it by dictionary["key"] = value or the update(method)
 you can add to its values by +=
 you can search in it by key dictionary["key"] but not by index
 you can remove tfrom it by the pop("key") method
 you can iterate through its keys, values, or both

#### What does it mean that an object is immutable in Python?

 it means that the objects values cannot be changed. I.e: tuple

#### What is conditional expression in Python?

 it is an expression that can control what happens if a condition meets its criteria
=======

you cannot index it by order, because it is unordered. You can find values by indexing by the key. you can index key-value pairs by iterating through a loop. you can add new key by dictionary[key] = value, and add to it by dictionary[key] += add_value

#### What does it mean that an object is immutable in Python?

it means that its value cannot be changed. string is immutable, list is mutable


#### What is conditional expression in Python?

operators that evaluate something based on a condition being true or false.
if condition1 and condition2:
else:
>>>>>>> 6449c592a5d8032e2071bc7a6a8ef299bf1373d9

#### What are different types of arguments in Python?

default arguments. def function(default='def')  -  if no parameter is passed when it's called, then the defined value will be in effect - order: non-default, default

keyword arguments. def function(a, b, default='def') - function(default=10, a=10, b=15) order is not important

positional arguments. def function(a, b, c) - function(10, 20, 30) or function(10, c=30, b=20) 

arbitrary positional arguments. def function(*a) - a acts as a tuple -- function (10, 20, 30, 40)- 
for i in a:
   sum += i

arbitrary keyword arguments. def function(**a)
   a holds dictionary values

a function can look like this:
def function(pos1, pos2, /, pos_or_kwd, *, kwd_only):
before / pos only, after / pos or kwd, after * kwd only

#### What is variable shadowing? (context: variable scope)

it means that on the outer scope x is defined and in the inner scope with the same name we define x again. Though it has the same name, the original(outer) x's value doesn't change, because we have another instance defined locally. if we DO want to redefine x, we use the nonlocal x keyword. We can also use global x keyword to use it on only global variables

#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?

it doesnt return any value (None), when deleting if I give invalid parameter, it will throw an exception(ValueError) if not in list.

#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
LEGB: Local, Enclosing, Global, and Built-in these are scopes in a program
local is inside a function, like lambda, and is only visible inside the function
enclosing: in nested functions the names in the enclosing scope are visible from the code of the inner and enclosing functions.
global: This Python scope contains all of the names that you define at the top level of a program or a module.
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
i would create a variable outside the loop and copy the value of the iterator inside the loop
#### What type of elements can a list contain in Python?
basically any. Bool, int, float, string, list, tuple, dictionary, object.
#### What is slice operator in Python and how to use?
slice defines a series of numbers, that can be used to index and 'slice' any indexable data structure. 
slice_to_use = slice(2)
a = 'apple'
b = a[slice_to_use]
b is 'ap'
slice(start, end, step)
start is optional, end is mandatory, step is optional.
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
+ adds an element to the list
- removes an element from a list
* multiplies the list and returns the list's elements *number* many times (int)
/ is not a valid operator
#### What is the purpose of the in and not in membership operators in Python?
it can be used to identify elements inside a list. for i in list:
it can also be used as an operator to decide if an element is in a list
print('apple' not in fruits)
#### What does the + operator mean when used with strings in Python?
it means to append the value.
'app' + 'le' = apple
#### Explain f strings in Python?
<<<<<<< HEAD

it is a string that can include variable names and change it's characters accordingly


=======
it s a string f"{variable}" that can include variable names and change its value accordingly
>>>>>>> 6449c592a5d8032e2071bc7a6a8ef299bf1373d9
#### Name 4 iterable types in Python!
dictionary, tuple, list, set, string
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
[expression for item in iterable if conditional] generator expression - generates in advance
(expression for item in iterable if conditional) list comprehension - generates on demand
generator expressions are more elegant, and time efficient 
#### Does the order of the function definitions matter in Python? Why?
Yes. You can't call a function that doesn't exist yet, because the program runs 
#### What does unpacking mean in Python?
(a, b, c) = (1, 2, 3)
*a, = 1, 2
it means that in one expression you can assign values to multiple variables
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
it implicitly returns None
## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
You can print out values manually,
you can use the debugger, and see all the active variables values in the debugging window
#### What does step over, step into and step out mean while using the debugger?
step over will go onto the next line but will not descend into method calls
step into will descend in any method call
step out will go to the next return or equivalent
#### How can you start to debug a program from a certain line using the debugger?
place a debug dot on the line you want to start from and press the run and debug button 

### Version control

#### What are the advantages of using a version control system?
- you can track your changes, and you can keep a safe copy of the code you think is functional. If it turn out to be not functional you can always go back to an earlier version and fix the problem
- in a group project you can track who did whcih part of the task, and have a more structured way of maintaining the code.
- you can keep the same line of codes on multiple cpmputers, sharing the code has never been so easy!
#### What is the difference between the working directory, the staging area and the repository in git?
working directory are the CURRENT files you have in your computer, and in which directory you are currently working in.
The staging area is a place where you place the changes you have done, and still haven't committed. multiple staged files can go under the same commit
The repository is an abstract thing. The local repository are the files you have on our computer, and the code in it, which is either the same as the remote repository or have uncommitted changes in it.
the remote repository is the version of the files everyone sees, and is not on your computer, but in a sharing server (in most cases). 
you can commit 
#### What are remote repositories in git?
remote repositorories are repositories on remote servers from which you can pull into your local one. it is the 'official' version of your code
#### Why does a merge conflict occur?
merge conflict occurs when the remote repository and the pushing local one is diffrerent, not in length but in content
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
git pull
fix merge conflicts
git add -A
git commit -m "commit message"
git push
#### What does it mean atomic commits and descriptive commit messages?
atomic commits are single functional code snippets you included into your commit. It means that it works, it is irreducably miniature, and clear.
Descriptive commit messages are messages that are clear and simple. it should reflect the changes you made to the code, but remain clear, and not too in depth
#### What’s the difference between git and GitHub?
git is the technology with which you can control the versions.
Github is the platform that can handle git files.

## Software design

### Clean code

#### What does clean code mean?
<<<<<<< HEAD

 clean code means: 
 - there are no duplications in the code
 - there is no dead code in the code
 - the variable and function names are meaningful and well organized
 - there are no lines in the code that could have been obviously substituted by an expression
 - the code is well structured and the functions are simple and understandable, no functions do more than one or two things

#### What steps do we usually do during a clean code refactoring?

 - we realize what lines of the code smell
 - we make an effort to make the code clean
 - we test it that the functionality of the code didn't change and the program works the same as before
 - (optional) commit the changes

### Error handling

#### What is exception handling?

 It is when the program would normally crash and the programmer tries to prevent it and finally handle it while the program is still running, by incorporating proper lines in the code


#### What are the basics of exception handling in Python?

 it has a syntax: 
 try:
     piece of code
except: TypeOfError
	code when error occurs
 and it has an order: the line at which the error occurs, and the lines after that(but inside the try statement) don't run, the lines inside the except statement will run instead.
after the except we should give a type of error, if we don't we we'll handle all of the errors

#### In which case should we catch an exception? Why?

we should catch and exception if we know what to do with it. Otherwise the code will be unmaintainable, and logically unordered

#### What can/should we do with an exception in the ‘except’ block?

we can catch it inside or outside the except block as well.


#### What does the else and finally statement do in a try-except block in Python?

the else block will run if there are no exception raised in the try block, the finally will run regardless if there were any exceptions raised.

=======
- there are no duplications in the code
- there is no dead code in the code
- the variable and function names are meaningful and well organized
- there are no lines that could have been obviously substitued by and expression
- functions are simple, and understandable, preferably doing one thing at once
#### What steps do we usually do during a clean code refactoring?
- we realize that there is code smell
- we make an effort to make the code clean
- we test that the functionality of the code didn't change, the program works the same as before
- commit the changes
### Error handling

#### What is exception handling?
It is when the program would normally crash and the programmer tries to prevent it and finally handle it while the program is still running, by incorporatin proper lines in the code
#### What are the basics of exception handling in Python?

syntax
try:
   code
except TypeOfError:
   code
else:
   code
finally:
   code
after the exception happens no lines will be exectued in the try block
if we dont give type of error, all exceptions will be cought
#### In which case should we catch an exception? Why?
We should catch an error if we know what to do with it
#### What can/should we do with an exception in the ‘except’ block?
give some feedback to the user, orother programs, maybe return something.
Or catch additional errors and try to fix it
#### What does the else and finally statement do in a try-except block in Python?
else: runs if no exceptions are cought in the try block
finally: runs at the end of the blocks no matter what
>>>>>>> 6449c592a5d8032e2071bc7a6a8ef299bf1373d9
## Software Development Methodologies

#### What is the main goal of a retrospective meeting?
it is to evaluate its past working cycle at the end of an agile sprint
## Programming environment

### Unix

#### What is UNIX and what is Linux?
UNIX   is an operating system written in C. It has a CLI. Mutli-user multitasking, and can be used as a master control program in workstations and servers.
Linux is an operating system. Multithreading multitasking, more portable, can coexist with other operating systems. It is a replica of UNIX, but it does not use its code
#### What do we call the shell in Linux?
Bash
#### What does root means in a Linux environment?
s the user name or account that by default has access to all commands and files on a Linux
#### How do you access your personal files in Linux?
/home/username
#### How can you install an application in Linux?
sudo apt-get install [application name]
#### What is package management in Linux, what are repositories?
A Linux repository is a storage location from which your system retrieves and installs OS updates and applications.
Package management is a method of installing, updating, removing, and keeping track of software updates from specific repositories (repos) in the Linux system.
#### How do you navigate in the filesystem with the command line?
ls - view list of file names
pwd - print working directory - directory you are currently working with
cd - change directory
cd .. go up a directory
cat - open file
#### What does the following commands do: mkdir, rm, cat, cp, touch?
mkdir - create a directory
rm - delete file
cat - open file, read file in 
cp - copy file to another location
touch - create file
#### How can you look up what does a command do in Linux if you have no internet connection?
command -help
#### What does the following commands do: head, tail, more, less?
more filename : show the document one page at a time
less filename : is much the same as more command except you can navigate the page up/down using the less command and not possible in more command.
tail -n filename : display the last n lines of the file3
head -15 myfile.txt – Would display the first fifteen lines of myfile.txt.
#### How do you download a file from internet using the terminal?
wget  -O /[location]/NewFileName "[url]"
will download the file in the url to /h[location] and give it your NewFileName name.
