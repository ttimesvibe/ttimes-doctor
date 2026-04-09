# ttimes-doctor

티타임즈 인터뷰 스크립트 교정 & 편집 가이드 도구

## 구조

```
docs/           ← GitHub Pages 배포 (프론트엔드)
  index.html
  assets/
  src/App.jsx   ← 소스 보존
worker/         ← Cloudflare Worker (wrangler deploy)
  index.js      ← 로컬에서 관리
  wrangler.toml
  README.md
```

## 프론트엔드 배포

GitHub Pages: `docs/` 폴더 기준
URL: https://ttimesvibe.github.io/ttimes-doctor/

## Worker 배포

```powershell
cd worker
wrangler deploy
```

배포 후 Cloudflare 대시보드에서 Region 확인 (aws:us-east-1)
