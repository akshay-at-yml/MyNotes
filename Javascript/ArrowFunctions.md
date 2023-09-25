# Arrow Functions

```kotlin
function add(a, b) {
    return a + b;
}
```

```kotlin
const add = (a, b) => {
    return a + b;
}
```

#### Limitations of arrow functions

- Arrow functions do not have **this** key word
- Arrow functions do not have arguments
- Can not be constructors

##### How to create arrow functionss?

###### 1. Single Argument and single statement

```javascript
function add(a) {
  return a;
}
```

is Equivalent to

```javascript
const add = (a) => a;
```

###### 2. More argumments and one statement

Return keyword is not always needed

```javascript
const add = (a, b) => a + b;
```

###### 3. Multiple statements

```javascript
const doSomething = (a) => {
  let b = 10;
  return a + b;
};
```

###### 4. Multiple statements & multiple parameters

```javascript
const doSomething = (a, b) => {
  let c = 10;
  let d = 20;
  return a + b + c + d;
};
```

###### 5. When object is the argument

```javascript
const userObj = {
  name: "John",
  age: 23,
};

// With arrow functions -> short form

const userInfo = (user) => ({ name: user.name, age: user.age });

// Which is equivalent to
const userInfo = (user) => {
  return {
    name: user.name,
    age: user.age,
  };
};
```

##### Object Destruction

```javascript
const userObj = {
  name: "Akshay",
  age: 23,
};

function displayUser(user) {
  return `User is ${user.name} : ${user.age}`;
}

// is equivalent to with object destruction

function displayUser({ name, age }) {
  return `User is ${name} : ${age}`;
}

// Is equivalent to using arrow functions

const displayUser = ({ name, age }) => "User is ${name} : ${age}";
```

##### Array destruction

```javascript
const display = ([name, age]) => {
  return `User is ${name}, ${age}`;
};

console.log(["Akshay", 25]);
```

##### Default values in arrow functions

```javascript
const add = (a, b = 20) => a + b;

add(10);
```

##### Anonymous functions
```javascript
(function(a, b) {
    return a + b
})(3, 5)
// In arrow functions

((a, b) => a + b)(2, 3)
```
