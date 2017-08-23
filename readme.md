## package.jsonをつくる

```
npm init -y
```

## webサーバモジュールをインストールする

```
npm install --save connect
npm install --save serve-static
```
 
## webサーバを立てるコードを書く

server.js

```
var connect = require('connect');
var serveStatic = require('serve-static');
var app = connect();

//静的コンテンツを返せる
app.use(serveStatic(__dirname));

app.listen(8080);
console.log('Server running on 8080');
```

## webサーバを実行する

```
npm start
```
もしくは
```
node server.js
```

## htmlファイルをおく

index.html
```
<h1>hello node server</h1>
```

## webサーバ越しにhtmlを参照する

http://localhost:8080/index.html にアクセスする
