## git revert
## ローカルの状態（push前）
単一コミットを取り消し

```
$ git revert <commit id>
```

複数の場合は下記のコマンドを複数回実行してからgit commitを実行する

```
$ git revert -n <commit id>
```

## リモートの状態（push後）

pushした後の状態を取り消す場合はresetでも可能だが可能ならrevertで対応する。

```
$ git revert HEAD
```

このコマンドを実行すると、過去のコミットを打ち消す、新しいコミットができるので、

```
$ git push origin HEAD
```

でpushして完了

## git reset

push, commit, add 全て取り消す

```
$ git reset --hard HEAD^
```

ローカルの変更のみを残してpushを取り消す場合

```
$ git soft --hard HEAD^
```

何事もなかったかのようにpushして完了

```
$ git push -f origin HEAD
```

