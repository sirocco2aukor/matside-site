# Matside — matside.com.au

주짓수 온라인 언론사 *Matside*(Matside Media Pty Ltd)의 퍼블릭 사이트 소스.

## 구조

```
public/            배포되는 정적 사이트 (이 디렉터리 전체가 그대로 서빙된다)
  index.html         최신 호 (현재 Vol. 1 No. 2)
  vol-1-no-1/        아카이브
  long-match/        롱폼
  standards/         편집 헌장 (v1.1)
  position/          Outside the Line (KR/EN)
  _headers           보안·캐시 헤더
  robots.txt  sitemap.xml  404.html
legacy/            VentraIP/Apache 시절 .htaccess (배포되지 않음, 기록용)
wrangler.jsonc     Cloudflare Worker 설정
```

## 배포

`main` 브랜치에 푸시하면 Cloudflare Workers Builds가 자동으로 배포한다.

```bash
git add -A
git commit -m "Vol. 1 No. 3"
git push
```

Worker 이름은 `silent-butterfly-db25` (자동 생성된 이름이라 변경 불가).
`api.cloudflare.com`이 세션 네트워크 정책에 막혀 있어 Wrangler CLI 배포는 쓰지 않는다 —
GitHub 푸시가 유일한 배포 경로다.

## 아카이브 원칙

헌장 § 4.1 — 정정은 제자리에서, 삭제하지 않는다.
이 저장소의 커밋 기록이 그 약속의 증거가 된다. 발행된 페이지를 되돌려 지우지 말 것.

## 연락

editor@ · tips@ · corrections@ · standards@ — matside.com.au
