# 매티스토 (mathisto)

아이들을 위한 수학·물리 코딩 매거진. GitHub Pages(Jekyll)로 호스팅합니다.

## 로컬 구조
- `_posts/` : 매주 기사 (Jekyll 글 형식, 마크다운)
- `assets/episodes/NN-제목/` : 각 화의 정적 이미지
- `demos/NN-제목/` : 각 화의 인터랙티브 HTML 데모 (그대로 정적 파일로 서빙됨)

## 처음 배포하는 방법
1. https://github.com/ssnkoster/mathisto 저장소를 (비어있는 상태로) 만듭니다.
2. 이 폴더에서 아래 명령을 순서대로 실행합니다.

```bash
cd mathisto
git init
git add .
git commit -m "1화: 피보나치와 자연 속 수학"
git branch -M main
git remote add origin https://github.com/ssnkoster/mathisto.git
git push -u origin main
```

3. GitHub 저장소 페이지에서 **Settings → Pages** 로 이동해서
   Source를 "Deploy from a branch", Branch를 "main" / "/(root)" 로 설정하고 저장합니다.
4. 몇 분 후 https://ssnkoster.github.io/mathisto/ 에서 확인할 수 있어요.

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
3. 이미지는 `assets/episodes/NN-제목/`에, 인터랙티브 데모는 `demos/NN-제목/`에 넣고 글에서 상대경로로 링크합니다.
4. `git add . && git commit -m "N화: 제목" && git push` 하면 몇 분 안에 사이트에 반영됩니다.
