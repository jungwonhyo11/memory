# 나의 데이터 보관 저장소

이 저장소는 개인 데이터, 도구 산출물을 자동으로 백업동기화합니다.

## 폴더 구조

- harness/ — mafia-codereview-harness 파이프라인 산출물
  - docs/ — code-convention.yaml, adr.yaml
  - .review-artifacts/ — 브랜치별 리뷰 산출물

## 동기화 방법
sync-to-memory.ps1 스크립트를 실행하면 자동 백업됩니다.
