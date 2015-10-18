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

In this respect, custom objects are also similar to lists - they are both **composite objects**.

# Methods provide new functionality

    >>> class Basket(object):
    ...     def addContent(self, item):
    ...         self.weight = self.weight + item
    ...     def getContent(self):
    ...         return self.weight
    ... 
    >>> myBasket = Basket()
    >>> myBasket.weight = 0
    >>> myBasket.addContent(4)
    >>> myBasket.addContent(1)
    >>> myBasket.getContent()
    5
    >>> myBasket.getContent() + 3
    8

Note the variable **item**. **item** is a *parameter* to the method, which means that its value is assigned when the method is *called*. **self** is a special parameter that's allways present - it contains the current object, in this case **myBasket**.

To make the basket more usefull, let's make it contain a list of items:

    >>> class Basket(object):
    ...     def __init__(self):
    ...         self.content = []
    ...     def addContent(self, item):
    ...         self.content.append(item)
    ...     def getContent(self):
    ...         content = 0
    ...         for item in self.content:
    ...             content = content + item
    ...         return content
    ...     def getContentItems(self):
    ...         return self.content
    ... 
    >>> basket1 = Basket()
    >>> basket1.addContent(5)
    >>> basket1.addContent(10)
    >>> basket1.getContent()
    15

How would you write a getAverageWeight method?

# Flow control
Doing things only if some condition is True:

    if expression:
        statements
        ...
    else:
        statements
        ...

Doing things for each item in a list:

    for item in list:
        statements using the variable item
        ...

Doing things over and over as long as some condition is True

    while expression:
        statements executed over and over again until expression is False
        ...
 
# Modules
We've now started writing complicated enough code that copy-pasting it into the prompt over and over is a bit cumbersome, and soon it will also be hard to organize the growing amount of code.

    class Basket(object):
        def __init__(self):
            self.content = []
        def addContent(self, item):
            self.content.append(item)
        def getContent(self):
            content = 0
            for item in self.content:
                content = content + item
            return content
        def getContentItems(self):
            return self.content

The Basket class above can be placed inside a file called **basket.py**. This file casn then be loaded from python using the **import** statement:

    >>> import basket
    >>> basket1 = basket.Basket()
    >>> basket1.addContent(5)
    >>> basket1.addContent(10)
    >>> basket1.getContent()
    15

Note the **basket.Basket()**. The import call assigns a *module object* to a variable with the same name as the module. All the global variables created inside the module file are available as attributes on the **module object**, in this case the **Basket** class.
