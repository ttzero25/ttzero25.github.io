# ttzero25.github.io

teo (ttzero25) 보안 포트폴리오 — 오픈소스 취약점 리서치 · CTF.

빌드 도구 없는 정적 사이트. GitHub Pages에서 그대로 서빙됩니다.

## 구조

```
index.html          # 메인 (whoami / education / experience / CVE / hall of fame / projects / speaker / etc)
blog.html           # 블로그 (마크다운 글 목록 + 뷰어)
cv.html             # CV (준비 중 페이지)
assets/site.css     # blog·cv 공용 스타일
posts/
  posts.json        # 글 목록 (최신순 자동 정렬)
  *.md              # 글 본문 (마크다운)
```

## 새 블로그 글 쓰기

1. `posts/<slug>.md` 파일을 만들고 마크다운으로 작성
2. `posts/posts.json`에 항목 추가:
   ```json
   { "slug": "<slug>", "title": "보여줄 제목", "date": "YYYY-MM-DD" }
   ```
3. `git push` — 목록에 최신순으로 나타납니다.

## 로컬 미리보기

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## 배포 (GitHub Pages)

1. 저장소를 `ttzero25/ttzero25.github.io` 이름으로 생성 후 push
2. Settings → Pages → Source: `main` 브랜치 `/ (root)`
3. `https://ttzero25.github.io` 에서 공개

## 참고

- 폰트: Google Fonts (Inter, JetBrains Mono)
- 마크다운 렌더링: marked (CDN)
- 라이트/다크 토글 (localStorage 저장)
