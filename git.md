# アカウント登録
一度登録すれば後は不要
```
 $ git config user.name "<user_name>"
 $ git config user.email "<user_email>"
```

# 新規プロジェクトの作成
```
 $ git init 
 $ git remote add origin https://.... # 発行されたURL
 $ git add . # masterとして作成登録する
 $ git commit -m 'first-commit'
 $ git push origin master

```

# ブランチ
```
 $ git branch # 確認
 $ git checkout -b "<development>" # 作成
 $ git checkout master " チェックアウトのみ
```

# 状態確認とログ
```
 $ git status 
 $ git log
```

# コミットする
ただし、`development`としてコミットする。
```
 $ git add . 
 $ git commit -m 'second-commit'
 $ git push origin deveploment
```

# masterで変更された内容の取得。
conflictに注意する。
```
 $ git pull origin master
```

# 他アカウントのコード取得
```
 $ git clone https://....
```