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


#### What is XSS? How to protect an application against it?

Cross site scripting
it is when the user can manipulate an input and thus can make the server to run his code instead of the proper one
to prevent this:
- always check input before running scripts on the server
- encode data on output
- use appropiate content headers

#### How to properly store passwords?

store not the password, but the encrypted version of it inside the database. it usually has a decrypt method to it.

#### What is HTTPS?

a secure protocol - HTTP alternative, which can store sensitive data without or at least lesser security risks

#### What is encryption and decryption?

encryption is when from a string we create a hard to read string that we can decrypt back to the original string using an encryption algorithm

#### What is hashing?

the process of transforming any given key or a string of characters into another value

#### What is the difference between encryption and hashing? When would you use which?

Hashing is for indexing and retrieving items from the database very quickly. 
The purpose of encryption is to transform data to keep it secret from others.

#### What encryption methods do you know?

ceasar, RSA, 

#### What hashing methods do you know?

SHA

#### How/where would you store sensitive data (like db password, API key, ...) of your application?

environment variables, or a separate file outside of the scope of the application.

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

#### What is Big O complexity? Explain time and space complexity!

Big O specifically describes the worst-case scenario, it is to describe how fast a program runs without specifying the processor or the order of the programs
Time complexity is how elapsed time depends of the size of input.
Space is similar to time, it demonstrates how much space (memory space) our program uses, dependently of the input
O(1) means it is independent of the input
O(n) means it is linear
O(n^2) means it is  exponential

### Procedural
#### How the CASE condition works in SQL?

SELECT result_variable
CASE
    WHEN condition1 THEN result1
END AS result_variable;

#### How the switch-case condition works in JavaScript?

switch(expression) {
  case x:
    code
    break;
  default:
    code
}

it takes an expression, and if it equals a case then the proper line will run

#### How to achieve a switch-case-like structure in Python?

I would use a function, inside the function a dictionary which includes the corrisponding values

#### Explain variable scoping in Python!

global
function
local

variable scoping depends on indentation in python
global variables can be used at any function, and they can be defined using the global keyword
function inside functions like this

def a():
	x = 1
	def b():
		print(x)

	will print 1 because it sees the aboce functions x variable
otherwise its local, and it can be seen in the function only.
the same with loops

#### What’s the difference between const and var in JavaScript?

const's value cannot be change
and var's can, but it's outdated, use let instead

#### How the list comprehension looks like in Python?

newlist = [x for x in list if criteria]

#### How the “ternary expression” looks like in Python?

'true' if True else 'false'

#### How the ternary expression looks like in JavaScript?

condition ? exprIfTrue : exprIfFalse

#### How to import a function from another module in Python?

from folder import python_file
or 
from library import function

#### How to import a function from another module in JavaScript?

import { export1 } from "module-name";
import "module-name";

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

element.fireEvent("on" + event.eventType, event);

#### What is a callback function? Tell some examples of its usage.

a callback function is a function passed as a parameter of another fucntion
examples are eventlisteners: a function is run when an event occurs and it is passed as a paramter

#### What is a Python decorator? How does it work? Tell some examples of its usage.

it is a function that takes a function as an argument.
it can be written above a fucntion like @decorator
so what it does in the context
def decorator(func):
	print('a')
	func()
	
@decorator
def p():
	print('b')

is this: it runs as a function that took the below function as argument
output will be: a then b.
it is used to create connection to databases every time we get or manipulate data on them.
or to jsonify data everytime we send them to javascript.

#### What is the difference between synchronous and asynchronous execution?

synchronous is run sequentially, line after line, asynchrnonous is run on a different

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?

You could simply advertise your database connection address and port number on an open connection


#### When do you use the DISTINCT keyword in SQL?

With distinct you can obliterate matching results and only select them once

#### Talk about the behavior/goal of these base SQL clauses: WHERE, GROUP BY, HAVING, ORDER BY?

Where takes an expression which if true to a row it appends it to the result
group by make rows sort of merge into matching data, which then hold a whole other lot of columns data
having is when we want to give a criteria on the group rather than the data inside it
order by takes a column name, it sorts the data by a certain column, if you give it multiple columns then it will sort in order of the columns. Also you can give desc or asc to the end

