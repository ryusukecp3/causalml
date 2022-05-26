# causalml
causal ml を試す

## 1. Docker
docker imageをbuildするには以下のコードをrunすればいい。
```
docker build -f docker/Dockerfile --tag causalml .
```
次に以下のコードを実行することでコンテナを作成することができる。(nameは自分で指定する。)
```
docker run -it -p 8888:8888 --name mycausalml causalml /bin/bash
```
その後、以下のコードでjupyterlabを起動できる。
```
cd /work/
jupyter lab
```

コンテナのstatusがupであるのなら以下のコードをrunする。
```
docker exec -it mycausalml bash
```

mac では上記の方法でできなかった。
以下の方法でできた。
docker imageをbuildするには以下のコードをrunすればいい。
```
docker build -f docker/Dockerfile.mac --tag causalml .
```
次に以下のコードを実行することでコンテナを作成することができる。(nameは自分で指定する。)
```
docker run -it -p 8888:8888 --name mycausalml causalml /bin/bash
```
その後、以下のコードでjupyterlabを起動できる。
```
$ cd /work/
$ git clone https://github.com/uber/causalml.git
$ cd causalml
$ pip install -r requirements.txt
$ pip install causalml
$ cd ../
$ cd git clone 自分の
```
