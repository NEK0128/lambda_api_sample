# APIの仕様書をみる
- dockerの起動
```
docker-compose up  serve
```
- dockerを起動した際にhtmlが表示されるのでそれを参照

# モックサーバの立ち上げ
- docsに移動
```bash
cd docs
```
- docker起動
```bash
docker-compose up  prism
```
- 別ウインドウを立ち上げcurlコマンドでcall
  - dockerを起動した際にinfoでuriが表示される
  - &__dynamic=trueを作ることでランダムで値を返してくれる
```bash
curl http://0.0.0.0:4010/users\?id\=0e97a3dc-97e4-6648-a25b-89f4ed7d56ab\&__dynamic\=true
```

# 仕様書をhtmlで作成
```
swagger-codegen generate -i openapi.yaml -l html -o /tmp/swagger-sample
```

# lambda layer
```
zip -r layer.zip python
```

# 参考
https://github.com/wework/speccy
