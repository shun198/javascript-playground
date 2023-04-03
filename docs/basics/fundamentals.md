## Variables(変数) & Constant(定数)

### 変数

```javascript
let userName = 'Max';
userName = 'Bob';
```

#### 命名

- camelCase での命名が基本
- 文字列と数字のみ使っていい
- $からはじめてもいい
- \_(アンダースコア)を使ってもいい

```javascript
let userName;
let ageGroup5;
let $kindOfSpecial;
let _internalValue;
```

### 定数

変数と違って一度定義したら変更できない

```javascript
const totalUsers = 15;
```

### 文字列内に変数

```javascript
const name = 'Jim';
const age = 30;
console.log(`${name} is ${age} years old`);
// Jim is 30 years old
```

## 演算子

| 演算子 | 説明                     |
| ------ | ------------------------ |
| +      | 足し算                   |
| -      | 引き算                   |
| \*     | 掛け算                   |
| /      | 割り算                   |
| %      | 余り                     |
| \*\*   | 累乗                     |
| =      | 代入                     |
| ==     | (型に関係なく)値が等しい |
| !=     | (型に関係なく)等しくない |
| ===    | (型も含めて)値が等しい   |
| !==    | (型も含めて)値が等しい   |
| +=     | 加算して代入             |
| -=     | 減算して代入             |
| \*=    | 乗算して代入             |
| /=     | 除算して代入             |
| ++     | インクリメント           |
| --     | デクリメント             |

### == と !=

```javascript
2 == 2;
//true
2 == '2';
//true
3 != 2;
//true
3 != '3';
//false
```

### === と !==

```javascript
2 === 2;
//true
2 === '2';
//false
3 !== 2;
//true
3 !== '3';
//true
```

## 型

### String

```javascript
let food = 'ramen';
```

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#Escape_notation

### Int

```javascript
let age = 25;
```

### Object

```javascript
const logEntry = {
  name: 'John',
  age: 27,
};
// logEntryのnameプロパティにアクセスする
console.log(logEntry.name);
// 'John'
```

### Array

```javascript
let nums = [1, 2, 3];
nums.push(4);
// [1,2,3,4]
nums[2];
// 3
```

## 型変換

```javascript
// 文字列の'15'から数字の15に型変換される
parseInt('15');

// 数字の15から文字列の'15'に変換される
15.toString()
```

## 型の調べ方

```javascript
typeof 15;
//'number'
typeof '15';
//'string'
typeof true;
//'boolean'
typeof [1, 2, 3];
//'object'
```

## 関数

`{}`の後には;(セミコロン)は入れない
function 内で定義した変数は function 内にのみ有効

```javascript
// 関数を定義
function add(num1, num2) {
  const result = num1 + num2;
}

//関数を実行
add(3, 5); // The result is 8
```

### 戻り値の設定

```javascript
function add(num1, num2) {
  const result = num1 + num2;
  // resultを戻り値として指定
  return result;
}
```

## if

```javascript
const num = 12;
if (num % 2 == 0) {
  console.log('2の倍数です');
} else if (num % 3 == 0) {
  console.log('3の倍数です');
} else if (num % 5 == 0) {
  console.log('5の倍数です');
} else {
  console.log('2でも3でも5の倍数でもないです');
}
// 2の倍数です
```

## 三項演算子

```javascript
var age = 26;
age >= 21 ? 'ビール' : 'ジュース';
// "ビール"
```

## switch-case

```javascript
const fruits = 'Papayas';
switch (fruits) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
  case 'Mangoes':
    console.log('Mangoes are $1.79 a pound.');
  case 'Papayas':
    console.log('Papayas are $2.79 a pound.');
}
// "Papayas are $2.79 a pound."
```

## Loop

### for

```javascript
let str = '';

for (let i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// Expected output: "012345678"
```

### for-of

```javascript
const array1 = ['a', 'b', 'c'];

for (const element of array1) {
  console.log(element);
}

// Expected output: "a"
// Expected output: "b"
// Expected output: "c"
```

### for-in

```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

### while

```javascript
let n = 0;

while (n < 3) {
  n++;
}

console.log(n);
// Expected output: 3
```

### do-while

```javascript
let result = '';
let i = 0;

do {
  i = i + 1;
  result = result + i;
} while (i < 5);

console.log(result);
// Expected output: "12345"
```

### break

```javascript
let i = 0;

while (i < 6) {
  if (i === 3) {
    break;
  }
  i = i + 1;
}

console.log(i);
// Expected output: 3
```

### continue

```javascript
let text = '';

for (let i = 0; i < 10; i++) {
  if (i === 3) {
    continue;
  }
  text = text + i;
}

console.log(text);
// Expected output: "012456789"
```

### try-catch

```javascript
try {
  nonExistentFunction();
} catch (error) {
  console.error(error);
  // Expected output: ReferenceError: nonExistentFunction is not defined
  // (Note: the exact output may be browser-dependent)
}
```
