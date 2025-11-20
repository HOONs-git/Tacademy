# 버전 관리?

* 어떤 파일이 마지막 파일이지?
  * ex) report_final_final_진짜마지막.docx
* 여러명이 하나의 앱을 개발하면?
  * 수정한 코드를 어떻게 합치지?

> Git은 ‘시간을 되돌릴 수 있는 저장소’입니다.



# Git vs Github

> Git은 개인용 버전관리, GitHub는 협업을 위한 무대

| 항목 | Git            | Github            |
| ---- | -------------- | ----------------- |
| 역할 | 버전 관리 도구 | 협업 플랫폼       |
| 위치 | 내 컴퓨터      | 클라우드          |
| 기능 | commit, branch | PR, Issue, Review |

* 회사에 따라서 Github, Gitlab, Gerrit, bitbucket 등 다양한 솔루션중에서 하나를 사용

# GUI vs CLI

## GUI

* ex) github desktop
  ![002](image/002.png)

## CLI

```shell
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main
```

* GUI 를 사용하지 못하는 환경에서는 → CLI 사용
