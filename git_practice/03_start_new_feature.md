# 새로운 기능 개발 시작

## Fork 

* https://github.com/lim-dongsun/git_practice

* [repo init 은 readme 파일 참고](./01_readme.md)

## 기능 단위 브랜치 생성

```bash
git branch feature/add-profile
git checkout feature/add-profile
```

### 확인

```bash
git log --graph --all --oneline
```

OR

```bash
git log --graph --simplify-by-decoration --pretty=format:'%d' --all
```

OR

![003](image/003.png)

### Branch 란?

![005](image/005.png)

* Branch : 가지, 분기

* 이해하기 쉽게 생각하면 평행세계
  ![006](image/006.jpg)



## 기능 개발 중 변경사항 저장

```bash
echo "# profile" >> profile.md
git add .
git commit -m "add profile file"
git push origin feature/add-profile
```

## 코드 리뷰, 병합

* 팀원이 올린 PR(Pull Request)을 검토하고 병합 

  ```bash
  git merge feature/add-profile
  ```

  OR
  
  ```bash
  git cherry-pick {branch name or commit id}
  ```

### 🔀 git merge

* 두 브랜치 간의 공통 조상을 기준으로, **한 브랜치를 다른 브랜치에 통째로 합친다**.

  → merge commit 이 생성되며, 이력은 브랜치의 흐름을 유지.

* 프론트엔드와 백엔드를 나누어 작업을 하고, 기능 테스트를 위해 통합

* **서로 작업한 내역이 겹치거나 중복되는 부분**이 하나라도 있다면 **충돌**을 일으키므로 **각자의 영역을 철저하게 분리해서 작업** 필요

#### 예시

```bash
git checkout main
git merge feature/login
```

![007](image/007.png)

### 🍒 git cherry-pick

* 다른 브랜치의 **특정 커밋들만 선택해서 현재 브랜치에 복사하여 적용**

  → 적용한 커밋은 **새로운 해시 값을 가진 커밋**으로 생성 됨

#### 예시

```bash
git checkout main
git cherry-pick abc1234
```

![008](image/008.png)
