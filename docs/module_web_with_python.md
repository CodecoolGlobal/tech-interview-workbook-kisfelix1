# Web with Python questions

## Software design

### Clean code

#### Point out 5 suggestions, how to format an SQL query!

 - keep capitalization consistent - if you do a query capitalized then keep to that rule at the other.
 - don't write a query in one line - each statement, clause should be in a new line in order to prevent too long/hard to read lines in code
 - don't use f strings to format queries, to insert variables use sql.SQL() or the execute(, dict)
 - indent statements, operators, variables properly
 - name tables, variables properly - CityName is not right, all lowercase is the proper way, and underscores - city_name



#### What layers can you name in a simple web application?

 server layer - the user "interacts" with this layer, it handles routes and basic orders
 data_manager - it solves the problem of dealing with data. It manipulates data, deletes, inserts, edits. 
 database_common - it creates connection to the database on your system - from orders from datamanager it handles cursor and connection

### Error handling
#### What error can occur, when an array does not have an element on the requested index?

out of index range error

#### What is the “finally” block, and how would you use it?

it is a block inside try catch mechanics, it runs either if the catch catches an error. 
I would use it when I try to get all data from a database, i try to get an element by id and it doesnt exist, 
but even if i got the id right i want to display all the data - with or without it

#### Why should we catch special exception types?

so we know exactly what went wrong - if the user provided an incorrect username or a database isnt online.


### Security
#### What is SQL injection? How to protect an application against it?

an sql injection is when a user doesnt use input fields properly, and inputs sql commands which break the database or steal sensitive user data
an application can be protected by writing sql queries in a secure way inside the application. Frameworks usually have their own solutions to this problem. 


#### What is XSS? How to protect an application against it? ----------------------------------------------------
#### How to properly store passwords?

store not the password, but the encrypted version of it inside the database. it usually has a decrypt method to it.

#### What is HTTPS?

a secure protocol - HTTP alternative, which can store sensitive data without or at least lesser security risks

#### What is encryption and decryption?

encryption is when from a string we create a hard to read string that we can decrypt back to the original string using an encryption algorithm

#### What is hashing?

the process of transforming any given key or a string of characters into another value

#### What is the difference between encryption and hashing? When would you use which?



#### What encryption methods do you know?
#### What hashing methods do you know?---------------------------------------------------------------------------
#### How/where would you store sensitive data (like db password, API key, ...) of your application?

## Computer science

### Algorithms

#### What is the difference between Stack and Queue data structure?

stack is based on LIFO  principle, queue is on FIFO
insert/delete is from top, queue delete is from front, insert is from rear
stacks are for recursion, queues are for linear processing

#### What is BubbleSort? Describe the main logic of this sorting algorithm.

bubblesort is a sorting algorithm.
it iterates over a list and checks the elements, and if one is not in its place then it places on the last index and recurse.
this way the biggest value will "come on top" like a bubble, hence the name

#### Explain the process of finding the maximum and minimum value in a list of numbers!

we declare a variable outside the loop
we iterate over the list, and check if the iterated value is bigger/smaller than the declared one.
if it is, we change it to the iterated value

#### Explain the process of calculating the average value in an array of numbers!


 we declare a variable outside the loop called sum
 we iterate over the list, and add to the sum
 at the end, we divide the sum by the number of numbers in the list

#### What is Big O complexity? Explain time and space complexity! -----------------------------------------

### Procedural
#### How the CASE condition works in SQL?
#### How the switch-case condition works in JavaScript?
#### How to achieve a switch-case-like structure in Python?
#### Explain variable scoping in Python!
#### What’s the difference between const and var in JavaScript?
#### How the list comprehension looks like in Python?
#### How the “ternary expression” looks like in Python?
#### How the ternary expression looks like in JavaScript?
#### How to import a function from another module in Python?
#### How to import a function from another module in JavaScript?

### Functional
#### What is recursion?
recursion is when a function calls itself inside the function, thus creating a loop of function calls
#### Write a recursive function which calculates the Fibonacci numbers!
function fiboncaci(num):
	if num == 0:
		return 0
	elif num == 1:
		return 1
	else:
		return fibonacci(num-1)+fibonaci(num-2)
#### How to store a function in a variable in Python?
def val():
	return 5
	
func = val() // 5 lesz az értéke 
func = val // magát a függvényt tárolja el
#### List the ways of defining a callable logical unit in JavaScript!
function a(){}
var a = function a(){}
var a = {function a(): {return 0}}
var add = (num1, num2)=> num1+num2; 

