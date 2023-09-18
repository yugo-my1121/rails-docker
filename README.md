# 環境構築方法

1.ローカルにファイルをgit cloneして持ってくる
https://github.com/yugo-my1121/rails-docker.git

2.以下のコマンドを実行してlocalhost:3000でアプリケーションが 動くようにする。

```
docker-compose up -d

```

3.確認
```
docker-compose ps -a
```
上記のコマンドを実行し下記のようにstatusがUpになっていれば成功
```
[rails-docker] docker-compose ps -a                                                                                                                                                15:42:58  ☁  main ☂ ⚡ ✭
NAME                 IMAGE              COMMAND                                                                                              SERVICE   CREATED          STATUS          PORTS
rails-docker-db-1    postgres:12        "docker-entrypoint.sh postgres"                                                                      db        14 seconds ago   Up 13 seconds   5432/tcp
rails-docker-web-1   rails-docker-web   "bash -c 'rm -f tmp/pids/server.pid && rails db:create && rails db:migrate && rails s -b 0.0.0.0'"   web       13 seconds ago   Up 12 seconds   0.0.0.0:3000->3000/tcp

```
1~3を実施後にhttp://localhost:3000/にブラウザからアクセスする。
