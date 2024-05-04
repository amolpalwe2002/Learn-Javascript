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
