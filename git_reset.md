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