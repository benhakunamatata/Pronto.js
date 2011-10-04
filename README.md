# Pronto.js

Pronto is a Node.js library that allows you to declare a sequence of tasks.

## Airplane View

Pronto.js is a simple tool for executing a sequence of tasks. It looks declarative -- you create a list -- but in the background, Pronto takes full advantage of Node's event model. The result is that you can easily write very fast code.

There are only two things you need to know how to do:

### Declare a List of Tasks (or Commands)

Pronto provides a fluent interface for declaring your task list:

    pronto = require('pronto');
    
    pronto.register.request('hello')
      .doesCommand('print-hello')
      .whichInvokes(pronto.HelloCommand);

The above creates a new instance of the `pronto` toolkit and registers a single request.  

### Create a Task (or Command)

Creating a task is as simple as extending the base task prototype, implementing just a method or two:



## Acknowledgements

Tom Derykere coined the name for this module.
Alex Daw and Sam Boyer provided input at the outset.
Some of the patterns are derived from [Fortissimo](http://github.com/technosophos/Fortissimo).

This project was sponsored by [ConsumerSearch.com](http://www.consumersearch.com), part of the About.Com network, a New York Times company.
