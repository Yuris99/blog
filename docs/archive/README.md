# 학습 기록 이관

2026-10-12에 다음 원본을 기준으로 자료를 이관했다.

| 원본 | 기준 커밋 | 이관 범위 |
| --- | --- | --- |
| `Yuris99/past-blog` | `e65436978e96e9427b0c30bc6b8b754ccd8c6eb7` | 학습 글 20개, 개인 학습 이미지 31개 |
| `Yuris99/CCS` | `7a6a973e40755ddfb5037f92ba134a9950f32328` | 원본 24개 파일 전부 보존, 그중 내용이 있는 메모 14개를 게시글로 변환 |

## 파일 배치

- `_posts/archive/past-blog/`: 수업 노트. 날짜는 원래 파일명에서 가져왔다.
- `_posts/archive/ccs/`: 개발 메모. 날짜가 없던 원문은 파일의 마지막 Git 커밋 시각을 사용했다. 최초 작성일을 뜻하지 않는다.
- `assets/archive/past-blog/`, `assets/archive/ccs/`: 원본 이미지 37개. 바이너리를 그대로 복사했다.
- `docs/archive/sources/`: 원본 Markdown과 CCS의 전체 파일 스냅샷. 게시용 수정 전 내용이다.
- [manifest.json](manifest.json): 원본 경로·커밋·Git blob SHA와 이관 경로의 대응표.
- [sources/past/LICENSE](sources/past/LICENSE): 원본 past-blog에 포함된 라이선스 고지.

`docs/`는 사이트 빌드에서 제외되어 원문 스냅샷이 별도 게시글로 중복 노출되지 않는다. 빈 React 메모 2개, 원래 CCS README와 C++ 파일은 보존만 하고 게시글로 만들지 않았다.

## 게시용 변경

주제별 고정 주소와 목차를 만들고 상대 목차 링크를 새 주소로 연결했다. 이미지 경로는 이관 위치로 바꾸었으며, 원본 파일명의 오타와 경로 없는 이미지 자리도 정리했다. 원문 본문과 옛 자료의 기술 내용은 최신 설명으로 다시 쓰지 않았다.

Chirpy의 기본 이미지 CDN과 로컬 학습 이미지가 섞이지 않도록 이관 이미지에는 `absolute_url`을 사용한다. 사이트 URL은 기존 CNAME과 같은 `https://blog.yuris.io`로 지정했다. 테마 예제 글과 원본 저장소는 그대로 남긴다.

## 링크 수정 기록

- `_posts/Study/24-2/SWAnalysisNDesign/2024-10-09-3.md`: 빈 이미지 링크를 원문 경로 미기재 안내로 변경
