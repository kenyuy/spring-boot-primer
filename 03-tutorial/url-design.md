# URL設計

データベース定義に続いて URL 設計を行いましょう。

画面と機能から必要な URL を割り出していきます。

|URL|Method|ContentType|目的|
|:---:|:---:|:---:|:---:|
|/|GET|HTML|TOP 画面|
|/create|GET|HTML|メンバー追加 画面|
|/create|POST|HTML|メンバー追加 実行|
|/api/members|GET|JSON|すべてのメンバーを返す|
|/api/members/{words}|GET|JSON|words でメンバーを検索|

下の2つの ```/api/〜``` は、Ajax 用で JSON をレスポンスします。

前章で説明したように、コントローラークラスは HTTP リクエストと Java のメソッドを紐づける働きをするのでしたね。つまりURL 設計を作成しておけば、その設計に合わせてコントローラーを書き始めることができるということです。

データベース定義と URL 設計があれば、だいたいの開発規模やアプリケーションの大枠をつかむことができます。