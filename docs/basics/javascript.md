## async と defer

HTML の script 要素において、スクリプトファイルをダウンロードするときの挙動を制御するために使用される属性

```index.html
    <script src="assets/scripts/vendor.js" async></script>
    <script src="assets/scripts/app.js" async></script>
```

```index.html
    <script src="assets/scripts/vendor.js" defer></script>
    <script src="assets/scripts/app.js" defer></script>
```

### async

スクリプトファイルのダウンロードを非同期的に行い、HTML のパーシングをブロックしないため、ページの読み込み速度を向上させることができる
しかし、ダウンロードが完了する前に実行されるため、依存関係のあるスクリプトファイルの読み込み順序が保証されない場合がある
たとえば vendor.js より先に app.js のダウンロードが完了されたら vendor.js の方が順番が上でも app.js が先に実行される
また、app.js の処理が vendor.js に依存してたら app.js を実行できなくなってしまう場合がある

### defer

ブラウザはスクリプトファイルを非同期的にダウンロードするが、HTML のパーシングが完了した後にスクリプトファイルを実行する
つまり、スクリプトファイルは HTML の要素が完全にロードされた後に実行されるため、依存関係のあるスクリプトファイルの読み込み順序が保証される
たとえば vendor.js より先に app.js のダウンロードが完了されたとしても、vendor.js の方が順番が上だから vendor.js、app.js の順に実行される
async より実行するのに時間がかかっても app.js の処理が vendor.js に依存してたら vendor.js を実行してから app.js を確実に実行できる
