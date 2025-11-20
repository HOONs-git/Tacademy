# 충돌(conflict) 해결

* 두 명이 같은 파일을 수정함

```bash
git merge main
```

OR

```
git cherry-pick {branch name or commit id}
```

* conflict 표시 확인(`<<<<<<<`, `=======`, `>>>>>>>`)

![009](image/009.png)

* merge/cherry-pick 중단

```bash
git merge --abort 
```

OR

```bash
git cherry-pick --abort
```

* 상태 확인

```bash
git status
```

