Python Coding Standards
=======================

Use explicit imports
--------------------

Don't use::

  from foo import *
  Bar()


Use::

  from foo import Bar
  Bar()


Or::


  import foo
  foo.Bar()

Why?
~~~~

Importing * makes it harder to track where an object comes from, and can often have unforseen side effects (unless the imported module defines __all__).


Lambda Functions
----------------

Minimise the use of lambdas. If a single line of code takes more than a few seconds to understand, it's almost certainly too complicated. Lambdas have their place, but are easily abused.