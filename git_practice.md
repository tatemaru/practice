## git revert

単一コミットを取り消し

```
$ git revert <commit id>
```

複数の場合は下記のコマンドを複数回実行してからgit commitを実行する

```
$ git revert -n <commit id>
```

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

