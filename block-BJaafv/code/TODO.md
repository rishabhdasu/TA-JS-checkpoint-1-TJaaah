1. What is the difference between the two `sum` function given below?

```js
// first
function sum(a, b) {
  return a + b;
}

// second
function sum(a, b) {
  console.log(a + b);
}
```
The main difference is between the above 2 functions is that the 1st one has the return statement whereas the 2nd one doesn't. Therefore, the second function will give an undefined value because when we are calling a function there always should be a return statement.


2. If we store the returned value of both functions above in variable `first` and `second` what will be the value of `first` and `second`.

The value of first will be the sum of two numbers whereas in the second varibale will return undefined because of missing return statement.

3. What will be the output when you call above `sum` function (first) with three parameter like `sum(12, 24, 35)`. Explain why?

- The result will be 36 because in the functions we have taken only 2 parameters to take the values so only the first 2 values willbe passed.

4. Can you store the first `sum` function in a variable named `add`. If yes why? If no why?

- Yes, we can store the function 'sum' in a variable 'add' like this (let add = sum (2,5);), the reason we can do this is because functions are objects and objects are values or expressions which can be stored  in a variable.

5. Declare a function named `sayHello` the accepts a parameter `name` and returns the name like `Hello Arya`.

```
function sayHello(name){
   name = "Arya";
   return `Hello ${name}`
}

6. What will be the output of the function below and why?

```js
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  return message;
}

showMessage();

```
- Output of the above code wil be - "Hello, John"
We are declaring the variable userName outside the function but it can be called inside the function when required on the other hand if we would have declared it inside the function and would have tried to use it outside the function then it won't work, because we cannot directly use the variables used inside a function instead we need to call the function.

7. What will be the output for `Output1` `Output2` and `Output3` in the code below.

```js
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  return message;
}

alert(userName); "John"

showMessage(); "Hello John"

alert(userName); "John"
```

8. What is a Anonymous Function give example of three functions.

An anonymous functions are those which do not have any names. Examples:

let sum = function (a, b){
  return a + b;
}

let numb = function (num){
  num = +prompt(`Enter a number`);
  return num + 1;
}

let prod = (a, b) => {
  return a*b;
}

9. Can function declaration be a Anonymous Function? Explain

Yes, functions declaration can be anonymous. When we declare function expressions we store the function inside a variable so when we store it a variable then we don't need the function, we will have to call the function with the variable name so we don't need any function name.

10. Give 5 example of good naming convention for defining a function. You can read the details below to do that.

```md
Functions are actions. So their name is usually a verb. It should be brief, as accurate as possible and describe what the function does, so that someone reading the code gets an indication of what the function does.

It is a widespread practice to start a function with a verbal prefix which vaguely describes the action. There must be an agreement within the team on the meaning of the prefixes.

For instance, functions that start with "show" usually show something.

Function starting with…

"get…" – return a value,
"calc…" – calculate something,
"create…" – create something,
"check…" – check something and return a boolean, etc.

```
1. Converting minute into seconds.

function minToSec(intMin) {
  return intMin * 60;
}

2. Check wether the number lies within the range of a lower and upper bound.

  function isInRange(lower, upper, numb) {
  if(numb >  lower && numb < upper){
    return true;
  }else{
    return false;
  }
}

3.  Calculate BMI (Body Mass Index) :

  function calculateBMI(weight, height) {
  let bmi = weight / (height * height);
  if(bmi < 18.5){
    return `Underweight`;
  } else if(bmi >= 18.5 && bmi <= 24.9){
     return `Normal`;
  } else if(bmi >= 25 && bmi <= 29.9){
    return `Overweight`;
  }else {
    return `Obese`;
  }
}

4.  Convert celcius to fahrenhiet :

  function celsiusToFahrenheit(temp) {
  temp = +prompt(`Enter temperature in Celcius`);
  return  `Temperature in fahrenheit is ${(temp*9)/5 + 32}`;
}

5.  Check the type of the value :

function typeCheck(type) {
  type = prompt(`Enter a value`);
  return typeof type;
}