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

### 6 Why Keys are useful? 
- The keys plays a vital role in tracking down the widget.
- For Example, 3 todo items are listed here, when sorted , their position might change too. But flutter keeps the track of widgets, & doesn't recreate widgets' element, It instead reuses the element & displays the widget.
- But, when using the `CheckableTodoItem()` widget, & marking a widget and sorting on the go, it changes the serial and points another widget according to the position.
- So, ultimately keys are useful to track down widget, so that updates could be tracked too.