#### What are aggregate functions in SQL? Give 3 examples.

these are used with a group by, the data inside a group can be manipulated/selected according to the functions
SUM
COUNT
min max, avg


#### What kind of JOIN types do you know in SQL? Could you give examples?

left join
right join
inner join
outer join
this query will select all customers wether they have a sale or not(usually used when they surely do)
select * 
from customer left join sales on custumer.id = sales.customer_id;

#### What are the constraints in sql?

on a database you can constrain data, either tagging it as foreign key so you cannot just delete it because it has a relation,
or constrain it so it can be of a certain type.

#### What is a cursor in SQL? Why would you use one?

cursor is a temporary memory allocation to a user when the user does data manipulation on the database
it can only reference one row at a time, but can be set to another one
cursor enables the sequential processing of rows in a result set

#### What are database indexes? When to use?

it is a data structure that allows faster access to data at the cost of needing more space.
it is useful when you have a big database which should service a lot of users fast.

#### What are database transactions? When to use?

it is a method of keeping track of every data change in the database.
If one client has failed to transact, then the transaction is considered a fail.
I would use it to make sure that the database is secure, stable, and i can keep track of the changes.
If anything happens to the databases integrity or security, I could always recheck the log and revert to the last proper version of it.

#### What kind of database relations do you know? How to define them?
these are to represent how data ina  table is coorelated to another table
one-one father - mother
many-many children - teachers
one-many mother - children

#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
select * from table
where substring(address, Charindex(',', FullName)+1, 7) = 'Miskolc'

#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

With transactions I would always write to a log outside of the application

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

Design should focus on the user
website should be able to scanned not read: infographics and buttons not as text but as icons
simplicity and clarity: buttons should be easy to understand
Useful
useable
findable
credible

#### What is XML, XSLT, DTD?

xml is the alternative for transmitting data to json
it works with tags as well

xlst is a styling language which builds other documents from xml, such as other xml documents, or html documents. The original documents contents are unchanged

dtd is what defines the linked documents contents rules. Such as <!doctype>


#### What is the difference between HTML and XML?
HMTL is markup language that the browser  knows
XML is a markup language that stores data and is for other pages to use

### Javascript

#### What is javascript?

it is the default scripting language for browsers, which can access most of the browsers functions

#### When to use AJAX? Bring examples of its usage.

Asynchronous javascript
it is when you dont want to wait on something(loading of a data form database) for something else to work('being able to load another page')
like 

element.addEventListener('click', loadOtherPage);
and then you can load another page, while clicking the more button you could start another cycle of loading data
element.addEventListener('click', loadMoreData);

#### What is DOM and how to manipulate it from Javascript?

Document object model
a tree object model, html elements are objects with properties
js:
document.getElementById(id).innerHTML
you have to reference the html object, then you can either remove it, manipulate it, or create it inside any element.

#### What are events and how/why to use them in Javascript?

events are things that occur when the user interacts with the page. 
they are used like this:
html element gets an event listener with the AddEventListener('eventType', callback)
and then the callback function will run. it has the parameter of the event that was fired, and with the target property we can reference it.

#### What is event bubbling/capturing? How would you use it?

bubbling is when on the html tree we catch the event on the innermost element and propagate to the outer elements,
capturing is when the outermost is handled first
addEventListener(type, listener, useCapture) by default it is bubbling, but you can set it to true

#### What is JSON and how do we use it?

it is a format for representing structured data. it is used for data transmitting in web applications
we used it as a dictionary, it has key-value pairs.
we get a return value from a server route in string format, we make json from it with the jsonify() function, and use the data as we would have in the server

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

because you dont have to manage your packages by hand but automated and more quickly, more securely (no typos )

#### Why is it good to use a virtual environment for a project?

because you can define a vertain requirement to a specific project, and can handle different version of software than other computers, or even yours have.
The project will become independent of current newest version of softwares

