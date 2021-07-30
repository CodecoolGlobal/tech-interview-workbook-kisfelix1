# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!

 its porpuse is to store data/variables. It has the append(), remove(), sort(), count() methods that are for adding a new element to the list, remove an element from the list, sort the list by its elements value, and count the elements in the list that satisfies the input criteria


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

you cannot index it by order, because it is unordered. You can find values by indexing by the key. you can index key-value pairs by iterating through a loop. you can add new key by dictionary[key] = value, and add to it by dictionary[key] += add_value

#### What does it mean that an object is immutable in Python?

it means that its value cannot be changed. string is immutable, list is mutable


#### What is conditional expression in Python?

operators that evaluate something based on a condition being true or false.
if condition1 and condition2:
else:

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
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
#### What type of elements can a list contain in Python?
#### What is slice operator in Python and how to use?
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
#### What is the purpose of the in and not in membership operators in Python?
#### What does the + operator mean when used with strings in Python?
#### Explain f strings in Python?
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
It means
#### What steps do we usually do during a clean code refactoring?

### Error handling

#### What is exception handling?
#### What are the basics of exception handling in Python?
#### In which case should we catch an exception? Why?
#### What can/should we do with an exception in the ‘except’ block?
#### What does the else and finally statement do in a try-except block in Python?

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
