## Python

Python is a high level general-purpose programming language. It uses a multi-paradigm approach, meaning it supports procedural, object-oriented, and some functional programming constructs.

### programming language: python

1. set of instruction to the computer
2. but computers understand only 1 and 0
3. we need a translator(compiler or intrepreter) that converts the source code to binary(0,1)
4. compiler executes the whole source code file to a binary file at once.
5. interpreter interprets line by line and executes it before it goes to the next line.
6. python is written in C (cpython which is the interpreter)
7. python code => taken by interpreter(cpython) => converts to byte code(0,1) => taken by cpython VM and executed in the system.
8. code editors: visual studio code
9. IDEs: pycharm,spyder
10. notebooks: jupyter
11. repl.it(without installing anything we can work with python)
12. python creator guido van rossum
13. python3 --version

## Python datatypes

1. int
2. float
3. bool
4. str
5. list
6. dict
7. set
8. tuple
9. we can create custom types
10. none

## methods

1. bin(5) // converts to a binary no
2. int('0b101',2) // converts to a integer no
3. type('hi') // gives str
4. str(100) // converts to string
5. int('100') // converts to integer
6. input('enter your age') // get inputs from the user and inputs will be in string, so be careful so that you take the correct value out of it(convert to integer).

## variables

1. variables should be written in snake_case.
2. iq=190 // this is how variable is defined
3. PI=3.14 // to declare constants
4. a,b,c=1,2,3 // way to assign value to variable

## expression

a piece of code that evaluates to a value

## statement

a single line of code (ie) a=10 // statement

## string

1. we can use ''' ''' to type long text with multiple lines and print it

## Notes

1. formatted strings === format() // used for same purpose prefer print(f"Hi {firstname}")
2. print(array[0:len(array)]) // to retrieve particular values
3. input("") // to get input from user
4. list is similar to array, array.append to add additional value, array.sort to sort the array,array.pop to delete an element
5. set does not allow duplicate values {1,2,4,1}
   print({1,2,4,1}) //will print 124
6. how to create virtual environment
   `python -m venv fastapienv`
   `fastapienv/Scripts/activate.bat`

## Points

1. It can work with any client-side framework, and can deliver content in almost any format (including HTML, RSS feeds, JSON, and XML).

2. Django enables protection against many vulnerabilities by default, including SQL injection, cross-site scripting, cross-site request forgery and clickjacking (see Website security for more details of such attacks).

3. As a result, experienced Python/Django developers typically run Python apps within independent Python virtual environments. This enables multiple different Django environments on a single computer. The Django developer team itself recommends that you use Python virtual environments!

4. Experienced Python developers may install additional tools, such as linters (which help detect common errors in code).

Note that you should use a Django-aware linter such as pylint-django, because some common Python linters (such as pylint) incorrectly report errors in the standard files generated for Django.
