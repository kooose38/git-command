コマンド集

### ファイルの出力
```
$ cat file
$ cat -b file
```
### 上下逆で表示する
```
$ tac file
```

### 行番号を府って表示する
```
$ nl file
```

### バイナリで表示
```
$ od file
```

### エンコード、デコードする
```
$ base64 file 
$ base64 --decode file
$ bse32 file 
$ b2sum file
```
### 一部を出力する
```
$ head -n 10 file # 最初の10行を表示するオプション
$ tail -n 10 -f file001 file002 | grep error # それぞれのファイルから"error"の文字列を取得する
```

## 書式設定

### テキストを折りかえして表示する
```
$ fmt file
$ fold file
``` 

### 印刷要にヘッダーとフッターを追記する
```
$ pr file 
```

## ファイルの要約
### 行数の取得
```
$ wc -l file 
$ grep -o string file | wc -l # "string"の文字列が南海出現しているか取得する
```
## キャラクター操作
### トリムする
```
$ echo 123 | tr 321 654 # 123 -> 654に変換
$ tr -d '\r' < file001 > file002 #file001の改行を削除してfile002に出力する
```

## ファイルリスト表示

```
$ ls -la --color=no 
$ dir 
$ vdir 
```

## 複製
- `-a`で構造、属性をそのままコピー
- `-b`でバックアップ
- `-f`で上書き
- `-n`で上書きをしない

```
$ cp file001 file002
```

```
$ install -o <user> -g <group> file /tmp/ # group,userを指定してファイルを/tmp配下にコピー
```
### ファイルの移動
```
$ mv file001 file002 # file001 -> file002 
```
### 削除する
```
$ rm file 
$ rm -rf ./dir
$ alias rm="mv --target-directory=$HOME/.Trash" #削除時にバックアップをとる設定
```

### シンボリックリンクの作成
```
$ ln -s filename linkname # filenameをlinknameの別ファイルと共有する
```

### フォルダの作成
```
$ mkdir dir 
$ mkdir -m 777 dir1 #パーミッションを指定
$ mkdir -p /dir2/dir3  #２階層以上を作成
```
### ブロックの作成
```
$ mknod block
```
## 属性の変更
パーミッション操作のため`root`で行うのが良い。
```
$ chown user:group rootfile
$ chown +1000.+1000 rootfile
$ chown user. userfile
```

### ファイルの作成
```
$ touch file
$ chmod 777 file # パーミッションの変更 
```





