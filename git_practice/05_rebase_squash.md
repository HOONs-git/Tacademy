# Conflict 를 줄이려면?

* PR / Merge 전에 원본의 변경 사항 확인
* 내 커밋을 원본의 최신 변경 사항 이후로 이동 (git rebase)

![014](image/014.png)

# 커밋 정리

* PR 전에 커밋 정리 필요

```bash
git rebase -i HEAD~3
git merge --squash feature/add-profile
```

![010](image/010.png)



![011](image/011.png)