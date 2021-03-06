## Scoping

```
def f(x): # the name x as the formal parameter
  # x and y exist only in the scope of f
  y = 1          
  x = x + y
  print 'x =', x
  return x

x = 3
y = 2
z = f(x) # the value of x as actual parameter
print 'z =', z
print 'x =', x
print 'y =', y
```

> x = 4
> z = 4
> x = 3
> y = 2

* When we call the function `f` with variable `x`, i.e. `f(x)`, the formal parameter `x` is locally bound to the value of the actual parameter `x`. 

* They have the same name **BUT** they are not the same variable. Each function defines a new name space, also called a **scope**. 

* The formal parameter `x` and the local variable `y` exist only within the scope of the definition of `f`.

* The assignments in `f` have no effect at all on the bindings of the names `x` and `y` outside the scope of `f`.


Remember **Variable Scope Diagrams**?
Let's draw one for this:

```
def f(x):
  def g():
    x = 'abc'
    print 'x =', x

  def h():
    z = x
    print 'z =', z
    x = x + 1
    print 'x =', x
  
  h()
  g()
  print 'x =', x
  return g

x = 3
z = f(x)
print 'x =', x
print 'z =', z
z()
```
