# Flutter and Dart Internals 

### 3 Starting project 
Getting started with how UI is updated. A widget first executes the creation of the element of widget. Then, it runs the `Build()` method.

### 4 Refactor & Extract widgets to avoid unnecessary builds.

If any Statefull widget, that contains an element that updates on every `Build()` method runs, Then the element only is executed and not the complete *Widget Tree* .

### 5 About the Keys.

The **keys** , whether the ones used in for tracking the widget, or the ones used in dictionary .
Here, it is demonstrated how **keys** are useful.
The to-do application starts here, a `todo_item` class is created to store the task name & its priority. 
Now the todo_item object is stored in '_todos[]' list, 
It displays the items as list by wrapping the item w/Expanded widget. 
It also shows the item order as ascending or descending according to priority. 
The list order could be changed using an ElevatedButton places on top , which calls in for a function to change the order of list.