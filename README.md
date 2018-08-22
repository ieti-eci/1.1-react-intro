# React-intro
Introduction to ReactJS.

# Part 1: Create a basic React Application and understand React basics

1. Create a react App and test that it works:

```javascript
  npx create-react-app todo-app
  cd my-app
  npm start
```
2. Open the index.html file and replace the title tag from React App to TODO App.

3. Open the App.js file and change App-title to TODO React App (verify if the changes are reflected inmediately on your browser after you save without re-running your server).

4. Go to Codeacademy, register and do the first modules of the following course the get a basic understanding of React: https://www.codecademy.com/learn/react-101

# Part 2: Create React Components for the TODO App

1. Create a new JavaScript file called *Todo.js* 

```javascript

import React from 'react';

export class Todo extends React.Component {

    constructor(props) {
        super(props);
    }   

    render() {
        return (  
          //Add your code here to represent a TODO
        );
    }

}
```
2. Read about React Components & Props:  https://reactjs.org/docs/components-and-props.html

3. Once your understand these concepts, then add the HTML code to display the TODO information. You will access the TODO data by using the react props *text* ,  *priority* and *dueDate* as the following example (notice the curly braces inside the HTML used to evaluate the JavaScript expression)

```javascript
<h2>{this.props.text}  ... </h2> 
//Do not forget to add the other properties of your TODO!
```

4. Create another React Component called TodoList. This Component should render a list of Todo components. You can access the todo list by using the props: *this.props.todoList*. Start by importing the Todo component and the React module:

```javascript
import React from 'react';
import {Todo} from './Todo'
```

hint: You should use the map function to dynamically create your list inside the render method as the following example: https://codepen.io/gaearon/pen/jrXYRR?editors=0011

React Documentation: https://reactjs.org/docs/lists-and-keys.html 

5. Import your TodoList component into the App.js file and then add the <TodoList> tag to your code so it loads the Todo list.
  You can use the following code to create some sample data:

```javascript
render() {
      const todos = [{text:"Learn React", priority:5, dueDate: new Date() },
          {text:"Learn about APIs", priority:4, dueDate: new Date(2018,8,30) },
          {text:"write TODO App", priority:3, dueDate: new Date(2018,9,30) }];
 
 ...
 
 <TodoList todoList={todos}/>
```

6. Run your application and verify that it works as expected:

```javascript
  npm start 
```


# Part 3: Interacting with React Components

