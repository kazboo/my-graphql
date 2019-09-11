# my-graphql

graphql test

## Setup

warを生成する

```sh
# to build/libs
$ gradle build
```

Tomcatのwebapps配下に配置、Tomcat起動

## Usage

* リクエスト(POST)
  ```graphql
  query { hello }
  ```

* レスポンス(JSON)
  ```json
  {
    "data": {
        "hello": "world"
    }
  }
  ```

* クライアントツール
  + Insomnia
  + Postman


## 備考

* [(参考)graphql-java-kickstart](https://www.graphql-java-kickstart.com/servlet/getting-started/#create-a-servlet-class)
    + サンプルコードそのままだとTomcat開始時に「サーブレットマッピング中に無効な <url-pattern> 」でデプロイ失敗する
    + `{"graphql/*"}`を`{"/graphql"}`に変更する必要がある