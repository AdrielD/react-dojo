### Change the expressions below to ES6 notation.

*Try using, as much as possible: function and object shorthands, string interpolations,*
*let and const, spread operator, param defaults, arrow functions, etc.*


a)
```javascript
var alwaysTrue = function() { return true };
```


b)
```javascript
var double = function(n) { return n * 2 };
```


c)
```javascript
var compare = function(a, b) { return (a >= b) ? a : b; };
```


d)
```javascript
var buildMultiplication = function(factor) { return function(n) { return n * factor } };
```


e)
```javascript
setInterval(function() { console.log("hi!") }, 1000);
```


f)
```javascript
var buildPotato = function(name, cookMethod) {
    return {
        name: name,
        cook: function() { return cookMethod() + " potato!"; },
    };
}
```


g)
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


h)
```javascript
var times = 10;
"Hello World, 10 times!" === "Hello " + "World, " + times + " times!"; //true
```


i)
```javascript
var options = function(options) {
    return { name: options.name, age: options.age, profession: options.profession };
};
```


j)
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


k)
```javascript
var obj = { name: "potato", color: "yellow" };
var obj2 = obj1;
obj2.state = "fried";
```