#### What is an event listener? How to attach one?
event listener is waiting for an event and it is called when that event happens
hmtlObject.addEventListener('event', function)
#### How to trigger an event in JavaScript?
#### What is a callback function? Tell some examples of its usage.
a callback function is a function passed as a parameter of another fucntion
examples are eventlisteners: a function is run when an event occurs and it is passe das a paramter
#### What is a Python decorator? How does it work? Tell some examples of its usage.
#### What is the difference between synchronous and asynchronous execution?

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
#### When do you use the DISTINCT keyword in SQL?
#### Talk about the behavior/goal of these base SQL clauses: WHERE, GROUP BY, HAVING, ORDER BY?
#### What are aggregate functions in SQL? Give 3 examples.
#### What kind of JOIN types do you know in SQL? Could you give examples?
#### What are the constraints in sql?
#### What is a cursor in SQL? Why would you use one?
#### What are database indexes? When to use?
#### What are database transactions? When to use?
#### What kind of database relations do you know? How to define them?
#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
HTML is a markup language to give the browser orders what to do and how to do it
XML is a way to store data and allow communication between programs
XHTML is an XML based HTML, it is the same as HTML but with the rules of XML
#### How to include a JavaScript file in a webpage?
<script src="myscripts.js"></script>
<script>console.log('This is how');</script>

#### How to include a CSS file in a webpage?
<link rel="stylesheet" href="styles.css">
into the head
#### How to select an element using its id in CSS?
#elementId

#### How to select elements using their class in CSS?
.elementClass
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?
.apha .beta
#### How to select all list items in all ordered lists on the page in CSS?
ul li
#### How to select elements using their attributes in CSS?
[attribute]
#### What are UX and UI?
UX is user experience 
UI is user interface
UX is first then UI but nothing without the other
Ux is waht a user wants to do on a page, ui is what they want to see
#### Please list some points that an application should fulfill to have good UX.
#### What is XML, XSLT, DTD?
#### What is the difference between HTML and XML?
HMTL is markup language that the browser  knows
XML is a markup language that stores data and is for other pages to use

### Javascript

#### What is javascript?
it is the default scripting language for browsers, which can access most of the browsers functions
#### When to use AJAX? Bring examples of its usage.
#### What is DOM and how to manipulate it from Javascript?
#### What are events and how/why to use them in Javascript?
#### What is event bubbling/capturing? How would you use it?
#### What is JSON and how do we use it?

## Software engineering

### Version control

#### What type of branching strategy would you use?
I would make a different branch for every feature the end product has,  and when taht feature is done I would make a pull request to the development branch
#### What would you do if you find a bug on the production code (master branch)?
I would revert to the version which doesnt have the bug, make a different branch that aims to fix the bug and when thats done rebase
#### How can you move changes from one branch to another in GIT?
with rebase, or merge. If you want commits as well you use rebase
#### How does a VCS help with code reviews?
On code reviews this way the reviewer can have a better understanding of how the programmer worked
The reviewee can share their code easier

#### What is your favorite git command? Why?
git merge, because that's why git is so useable. If you are working in a team and on different branches then you use this a lot
and it really saves time compared to what you should do if you don't have this command
#### What does remote/local mean in Git? 
remote is what's on the online/not local repository(github servers for example)
local means whats on your computer physically and not on the shared repository

### DevOps

#### Why is it good to use a package manager software?
#### Why is it good to use a virtual environment for a project?

Because this way you can simulate different version of support programs than what's on your computer
And because this way you can ensure that you work with the proper version - requirements.txt you can specify which version
### Networks

#### What kind of HTTP status codes do you know?
#### What is a API?
#### What is REST API?
#### What is JSON? When to use?
#### What is TCP/IP? What layers does it define, what are they responsible for?
#### What’s the difference between TCP and UDP?
#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
#### What is DNS? How does it work?
#### What is a web server?
#### Explain the client-server architecture.
#### What would you use a session for?
#### What would you use a cookie for?

## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?
#### What are the SCRUM roles?

scrum master - helps and leads the development with scrum
product owner - 
scrum team - 
#### What are the SCRUM ceremonies?
#### What are the SCRUM artifacts?
#### What is the main goal of a retrospective meeting?
#### Explain, when would you recommend to use the waterfall methodology?
