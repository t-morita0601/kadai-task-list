課題：タスク管理アプリケーション
====

## 画面構成
* タスク一覧: /tasks
* タスク詳細: /tasks/{id}/get
* タスク新規作成: /tasks/create
* タスク編集: /tasks/{id}/update

## ローカル環境構築手順

1. リソース取得  
```
$ git clone https://github.com/t-morita0601/kadai-task-list.git
$ cd kadai-task-list
```

2. Database作成  
```
$ cd shell && ./create-local-mysql-db.sh  
```

3. マイグレーション実施  
```
$ cd ..
$ set _JAVA_OPTIONS="-Dfile.encoding=UTF-8"
$ sbt flywayMigrate
```

4. 起動  
```
$ sbt run
```

5. サイトアクセス  
http://localhost:9000/tasks
