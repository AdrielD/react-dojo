### Given an input, write a function to return the expected output in each case.

*Avoid using `for` loops. Instead, use `map`, `reduce` or `filter` functions, so no state is mutated.*
*You can and should create more functions to help and separate concerns.*
<br/>

```javascript
const input = [1, 2, 3, 4, 5];
// output: [10, 20, 30, 40, 50]
```
<details>
<summary>Possible solution</summary>

```javascript
const output = input.map(x => x * 10);
```
</details>
</br>

```javascript
const input = [1, 2, 3, 4, 5];
// output: 15
```
<details>
<summary>Possible solution</summary>

```javascript
const output = input.reduce((acc, value) => acc + value);
```
</details>
</br>

```javascript
const input = [1, 2, 3, 4, 5];
// output: [2, 4]
```
<details>
<summary>Possible solution</summary>

```javascript
const output = input.filter(value => value % 2);
```
</details>
</br>

```javascript
const input = { a: "potato", b: "tomato", c: "lettuce" };
// output: { potato: "a", tomato: "b", lettuce: "c" }
```
<details>
<summary>Possible solution</summary>

```javascript
const output = Object.keys(input).reduce((acc, key) => ({ ...acc, [input[key]]: key }), {});
```
</details>
</br>

```javascript
const input = { abc: 101, def: 3, ghi: 57, jkl: 222, mno: 100 };
// output: [3, 57, 100]
```
<details>
<summary>Possible solution</summary>

```javascript
const output = Object.keys(input)
                .filter(key => input[key] <= 100)
                .map(key => input[key]);
```
</details>
</br>

```javascript
const input = {
  anderson: { allowed: true, access: "lvl 1" },
  yan: { allowed: false },
  lucas: { allowed: true, access: "lvl 3" },
};
// output: ["anderson has lvl 1 access", "yan is not allowed", "lucas has lvl 3 access"]
```
<details>
<summary>Possible solution</summary>

```javascript
const grantAccess = (name, level) => (`${name} has ${level} access`);
const blockAccess = name => (`${name} is not allowed`);

const output = Object.keys(input)
                 .map(key => (input[key].allowed ? grantAccess(key, input[key].access) : blockAccess(key)));
```
</details>
</br>

```javascript
const input = [
  { framework: "react", message: "is awesome!", note: 10 },
  { framework: "angular", message: "meh", note: 4 },
  { framework: "vue", message: "seems cool...", note: 6 },
  { framework: "rails", message: "best friend!", note: 9 },
  { framework: "sinatra", message: "maybe one day", note: 7 }
];
// output: { react: "is aewsome!", rails: "best friend!" }
```
<details>
<summary>Possible solution</summary>

```javascript
const output = input
                .filter(hash => (hash.note > 7))
                .reduce((acc, hash) => ({ ...acc, [hash.framework]: hash.message }), {});
```
</details>
</br>

```javascript
const input = { item: { category: { name: "Playing Cards", code: 666 }, qty: 10 }, costumer: "Leonidas" }
// output: { item: { category: { name: "War Games", code: 666 }, qty: 10 }, costumer: "Leonidas" }
```
<details>
<summary>Possible solution</summary>

```javascript
const output = { ...input, item: { ...input.item, category: { ...input.item.category, name: "War Games" } } }
```
</details>
