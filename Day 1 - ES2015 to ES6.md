### Change the expressions below to ES6 notation.

*Try using, as much as possible: function and object shorthands, string interpolations,*
*let and const, spread operator, param defaults, arrow functions, etc.*
<br/>

```javascript
var alwaysTrue = function() { return true };
```
<details>
<summary>Possible solution</summary>

```javascript
const alwaysTrue = () => true;
```
</details>
</hr>

```javascript
var double = function(n) { return n * 2 };
```
<details>
<summary>Possible solution</summary>

```javascript
const double = n => n * 2;
```
</details>
</br>

```javascript
var compare = function(a, b) { return (a >= b) ? a : b; };
```
<details>
<summary>Possible solution</summary>

```javascript
const compare = (a, b) => (a >= b ? a : b);
```
</details>
</br>

```javascript
var buildMultiplication = function(factor) { return function(n) { return n * factor } };
```
<details>
<summary>Possible solution</summary>

```javascript
const buildMultiplication = factor => (n => n * factor);
```
</details>
</br>

```javascript
setInterval(function() { console.log("hi!") }, 1000);
```
<details>
<summary>Possible solution</summary>

```javascript
setInterval(() => (console.log("hi!")), 1000);
```
</details>
</br>

```javascript
var buildPotato = function(name, cookMethod) {
    return {
        name: name,
        cook: function() { return cookMethod() + " potato!"; },
    };
}
```
<details>
<summary>Possible solution</summary>

```javascript
const buildPotato = (name, cookMethod) => ({ name, cook: () => (`${cookMethod()} potato!`) });
```
</details>
</br>

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
<details>
<summary>Possible solution</summary>

```javascript
const defaults = (defaultAge = 30) => defaultAge;
```
</details>
</br>

```javascript
var times = 10;
"Hello World, 10 times!" === "Hello " + "World, " + times + " times!"; //true
```
<details>
<summary>Possible solution</summary>

```javascript
const times = 10;
"Hello World, 10 times!" === `Hello World, ${times} times!`;
```
</details>
</br>

```javascript
var options = function(props) {
    return { name: props.name, age: props.age, profession: props.profession, salary: 12000 };
};
```
<details>
<summary>Possible solution</summary>

```javascript
const options = ({ name, age, profession }) => ({ name, age, profession, salary: 12000 });
```
</details>
</br>

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
<details>
<summary>Possible solution</summary>

```javascript
const array1 = [1, 2, 3, 4, 5];
const array2 = [...array1];
```
</details>
</br>

```javascript
var obj = { name: "potato", color: "yellow" };
var obj2 = obj1;
obj2.state = "fried";
```
<details>
<summary>Possible solution</summary>

```javascript
const obj = { name: "potato", color: "yellow" };
const obj2 = { ...obj, state: "fried" }
```
</details>
</br>
