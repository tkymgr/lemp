# LEMPスケルトン

## 起動手順

### 作業フォルダを作成する
```
$ mkdir lemp
$ cd lemp
```

### Githubから展開
``` 
$ git clone git@github.com:tkymgr/lemp.git .
```

### docker用の環境ファイルを作成
```
cp env_default .env
```
コピー後に適宜変更する感じ

### ワークフォルダーを作成する
```
$ mkdir .data logs app
```
環境ファイルに従ってフォルダーも変える感じ

### dockerイメージの作成
```
$ docker-compose build
```

### Let's Enjoy!!
```
$ docker-compose up -d
```

