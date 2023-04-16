## アロー関数

```javascript
const add = (a, b) => a + b;
```

## rest 演算子

関数の引数で使用される演算子で、可変長の引数リストを 1 つの配列にまとめることができる
Python の\*に相当する

```javascript
function sum(...numbers) {
  let total = 0;
  for (let number of numbers) {
    total += number;
  }
  return total;
}

console.log(sum(1, 2, 3)); // 6
console.log(sum(4, 5, 6, 7)); // 22
```
