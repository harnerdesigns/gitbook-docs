# JavaScript

In order to understand how **Frontity** works and be able to modify its files and develop your own project, it would be necessary to understand the main JavaScript concepts that we use in our code. The number of them could seem overwhelming, but most of them are pretty simple.

{% hint style="info" %}
Note this guide purpose is to give you a better understanding of which JavaScript concepts we use at **Frontity**, and a brief explanation of them. If you want a more detailed way of learning JavaScript you can check other guides like [freeCodeCamp](https://www.freecodecamp.org/) or [w3schools](https://www.w3schools.com/js/default.asp).
{% endhint %}

* \*\*\*\*[**Javascript concepts**](javascript-basics.md#javascript-concepts)\*\*\*\*
  * [Comments](javascript-basics.md#comments)
  * [Variables](javascript-basics.md#variables)
  * [Strings](javascript-basics.md#strings)
  * [Numbers](javascript-basics.md#numbers)
  * [Objects](javascript-basics.md#objects)
  * [Arrays](javascript-basics.md#arrays)
  * [Functions](javascript-basics.md#functions)
  * [Operators](javascript-basics.md#operators)
  * [If-else](javascript-basics.md#if-else)
  * [Switch](javascript-basics.md#switch)
  * [For loops](javascript-basics.md#for-loops)
  * [While loops](javascript-basics.md#while-loops)
  * [RegExp](javascript-basics.md#regexp)
* \*\*\*\*[**ES6 concepts**](javascript-basics.md#es6-concepts)\*\*\*\*
  * [Variables \(let & const\)](javascript-basics.md#variables-let-and-const)
  * [Arrow functions](javascript-basics.md#arrow-functions)
  * [Default parameters](javascript-basics.md#default-parameters)
  * [Destructuring assignment](javascript-basics.md#destructuring-assignment)
  * [Template strings](javascript-basics.md#template-strings)
  * [Import and export](javascript-basics.md#import-and-export)

## JavaScript concepts

### Comments

As in most of programming languages, you are able to include comments in your code. You can write single-line comments with `//` and multi-line comments between `/*...*/`

```javascript
// Single-line comment.
/*
Multi-line comment.
*/
```

### **Variables**

You can store data inside variables in order to be used later. ****For creating one you just have to define it and assign a value.

```javascript
var number1 = 3;
var number2 = 2;
var total = number1 + number2 // Total value would be 5.
```

JavaScript variables can hold many **data types**: numbers, strings, objects and more.

Since the [ES6 update](https://www.freecodecamp.org/news/write-less-do-more-with-javascript-es6-5fd4a8e50ee2/) there are other ways of declaring variables. We explain them later at [ES6 variables \(let, const\)](javascript-basics.md#variables-var-let-and-const).

### Strings

 Strings are used for storing text and can be defined between double or single quotes.

```javascript
var text1 = "This is a string";
var text2 = 'This is also a string';
```

There are some specific methods to work with strings that could be useful. You can check [this guide](https://www.w3schools.com/js/js_string_methods.asp) to see some examples, although it is not needed to work with Frontity.

Since the [ES6 update](https://www.freecodecamp.org/news/write-less-do-more-with-javascript-es6-5fd4a8e50ee2/) there is also a new way of declaring strings, more versatile than single and double quotes. We explain them later at [ES6 template strings](javascript-basics.md#template-strings).

### Numbers

Numbers can be written with or without decimals.

```javascript
var number1 = 5; // This is a number.
var number2 = 5.6; // This is also a number.
```

There are some specific methods to work with numbers too. Although not needed to understand Frontity, you can check [this guide](https://www.w3schools.com/js/js_number_methods.asp) to see some examples.

### Objects

Objects are also variables and they can store multiple values, assigning values to properties. You define objects this way:

```javascript
var person = {
  firstName: "Jon",
  lastName: "Snow",
  age: 40
};
```

This way, we have the variable `person` with as many properties-values as we want. You can access/modify the value of a specific property in two different ways:

```javascript
var name1 = person.firstName;
var name2 = person["firstName"]; // Both return the same value.
```

Object properties can also store other objets, like this:

```javascript
var person = {
  name: {
    first: "Jon",
    last: "Snow"
  },
  age: 40
};
```

### Arrays

Arrays store multiple values as a list of items.

```javascript
var pets = ['dog', 'cat', 'turtle'];
```

You can store as many items as you want, and they don't need to be strings, they can be anything you want, even objects. In order to access/modify an array item, you have to specify its position \(starting at 0\):

```javascript
var item1 = pets[0]; // Returns 'dog'.
var item2 = pets[1]; // Returns 'cat'.
var item3 = pets[2]; // Returns 'turtle'.
```

Arrays are an important part of JavaScript and there are lots of array methods that will simplify your logic. You can check a extended list of them at [w3schools array reference](https://www.w3schools.com/jsref/jsref_obj_array.asp). We consider specially interesting:

* [myArray.forEach\(\)](https://www.w3schools.com/jsref/jsref_foreach.asp): to run a function for each array element.
* [myArray.filter\(\)](https://www.w3schools.com/jsref/jsref_filter.asp): to create a new array with every element in an array that pass a test.
* [myArray.map\(\)](https://www.w3schools.com/jsref/jsref_map.asp): to create a new array with the result of calling a function for each array element.

### Functions

A JavaScript function is a chunk of code intended to perform a specific task. You have to define it first and call it later. You can pass parameters to the function to return a different value depending on the parameters.

```javascript
// Defining the function.
function myFunction(parameter1, parameter2) {
  return parameter1 + parameter2;
}
// Calling the function with specific parameters.
myFunction(2, 3); // It will return 5.
myFunction(5, 4); // It will return 9.
```

Since [ES6 update](https://www.freecodecamp.org/news/write-less-do-more-with-javascript-es6-5fd4a8e50ee2/) there are other ways of declaring functions that are commonly used and make your code easier to understand. We explain them later at [ES6 arrow functions ](javascript-basics.md#arrow-functions).

### Operators

In JavaScript, there are many types of operators. We could divide them this way:

* **Arithmetic Operators:** To perform arithmetics like addition \( `+` \), subtraction \(`-`\), multiplication \(`*`\), etc.
* **Assignment Operators:** To assign values to variables \(`=`\).
* **Comparison Operators:** To test if a condition is true/false. It could be `x === y`, `x < 5`, `x > 20`...
* **Logical Operators:** To add some logic to the comparison statement.  For example in this statement`x < 5` **`&&`** `y > 25`  "x" must be less than 5 **AND** "y" must be more than 25**.**

These are just some examples of JavaScript operators, there is a good summary at [**w3schools JavaScript Operators**](https://www.w3schools.com/js/js_operators.asp) ****to fully understand them.

In JavaScript the `==` and `!=` operator exist, but they are never used because sometimes they don't behave properly \(i.e.  `0 == ""` is true!\). For that reason everybody always use three equals: `===` and `!==` for comparisons.

### If-else

Conditional statements are used to run different code based on different conditions. You can define an `if-else` statement this way:

```javascript
if (condition1) {
  // Run this code if condition1 is true.
} else if (condition2) {
  // Run this code if condition2 is true.
} else {
  // Run this code if condition1 and condition 2 are both false.
}
```

You can add as many `else if` \(each one with it condition\) as you want, and it will run the code of the first one that match true. Moreover, you can use `if-else` without any `else if`, or even without the `else` statement, and it will continue with the rest of the code if `condition1` is false.

{% hint style="info" %}
In React, `if-else` statements don't work, and instead we have to use operators and ternary expressions. It is more detailed at [React basics - Special cases](react-basic.md#if-else-statements-dont-work).
{% endhint %}

### Ternary operator

In JavaScript there's another way to do conditionals: using [ternary operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator).

```javascript
condition ? /* Runs when condition is true */ : /* Runs when condition is false */;
```

They are useful when defining variables, like this:

```javascript
// Assign the blue color when age is above 30 and yellow when is below. 
var color = person.age > 30 ? "blue" : "yellow"
```

They are also useful in React, but we'll see that later.

### Switch

Switch statements are similar to `if-else`, and they let you run different code depending on a condition. This is the way to define them.

```javascript
switch(value) {
  case 1:
    // Run this code if value === 1.
    break;
  case 2:
    // Run this code if value === 2.
    break;  
  default:
    // Run this code if no case match.
}
```

Again, you can define as many cases as you want, and if none of them match, the default would run.

### For loops

This statement is really useful if you want to perform the same code, with different values, a lot of times. For doing so you have to define 3 statements:

```javascript
for (i = 0; i < 5; i += 1) {
  // Code block to be executed.
}
```

* **Statement 1** \(`i = 0`\): The initial value when the loop starts.
* **Statement 2** \(`i < 5`\): The condition that has to match to finish the loop.
* **Statement 3** \(`i += 1`\): This is optional and is executed after each loop iteration. Usually used to change the value before running the next loop iteration.

{% hint style="info" %}
It is common to use `for loops` to run the same code at every array item. For doing so, we strongly recommend to use the [forEach\(\) method](https://www.w3schools.com/jsref/jsref_foreach.asp) instead of it.
{% endhint %}

### While loops

It is related to `for loops`, and it performs the same code while a condition is true. You have to make sure that you change the condition in the code to not create infinite loops.

```javascript
while (condition1) {
  // Code block to be executed.
}
```

There is a similar loop called `do/while` which is a variant of the while loop. The only difference is that it will execute the code block once, before checking if the condition is true, and continue until the condition is `true`.

```javascript
do {
  // Code block to be executed.
}
while (condition);
```

### RegExp

The Regular Expressions \(RegExp\) are really useful in JavaScript as they let you match a pattern, and it can be used for example for defining a more complex condition.

They can be overwhelming, so if you are not familiar with them don't worry. We would recommend you to try to understand each particular case once you find them in our code, and know they exist as they could be useful in your code. Again, don't worry and just learn the concepts once you need them. This way, you will learn step by step and it will be easier.

For learning the basics and help you understand or create some RegExps, you can use [w3schools guide](https://www.w3schools.com/js/js_regexp.asp), [freeCodeCamp regExp](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/regular-expressions) and also [RegExr](https://regexr.com/) to test them.

## ES6 concepts

There are some features introduced with [ES6 update](https://www.freecodecamp.org/news/write-less-do-more-with-javascript-es6-5fd4a8e50ee2/) that are widely used across Frontity:

### Variables \(let and const\)

We previously defined variables with the statement `var`, however, since ES6, it is not used at all. Instead, people use `let` and `const` :

* **Const** is used in almost 100% of the cases in Frontity, and it implies that the variable can't be reassigned, it has a constant value.
* **Let** is used when you want to iterate through that variable and you would like to reassign its value.

There are lightly differences between `let` and `var` too and you can check them [here](https://www.w3schools.com/jS/js_let.asp), but they are not that important and `var` is not commonly used anymore.

### Arrow functions

It is a new way of defining functions that make them shorter. Here you can see an example of how to declare the same function with and without arrow functions:

#### _Without arrow functions_

```javascript
const hello = function(name){
    return 'Hi ' + name + ', nice to meet you!';
}
hello('Jon');
```

#### _With arrow functions_

```javascript
const hello = (name) => {
    return 'Hi ' + name + ', nice to meet you!'
};
hello('Jon');
```

As you can see, the common way of using them is deleting the word `function` and adding `=>` just after it.

However, sometimes the syntax can be even smaller. If your function is just composed of a `return` statement, you can change the curly braces `{ }` for parentheses `( )`, delete the `return` statement and it will interpret it must return the whole function.

```javascript
const hello = (name) => (
    'Hi ' + name + ', nice to meet you!'
);
hello('Jon');
```

You can avoid the parentheses too:

```javascript
const hello = (name) => 'Hi ' + name + ', nice to meet you!';
hello('Jon');
```

But if you return an object, the parentheses are required:

```javascript
const hello = (name) => ({ firstName: name, lastName: "Snow" });
hello('Jon'); // Outputs { firstName: "Jon", lastName: "Snow" }.
```

{% hint style="info" %}
Note that **if we don't want the function to return**, for example if we are defining variables inside it, **we must use the curly braces**.
{% endhint %}

Finally, we can remove the parenthesis from the parameters if only one parameter is used:

```javascript
const hello = name => "Hi " + name + ", nice to meet you!";

const hello2 = (name, surname) => "Hi " + name + surname + ", nice to meet you!";
```

### Default parameters

You can create a default value for one parameter and it will be used if no other value is passed. For doing so, you can use the operator `=` while defining the parameter.

```javascript
const hello = (name = "there") => "Hi " + name + ", nice to meet you" ;

hello("Jon"); // It will return "Hi Jon, nice to meet you".
hello(); // It will return "Hi there, nice to meet you".
```

### Destructuring assignment

This Javascript expression is used to unpack values from arrays or objects properties. It can seem a bit weird at the beginning, but if you get used, it will reduce a lot the lines of code of your project.

#### _Object destructuring_

As mentioned before, destructuring an object lets you assign to a variable the value of one property.

```javascript
const person = {
    name: "Jon",
    lastName: "Snow",
    age: 30
};
const { name, lastName } = person;

// You are assigning the value of person.name to a new variable called "name".
console.log(name); // Returns Jon.
console.log(lastName); // Returns Snow.
console.log(age); // ERROR: age is not defined.
```

As you can see, you select all the variables you want to create using curly braces `{ }`, and equals them to the object properties you want to get the values from. Yes, at the beginning it seems weird, but it is much easier than before ES6. Here you have an example of how to do it with/without destructuring:

```javascript
// With destructuring.
const { name, lastName, age } = person; 

// Without destructuring.
const name = person.name; 
const lastName = person.lastName;
const age = person.age;
```

We are just defining three variables, but imagine doing it with more, you would write much less code.

**You can also assign a different name to the variables** if you want. For example:

```javascript
const { name: a, lastName: b } = person

console.log(a); // Returns person.name.
console.log(b); // Returns person.lastName.
```

This way you are getting the value of `person.name`  and storing it in a variable called "a".

Moreover, you can define a default value for a variable as mentioned [before](javascript-basics.md#default-parameters), just in case the object doesn't have that property defined.

```javascript
const person = {
    name: "Jon",
    lastName: "Snow",
    age: 30
};
const { name, lastName, family = "Stark" } = person;

console.log(family); // Returns Stark even though it's not defined in person.
```

#### _Array destructuring_

They work in a similar way to objects:

```javascript
const items = [10, 20, 30, 40, 50];
const [a, b] = items;

console.log(a); // Returns 10.
console.log(b); // Returns 20.
```

Again, it is the same as object destructuring, instead of using curly braces we use `[ ]`, because we are working with arrays, and it will get values depending on the position.

You can also use default values in case the array length is smaller than the variables defined.

```javascript
const items = [10, 20];
const [a = 35, b = 45, c = 55] = items;

console.log(a); // Returns 10.
console.log(b); // Returns 20.
console.log(c); // Returns 55.
```

As `items` has just two elements they are assigned to the first variables and `c` gets its default value.

If you have any questions, or you want more information about arrays and objects destructuring, it is well explained at the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment).

### Template strings

Template strings \(also called template literals\) are just an easier way to work with strings. To define them you have to use back-ticks \(``` ```\), and these are they main advantages:

* They allow embedded expressions.
* You can use multi-line strings, just by adding a line-break.

Here you have an example showing them:

```javascript
const name = "Jon Snow";

const text = `Hi there!
I am ${name},
and I have killed ${43 + 57} white walkers`;
```

There are more advantages of working with template strings, you can check them in guides like [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) or [Google docs](https://developers.google.com/web/updates/2015/01/ES6-Template-Strings). In Frontity, we will mainly use them for the styles, but you can find them in other parts of the code.

### Import and export

JavaScript lets you export functions \(including components\), classes, objects, or anything else from one module in order to be used in other programs. The same way, you can reuse the ones written by external programs too.

The import and export statements are exactly for this. If you want anything from your module/file to be reused somewhere else, you will use **`export`**, and if you want to use anything external, you will use **`import`**.

#### _Export_

There are two different types of export, **named** and **default**, and depending on each one, the corresponding import will be different. 

* **Named export:** You ****can have multiple named exports per module. It is useful to export many values, and import after just the ones you need.

```javascript
export const Component1 = () => { /* Code of Component1. */ };
export const Component2 = () => { /* Code of Component2. */ };
```

You will be exporting two components, with different names. This will be useful in case you want to import just one of them in other files.

You can also export all the variables at once:

```javascript
const Component1 = () => { /* Code of Component1. */ };
const Component2 = () => { /* Code of Component2. */ };

export {
  Component1,
  Component2
};
```

* **Default export:** You just have one default export per module, and it will be used for the default import.

```javascript
const Component = () => {};

export default Component;
```

#### _Import_

Depending on the export of the source file, the import will be lightly different.

* **From named export**: It is mandatory to use the same name of the corresponding object and you have to include it between curly braces.

```javascript
import { Component1, Component2 } from "./file-name"
```

* **From default export:** Importing from a default export, you can use the name you prefer for your file, just don't include it between curly braces.

```javascript
import Component from "./file-name"
```

Note that in both methods you have to specify the file you are importing from. For more info about these statements you can visit the [import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and [export](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export) documentation.

When you import stuff from files, you have to use `"./"` at the beginning. That way, JavaScript knows that it is a file. For example:

```javascript
import Component from "./file-name"
```

You can also go deep inside folders:

```javascript
import Component from "./some-folder/nested-even-more/file-name"
```

Or go up a level using `"../"` .

```javascript
import Component from "../../file-name" // Up two levels from the current folder.
```

When you import stuff from npm packages \(the ones you install with `npm install`\) you have to use the name of the package directly, without any `"./"` before. Like this:

```javascript
import Component from "some-package-name"
```



There are other important ES6 aspects, but understanding them will give you a wide understanding of Frontity code. Another important concept that is commonly used in React are classes, but since introduction of hooks they are no longer needed, and in Frontity core are not used at all. You may want to take a look at them because they could be used by other packages, but it is not a must to get started.

For more detailed guides about these concepts, including classes, you can visit [https://www.w3schools.com/react/react\_es6.asp](https://www.w3schools.com/react/react_es6.asp).



{% hint style="info" %}
These are the main JavaScript concepts used in Frontity, if you understand them, you will be able to continue with [React basics](react-basic.md) to master Frontity. If you want to go deeper in learning JavaScript, there are a lot of resources out there, and if you have questions don't hesitate to ask them at [our community](https://community.frontity.org/c/dev-talk-questions) ☺️. 
{% endhint %}



