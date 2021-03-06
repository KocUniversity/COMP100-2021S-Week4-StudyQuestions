## Functions

```
def name of function (list of formal parameters):
   body of function
```

Let's look at the max example:

```
def max(x, y):
  '''
  finds and returns the max of x and y
  '''
  if x > y:
    return x
  else:
    return y
```

**Formal parameters**: `x` and `y`
**Function call**: `max(3, 4)`
  * Binding **formal parameters** to **actual parameters (arguments)**: `x` to 3 and `y` to 4

**Return** value:
`max(3,4) * max(3,2)`

When a function is called:

1. Binding the formal parameters of the function to the values of actual parameters

  **Example:** `max(3+4, z)` will bind the formal parameter `x`
to 7 and the formal parameter `y` to whatever value the variable z has.

2. Move the point of execution (the next instruction to be executed) from the point of invocation (caller) to the first statement in the body of the function.

3. Execute the code in the body of the function is executed until 
* either a return statement is encountered 
(returns the value of the expression following the return)
* or there are no more statements to execute 
(returns `None`)

4. Replace the function call by the return value

5. Tranfer the point of execution to the caller


**Positional arguments**: the first formal parameter is bound to the first actual parameter, the second formal to the second actual, etc. 

**Keyword arguments**: Formals are bound to actuals using the name of the formal parameter.

```
def printName(firstName, lastName, reverse):
  if reverse:
    print lastName + ', ' + firstName
  else:
    print firstName, lastName
```

These are all equivalent:
```
printName('Jon', 'Snow', False)
printName('Jon', 'Snow', reverse = False)
printName('Jon', lastName = 'Snow', reverse = False)
printName(lastName = 'Snow', name = 'Jon', reverse = False)
```

Keyword arguments can appear in any order **BUT** cannot be followed by a non-keyword argument.

Not allowed:
`printName('Jon', lastName = 'Snow', False)`


**Default Parameter Values** to call a function with fewer than the specified number of arguments:

```
def printName(firstName, lastName, reverse = False):
  if reverse:
    print lastName + ', ' + firstName
  else:
    print firstName, lastName

printName('Jon', 'Snow')                 # will print Jon Snow
printName('Jon', 'Snow', True)           # will print Snow, Jon
printName('Jon', 'Snow', reverse = True) # will print Snow, Jon
```