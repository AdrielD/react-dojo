### Given an input, write a function to return the expected output in each case.

*Avoid using `for` loops. Instead, use `map`, `reduce` or `filter` functions, so no state is mutated.*
<br/>

```javascript
const input = [1, 2, 3, 4, 5]
// output: [10, 20, 30, 40, 50]
```
<details>
<summary>Possible solution</summary>

```javascript
input.map(x => x * 10)
```
</details>
