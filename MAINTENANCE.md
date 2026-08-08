# 운영 가이드 (제작자용 메모)

이 문서는 방문자용이 아니라, 이 저장소를 관리하는 사람을 위한 참고 메모예요.

## 로컬 구조
- `_posts/` : 매주 기사 (Jekyll 글 형식, 마크다운)
- `assets/episodes/NN-제목/` : 각 화의 정적 이미지
- `demos/NN-제목/` : 각 화의 인터랙티브 HTML 데모 (그대로 정적 파일로 서빙됨)

## 매주 새 글을 올리는 방법
1. `_posts/`에 `YYYY-MM-DD-영문슬러그.md` 형식으로 새 파일을 추가합니다 (파일명 맨 앞 날짜가 중요해요).
2. 상단에 다음과 같은 front matter를 넣습니다.
   ```yaml
   ---
   layout: post
   title: "N화. 제목"
   date: YYYY-MM-DD
   ---
   ```
3. 이미지는 `assets/episodes/NN-제목/`에, 인터랙티브 데모는 `demos/NN-제목/`에 넣고 글에서 절대경로(`/mathisto/assets/...`, `/mathisto/demos/...`)로 링크합니다.
4. `git add . && git commit -m "N화: 제목" && git push` 하면 몇 분 안에 사이트에 반영됩니다.

## 처음 배포 시 설정
GitHub 저장소 **Settings → Pages**에서 Source를 "Deploy from a branch", Branch를 "main" / "/(root)"로 설정합니다.
