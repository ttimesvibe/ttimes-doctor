# ttimes-doctor Worker

## 배포 방법

```powershell
cd C:\Users\Hong4137\ttimes-doctor\worker
wrangler deploy
```

## 배포 후 체크리스트

1. Cloudflare 대시보드 → Workers & Pages → ttimes-doctor → Settings → Runtime → Placement
2. Region이 `aws:us-east-1`로 되어있는지 확인 (없으면 수동 설정)
3. `[placement]`를 wrangler.toml에 추가하면 deploy시 리셋되므로 절대 추가 금지

## Secrets

- `OPENAI_API_KEY` — `wrangler secret put OPENAI_API_KEY`
- `GEMINI_API_KEY` — `wrangler secret put GEMINI_API_KEY`

## KV

- Binding: `SESSIONS`
- Namespace ID: `b91de13be69045e59941b1ff000ffa0a`
