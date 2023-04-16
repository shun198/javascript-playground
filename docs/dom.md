## DOM って何？

Document Object Model の略称で、Web ページを JavaScript で操作するためのインターフェース

DOM は、Web ページ全体を一つのツリー構造に分割し、それぞれの要素をノードとして表す

DOM ツリーのルートノードは、document オブジェクトで表される
JavaScript の DOM を使用することで、Web ページの要素に対して次のような操作を行うことができる

- HTML 要素の取得、追加、変更、削除
- CSS スタイルの変更
- イベントの追加、削除、制御
- ユーザー入力の取得
- アニメーションやエフェクトの制御
- AJAX を用いた非同期通信

以下は、JavaScript の DOM を使用して、Web ページの要素を操作する例

```html
<!DOCTYPE html>
<html>
  <head>
    <title>DOM Example</title>
  </head>
  <body>
    <h1 id="main-heading">Welcome to my Webpage</h1>
    <p>Here you will find lots of interesting content.</p>
    <button id="change-heading-btn">Change Heading</button>
    <script>
      const mainHeading = document.getElementById('main-heading');
      const changeHeadingBtn = document.getElementById('change-heading-btn');
      changeHeadingBtn.addEventListener('click', function () {
        mainHeading.textContent = 'New Heading';
      });
    </script>
  </body>
</html>
```

上記の例では、getElementById メソッドを使用して、

- main-heading
- change-heading-btn

の要素を取得しています

addEventListener メソッドを使用して、 change-heading-btn ボタンがクリックされたときに、main-heading 要素のテキストコンテンツを変更する関数を登録する DOM を使用することで、Web ページの要素を動的に操作することができる

## DOM における document

Web ページ全体を表すオブジェクトで Web ページの HTML 要素やその他のコンテンツを表すノードのトップレベルノードです

```
console.dir(document);
```

で確認できます
主な document は以下の通りです

| ノード                                     | 説明                                                  |
| ------------------------------------------ | ----------------------------------------------------- |
| document.documentElement                   | ドキュメントのルート要素                              |
| document.head                              | `<head>`要素を表すノード                              |
| document.body                              | `<body>`要素を表すノード                              |
| document.getElementById(id)                | 指定した ID 属性を持つ要素を取得する                  |
| document.getElementsByClassName(className) | 指定したクラス名を持つ要素を取得する                  |
| document.getElementsByTagName(tagName)     | 指定したタグ名を持つ要素を取得する                    |
| document.createElement(tagName)            | 指定したタグ名の新しい要素を作成する                  |
| document.createTextNode(text)              | 指定したテキストを持つ新しいテキストノードを作成する  |
| document.querySelector(selector)           | 指定した CSS セレクターに一致する最初の要素を取得する |
| document.querySelectorAll(selector)        | 指定した CSS セレクターに一致する全ての要素を取得する |

## DOM における window

ブラウザウィンドウ全体を表すグローバルオブジェクトです

window オブジェクトは、ブラウザウィンドウのすべてのコンテンツ、つまり

- DOM
- JavaScript
- CSS
- 画像
- ビデオ

などを管理します

```
console.dir(window)
```

で確認できます

window オブジェクトには、以下のようなプロパティやメソッドがあります。

| プロパティ・オブジェクト               | 説明                                                                                |
| -------------------------------------- | ----------------------------------------------------------------------------------- |
| window.document                        | 現在表示されているドキュメントの document オブジェクトを表す                        |
| window.innerWidth / window.innerHeight | ブラウザウィンドウの内部の幅/高さを表す                                             |
| window.open(url, name, specs, replace) | 新しいブラウザウィンドウを開く                                                      |
| window.close()                         | 現在のブラウザウィンドウを閉じる                                                    |
| window.alert(message)                  | ダイアログボックスを表示してメッセージを表示する                                    |
| window.prompt(message, default)        | ダイアログボックスを表示して入力を促し、入力された値を返す                          |
| window.confirm(message)                | ダイアログボックスを表示して、OK/キャンセルのいずれかを選択させ、選択された値を返す |
| window.location                        | 現在表示されているドキュメントの URL を表すオブジェクト                             |
| window.history                         | ブラウザの履歴を表すオブジェクト                                                    |
| window.navigator                       | ブラウザに関する情報を表すオブジェクト                                              |
| window.setTimeout(func, delay)         | 指定された時間後に関数を 1 回だけ実行する                                           |
| window.setInterval(func, interval)     | 指定された間隔で関数を繰り返し実行する                                              |
