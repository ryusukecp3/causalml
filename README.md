# causalml
causal ml を試す

## 1. Docker
docker imageをbuildするには以下のコードをrunすればいい。
```
docker build -f docker/Dockerfile --tag causalml .
```
次に以下のコードを実行することでコンテナを作成することができる。(nameは自分で指定する。)
```
docker run -it -p 8888:8888 --name mycausalml causalml/bin/bash
```
その後、以下のコードでjupyterlabを起動できる。
```
cd /work/
jupyter lab
```

コンテナのstatusがupであるのなら以下のコードをrunする。
```
docker exec -it mycausakmk bash
