## docker基本操作

```
imageをdocker hubから取得
docker image pull gihyodocker/echo:latest

コンテナをタグをつけて起動　
ポートフォワーディングでローカルからは9000で接続し、dockerでは8080で受け取る
docker container run -t -p 9000:8080 gihyodocker/echo:latest

curlで接続
curl http://localhost:9000/

自ホストのポートは省略可
docker container run -t -p 8080 gihyodocker/echo:latest

その場合は空いてるポートが自動で設定される
curl http://localhost:32768/
```
