# Types
We have already encountered types - we have talked about integers, strings, lists and so on, but without examining them in any depth.
But python supports expressions that deal with types of values just as well as with the values themselves:
    
    >>> type(1) == type(2)
    True
    >>> type(1.0) == type(2)
    False

    >>> type(1)
    <type 'int'>
    >>> type(2)
    <type 'int'>
    >>> type(1.0)
    <type 'float'>
    >>> type("1")
    <type 'str'>

    >>> type("Hello")
    <type 'str'>
    >>> type(True)
    <type 'bool'>
    >>> type([1, 2])
    <type 'list'>

Types can be assigned to variables

    >>> oneType = type("1")

In fact, types are values just like any other value. You can even enquire the type of a type!

    >>> type(type(1))
    <type 'type'>

And, this type too, has a type:

    >>> type(type(type(1)))
    <type 'type'>
    
The type of the type type, is type type! Very typical! (Ok, you get to groan now :P)

# Creating our own types

    >>> class Apple(object):
    ...   pass
    ... 
    >>> type(Apple)
    <type 'type'>
    >>> apple1 = Apple()
    >>> type(apple1)
    <class '__main__.Apple'>

Custom objects like our apple1 functions kind of like containers for variables - you can store multiple values inside them, giving each a name:

    >>> apple1.weight = 3
    >>> apple1.cost = 45
    >>> apple1.weight
    3
