ng-simple-todo
==============

A Simple TODO list management application built using AngularJS.The whole purpose behind this application is to introduce AngularJS to developers who are new to it.It demonstrates some basic but important features of AngularJS which would help novices to start getting hands-on using AngularJS in real-world applications or at-least should be able to read and understand already existing AngularJS applications. A brief listing of AngularJS features(in order) this application introduces:

1. Including AngularJS library in HTML file
2. Marking an HTML element as an AngularJS app using `ng-app` attribute (in AngularJS it is termed as `directive`)
3. Analysing the data and behaviors and categorizing those to be part of Model, View and Controller aspects of MVC Pattern supported by AngularJS.As a part of doing this introduced:
  - how to define a model data
  - how to define a Controller in AngularJS, 
  - the $scope service object used in a controller and how model data can be binded to $scope object
  - how to mark a container in HTML to be processed by a controller.This marking is facilitated by AngularJS's `ng-controller` directive,
  - double-curly braces `{{}}` syntax for evaluating AngularJS expressions
  - `ng-repeat` directive that tells AngularJS to generate the element it is applied to and its contents for each object in a collection.
4. The powerful Two-way Model Binding supported by AngularJS which demonstrates how the model is used to generate elements AND changes in the element cause corresponding changes in the model.As part of this `ng-model` is introduced which helps in achieving this two-way model or data binding.
5. Adding behaviors to the controller.Demonstrated the working of behavior, in context of the application, by dynamically updating the TODO list items count in the header when user marks one ore more items as complete.As part of this `ng-hide` directive is introduced which hides the element it is applied to - and its content elements - if the expression that is assigned as the attribute value evaluates to true (boolean).
6. Adding behavior in the controller which depends on another behavior already present.Demonstrated the working of  behavior, in context of the application, by applying `label-warning` and `label-success` CSS classes (of [Twitter Bootstrap](http://getbootstrap.com/)) dynamically by examining the incomplete TODO items count.As part of this introduced the AngularJS's `ng-class` directive which applies the CSS class returned by the behavior.Also demonstrated that an HTML element can use multiple AngularJS directives, each of which relies on a different behavior to get the effect we require in an application.
7.


Folders
=======

```
- css        -- Holds the Twitter Bootstrap (3.x) stylesheets
- scripts    -- Holds the stable AngularJS library
- util       -- Holds a simple web-server created using NodeJS
- todo.html  -- A Single Page simple TODO-list application built using HTML and AngularJS
- todo.json  -- A JSON data file serving initial data to todo.html
```

Assumptions
===========

The instructions below assume that you are working on Linux-based system like Ubuntu.


Setup Pre-requisites
===================

1. [NodeJS](http://nodejs.org/) must be installed prior running the web server located at `util/web_server.js`.For installation instructions please refer [Installing Node and NPM in 30 seconds][2]


Usage
=====

1. Clone the application on your disk at a location say `/home/<user_name>/ng-simple-todo` (henceforth in the document this will be referred to as `$APP_ROOT`).
2. Change directory to `$APP_ROOT`.
3. Run the following command `APP_ROOT$ npm install connect` to install the `connect` module used as a dependency by the `util/web_server.js` to implement the server.
4. Run the following command `APP_ROOT$ node ./util/web_server.js` to start the web server.**Please note** that the application name `ng-simple-todo` is hard-coded in the file `util/web_server.js` so in case changing the application root folder name then accordingly update it in `util/web_server.js` else you would not be able to start the web server successfully.
5. Open a browser and open the following link: `http://localhost:5000/todo.html` and you should be able to see a default TODO list.


AngularJS Features Demonstration
================================

This application demonstrates the basic but important features of AngularJS by building a simple TODO List management.

The application is built in an incremental manner starting with a static HTML mockup of TODO List.Then step-by-step AngularJS features are introduced to it to make it dynamic and usable.

The incremental changes made while implementing this application can be referred from the HTML comments added in `todo.html` source code in each commit.The starting point of reference is the  [commit](975d00585cda5981601f54bce9aa6a5c507b4800) and ending point of reference is the [commit](ae08f183163f0bf04bbcaa9d4e94cbca59dc2382).





Courtesy
--------

This application has been built using content from the book [Pro AngularJS](http://www.apress.com/9781430264484) by **Adam Freeman**



[1]: http://www.joyent.com/blog/installing-node-and-npm/  "Installing Node and NPM"
[2]: https://gist.github.com/isaacs/579814#file-node-and-npm-in-30-seconds-sh "Installing Node and NPM in 30 seconds"
