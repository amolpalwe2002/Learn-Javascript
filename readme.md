# Java is as similar to Javascript, as a Car is similar to Carpet

## What is Javascript Engine?
1. V8
2. SpiderMonkey

```
// print on the console
console.log("Hello World");
```

## What ES(ECMAscript) version is good for us
--> ES6

## Variables and Datatypes in JS
var, let and const

```
// declaring and initialising variables
var fullName = "Amol Palwe";
var isLoggedIn = true;
var loggedCount = 14;

console.log(loggedCount);
console.log("loggedCount");

var paymentMethod;
paymentMethod = "Credit Card";
```

## Creating user signup
```
const UID = "1234567890";

// Assignment to const variable
// UID = "0987654321";

var firstName = "John";
var lastName = "Doe";
var email = "pCJ0h@example.com";
var password = "123456";
var verifyPassword = "123456";

console.log(`Hello ${firstName} ${lastName}! 
You can email me at ${email} and 
my UID is ${UID}.`);

```

## Operators
"+", "-", "*", "/", "%", ">", "<"
--> Math library
--> Operator precedence

## What are conditionals in JS
```
var temperature;

// TODO: Go to GOOGLE and fetch data
temperature = 20;

if(temp < 30){
    console.log("it's cold outside");
}else{
    console.log("it's hot outside");
}

// Allow user to logIn if:
// 1. logged in form email
// 2. logged in form Google
// 3. logged in form facebook

var loggedInUsing = "Instagram";

if(loggedInUsing == "Google" || loggedInUsing == "facebook" || loggedInUsing == "email"){
    console.log("You are logged in using " + loggedInUsing);
}else{
    console.log("You are not logged in");
}

```

## Ternary Operator
```
var age = 20;
var result = age>18 ? "You can vote" : "You can't vote";
console.log(result);

```
## Switch case

```
// Authorization differnt users
// 1. Admin - full-access
// 2. subAdmim - create/delete content
// 3. users - read only access

var user = "subAdmin";

switch (user) {
    case "admin":
        console.log("Full access");        
        break;
    case "subAdmin":
        console.log("Create/delete content");
        break
    default:
        console.log("Read only access");
        break;
}
```

## Coercion and Falsy values
- falsy values (considered as false)
1. undefined
2. null
3. NaN
4. 0
5. ""

## Functions in JS
```
function sayHello(name = "Amol") {
    console.log(`Hello ${name}`);
}

sayHello("John");
sayHello("Carry");
sayHello();

function namaste(name = "Amol") {
    return `Namaste ${name}`;
}

console.log(namaste("John"));


/*
Define a function to answer the role of the user
1. Admin - full access
2. SubAdmin - access to create/delete courses
3. User - read only access
4. other - no access
*/

function roleChecker(name, user) {
    if (user === "admin") {
        return `Full access for ${name}`;
    } else if (user === "subAdmin") {
        return `create/delete courses for ${name}`;
    } else if (user === "user") {
        return `read only access for ${name}`;
    } else {
        return "`No access for ${name}`";
    }
}

console.log(roleChecker("Deep", "subAdmin"));
```

## Context in JS
```
// Execution context
console.log(fullName);
sayHello("Amol Palwe");

var fullName="Amol";

function sayHello(name){
    console.log(`Hello ${name}`);
}

<!-- 
function declared is scanned and made available
variable declared is scanned and are made undefined
 -->
```

## Scope chaining in JS
```
var fullName = "Amol Palwe";

console.log(`Hello ${fullName}`);

function sayHello1(fullName = "John Doe") {
    console.log(`Hello ${fullName}`);
}
function sayHello2(fullName = "Carlos") {
    console.log(`Hello ${fullName}`);
}

sayHello1();
sayHello2();

```

## THIS in JS
```
console.log(this);

let user = {

    name: "John",
    age: 30,
    isAdmin: true,
    getUserName: function(){
        console.log(this);

        function sayHi(){
            console.log(this);
        }
        sayHi();
    }
}

user.getUserName();

```

## Array in JS
```
var arr = ["Amol", "Palwe", "Java", "Script"];
console.log(arr);
arr.pop();
console.log(arr);
arr.push("Hello");
console.log(arr);
arr.unshift("Hi");
console.log(arr);
arr.shift("Hi");
console.log(arr);
console.log(arr.length);
console.log(arr.indexOf("Java"));
```

## Callback and Arrow function
```
var isEven = (number) => {
    return number % 2 === 0;
}

// console.log(isEven(4));

console.log([8, 2, 6, 4].every((e) => {
    return e % 2 === 0;
}));
```

## fill and filter methods
```
const arr = [1,2, 3, 4, 5, 6, 7, 8, 9, 10];

console.log(arr.fill("A", 2, 6));

console.log(arr.filter((num) => {
    return num>=5;
}));
```

## slice and splice methods
```
const users = ["ted", "john", "amol", "deep", "Carry", "Lorem"];

// console.log(users.slice(1, 3));
const arr = users.splice(1, 3, "edited");
console.log(arr);
console.log(users);
// console.log(users.splice(1, 3, "edited"));
```

## Objects in JS
```
let user = {
    firstName: "Amol",
    lastName: "Palwe",
    age: 20,
    email : "amol@gmail.com",
    courseList : [],
    buyCourse : function (courseName){
        this.courseList.push(courseName);
    }
}
user.buyCourse("Javascript");
user.buyCourse("HTML");
console.log(user.email);
console.table(user);
console.log(user);

```

## For Loop in JS
```
// for(let i=0; i<10 ; i++){
//     console.log(i);
// }

const states = ["Maharashtra", "Goa", "Karnataka", 1947, "TamilNadu", "Kerala"];

for(let i=0; i<states.length; i++){
    if(typeof states[i] === "number") break; //continue;
    console.log(states[i]);

}

const states = ["Maharashtra", "Goa", "Karnataka", 1947, "TamilNadu", "Kerala"];

let i=0;
while(i<states.length){
    console.log(states[i]);
    i++;
}

const states = ["Maharashtra", "Goa", "Karnataka", 1947, "TamilNadu", "Kerala"];

states.forEach((state) => (console.log(state)));
```
## forIn and forOf loop in JS
```
// forOf is used for arrays
const companies = ["Google", "Amazon", "Facebook", "Apple"];

for(let company of companies){
    console.log(company);
}

// forIn is used for objects
let user = {
    firstName: "Amol",
    lastName: "Palwe",
    age: 20,
    email : "amol@gmail.com",
    courseList : [],
    buyCourse : function (courseName){
        this.courseList.push(courseName);
    }
}

for(let key in user){
    console.log(key, user[key]);
}

```

## DOM - Document Object Model
```
// Select elements on web page

console.log(document.getElementById("heading").innerHTML);
let heading = document.getElementById("heading");
heading.innerHTML = "Jay Radhe Jay Krishna";

```