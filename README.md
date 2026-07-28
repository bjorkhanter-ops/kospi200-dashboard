# 코스피200 분석 현황 대시보드

`kospi200-analysis` 파이프라인이 생성하는 정적 대시보드 1장을 호스팅한다.

- `index.html` — 자동 생성물. **직접 수정하지 않는다** (다음 발행 때 덮어쓰인다)
- 생성기: `scripts/analysis_dashboard.py` (읽기 전용·재계산 없음)
- 발행: `python scripts/publish_dashboard_pages.py`

## 공개 범위

검색엔진 색인은 `noindex, nofollow` 메타태그와 `robots.txt`로 차단한다.
**색인 차단이지 접근 차단이 아니다** — URL을 아는 사람은 열람할 수 있다.

계좌·잔고·보유 포지션은 담기지 않는다. 발행 스크립트가 매번 계좌 어휘·내부어·
외부 리소스를 검사해 하나라도 걸리면 푸시를 중단한다(fail-closed).
