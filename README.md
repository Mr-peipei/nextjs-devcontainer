# Docker環境構築 

## 主要コマンド

### Docker起動コマンド

docker-compose.ymlに書かれているサービスを起動する。
```bash
docker compose up -d
```

-dオプションを付与することでバックグラウンド実行可能。

### Docker停止コマンド

docker-compose.ymlに書かれているサービスを停止する。
```bash
docker compose down
```

### Dockerイメージbuild＋起動コマンド

Dockerfileを編集後に既存のコンテナに反映するには、  
1. イメージの構築
2. コンテナの構築
3. コンテナの起動

が必要。  
Dockerfileを使用すると以下のコマンドでイメージ構築から実施。

```bash
docker compose up --build -d
```

### Dockerコンテナステータス確認コマンド

現在起動しているコンテナの確認。
```bash
docker ps
```

全てのコンテナの一覧を確認。
```bash
docker ps -a
```

###  Dockerイメージ確認コマンド

Dockerfileで作成したイメージの確認。
```bash
docker images
```