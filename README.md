# Flutter and Dart Internals 

### 3 Starting project 
Getting started with how UI is updated. A widget first executes the creation of the element of widget. Then, it runs the `Build()` method.

### 4 Refactor & Extract widgets to avoid unnecessary builds.

If any Statefull widget, that contains an element that updates on every `Build()` method runs, Then the element only is executed and not the complete *Widget Tree* .
