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

## 演算子

| 演算子 | 説明   |
| ------ | ------ |
| +      | 足し算 |
| -      | 引き算 |
| \*     | 掛け算 |
| /      | 割り算 |
| %      | 余り   |
| \*\*   | 累乗   |
| =      | 代入   |

## String

```javascript
let calculationDescription = 'defaultResult';
```

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#Escape_notation

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

## 型変換

### 文字列を数字に変換

```javascript
parseInt('15');
// 数字の15に型変換される
```