Because this way you can simulate different version of support programs than what's on your computer
And because this way you can ensure that you work with the proper version - requirements.txt you can specify which version

### Networks

#### What kind of HTTP status codes do you know?

200 - Ok
300 - reroute - other routes are necessary to finish the request
400 - not found, bad syntax
500 - the succesful request was failed by the server

#### What is a API?

application program interface. it allows two application to interract with each other.
it is kind of a program package that allows the user or the server to interract with something else more fast, more easly, more simply.

#### What is REST API?

it is not a protocol, but a few restraints of the application architecture.

- server client architecture and http request as a median
- it is stateless - no user information is stores between two get request and each request is separate and unconnected
- uniform interface between components so that information is transferred in a standard form


#### What is JSON? When to use?

data transmission structure, use it when you want to make a useful object that is meaningful to the other client/server and can work with that

#### What is TCP/IP? What layers does it define, what are they responsible for?

the application layer-  an abstraction layer that specifies the shared communications protocols and interface methods used by hosts
transport layer -  provides transparent transfer of data between end users
network layer - It handles the service requests from the transport layer and further forwards the service request to the data link layer
data link layer - the protocol of the transmission, tcp in this instance
physical layer - phisical characteristics of the network, frequency, voltage, ethernet, etc

#### What’s the difference between TCP and UDP?

TCP is for secure and stable transmission - like logins and important data
UDP is for fast transmission that doesn't need to be spotless - like video streams

#### How does an HTTP Request look like? What are the most relevant HTTP header fields?


content type
authorization
accept
cookie

example:

POST /cgi-bin/process.cgi HTTP/1.1
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
Host: www.tutorialspoint.com
Content-Type: application/x-www-form-urlencoded
Content-Length: length
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Connection: Keep-Alive

#### What is DNS? How does it work?

it is like google.com
it makes requests easier for the users, it reduces the ones and zeros to keep in mind when requesting a website.
it works like this:
a datacentre runs a dns server which keeps track of which dns is on which ip address. it is like a dictionary.
then you send the request of your site to it, it signals to the site, the site signals back, you get your data back.
You don't have to remember ip addresses, the dns does it for you.

#### What is a web server?

it is a program that can "serve" client requests to its defined routes.

#### Explain the client-server architecture.

there is a server, which awaits for client requests. If they request a certain thing it processes the request, and will return with an answer/response accordingly.
there are multiple clients,
that are sending requests to the server, and will act according to the response of the server. It is a one to many relation, and it can be happening simulatiniously, independently from the 
architecture of the device the request was sent from.

#### What would you use a session for?

for keeping user related data as long as they use the browser. Like shopping cart to remember what they put in, username to distinguish them.

#### What would you use a cookie for?

to save information about the user on their local machine. Like preference of the styling of the site, what kind of ads they want to see.

## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?

Agile - from backlog tasks go into an iteration cycle, and a feedback mechanism. It allows less errors, bugs, risks.
it allows the developers to release iterations, and based on feedback correct it. It needs real time communication, and users often lack information about the current iteration

DevOps improves time to market, lowering the failure rate of new releases, and it shortens the time between fixes. They do it with automated release deployment. It is cost effective, smooth, and quick
Although not all users want aumotated updates, and certain industries have regulations on testes

waterfall - linear project structure. It is easy to understand and manage, easy to lead, doesnt require too much experience.
but its often slow and costly because of its rigid structure

#### What are the SCRUM roles?

scrum master - helps and leads the development with scrum, gives/takes positions, roles in the management, defines tasks and holds the scrum meetings
product owner - the customer that wants to see results preferably regularly, see advances of the project
scrum team - the developers writing the code

#### What are the SCRUM ceremonies?

meetings that are unique to scrum teams. Scrum ceremonies ensure that everyone is in-sync.

#### What are the SCRUM artifacts?

Product backlog, sprint backlog, product increment

#### What is the main goal of a retrospective meeting?

It is to find errors in humans, or advantages of dev team members, talk through the closed project so everyone can learn from it

#### Explain, when would you recommend to use the waterfall methodology?

when the project only has parts that are based on the done parts

