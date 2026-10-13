---
title: GitHub API 정리
categories:
- Development
- GIthub
tags:
- github
date: 2021-07-20 18:35:24 +0900
permalink: /notes/github/api-notes/
math: true
archive_source: Yuris99/CCS
archive_source_path: GIthub/Gihub Docs.md
archive_source_commit: 7a6a973e40755ddfb5037f92ba134a9950f32328
---

# Github Docs
프로젝트를 진행할 때 필요한 API를 찾아보면서 정리한 깃허브 API

- Repositories
  - Get a Repository


Repository Content 접근방법
  - https://api.github.com/repos/{user}/{repo}/contents/{path}//download_url
  - download_url이 null이면 디렉토리, 아니면 파일

---

원문: [Yuris99/CCS](https://github.com/Yuris99/CCS/blob/7a6a973e40755ddfb5037f92ba134a9950f32328/GIthub/Gihub%20Docs.md) · [전체 학습 기록]({{ '/study/' | relative_url }})
