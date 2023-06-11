Classes are methods
===================

It is useful to think of classes as methods because it helps you refactor them and test them. It also helps you think about methods in a way that allow you to convert long methods into classes systematically.

In its simple form, a class is equivalent to a method in this way:

```ruby
def add(left, right)
  left + right
end

a = add(1, 2)
```

```ruby
class AdditionMethod
  def initializer(left, right)
    @left = left
    @right = right
  end
  
  def perform
    @left + @right
  end
end

a = AdditionMethod.new(1, 2).perform
```

As you can see the constructor of a class is basically the parameter list of a method. The constructor acts as a way to accept the parameters and store them.

A `perform` method then performs the core task of the method, and returns its results.

Why so much fuss for such a simple method
-----------------------------------------



Testing
-------




Why you shouldn't do anything in the constructor
------------------------------------------------


Private methods?
----------------



Languages without 'classes'
---------------------------

Some languages that don't have classes as a language construct also actually have some sort of equivalent.


Algorithms and loops
--------------------

Many algorithms tend to be presented as nested loops and conditional breaks. We can examine here how these can also be broken down into easier to read classes.


Classes that don't look methody
-------------------------------

Occasionally classes that were written before are made in a way that do not fit the idea of being called once. Classes like these can also actually be treated like methods and refactored.
