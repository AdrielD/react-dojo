### Change the expressions below to ES6 notation.

*Try using, as much as possible: function and object shorthands, string interpolations,*
*let and const, spread operator, param defaults, arrow functions, etc.*
<br/>

```javascript
var alwaysTrue = function() { return true };
```
<br/>

```javascript
var double = function(n) { return n * 2 };
```
<br/>

```javascript
var compare = function(a, b) { return (a >= b) ? a : b; };
```
<br/>

```javascript
var buildMultiplication = function(factor) { return function(n) { return n * factor } };
```
<br/>

```javascript
setInterval(function() { console.log("hi!") }, 1000);
```
<br/>

```javascript
var buildPotato = function(name, cookMethod) {
    return {
        name: name,
        cook: function() { return cookMethod() + " potato!"; },
    };
}
```
<br/>

```javascript
var defaults = function() {
    var defaultAge = 30;
    if (age === undefined || age === null) {
        return defaultAge;
    else {
        return age;
    }
};
```
<br/>

```javascript
var times = 10;
"Hello World, 10 times!" === "Hello " + "World, " + times + " times!"; //true
```
<br/>

```javascript
var options = function(options) {
    return { name: options.name, age: options.age, profession: options.profession };
};
```
<br/>

```javascript
var array1 = [1, 2, 3, 4, 5];
var array2 = [];
for (var i = 0; i < 5; i++) {
    array2.push(array[i]);
}
array1 === array2; //true
array2[2] = 10;
array1 === array2; //false
```
<br/>

```javascript
var obj = { name: "potato", color: "yellow" };
var obj2 = obj1;
obj2.state = "fried";
```
<br/>
