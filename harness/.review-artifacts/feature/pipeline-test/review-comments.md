# 코드리뷰 결과

## 리뷰 대상
- Branch: feature/pipeline-test
- 파일: test.js

---

## 지적 사항

### [CRITICAL] var 사용
`js
var result = a+b; // 위반
`
- 근거: GEN-001, 현대 JS에서 var는 스코프 문제 유발
- 제안: const result = a + b;로 변경

### [MAJOR] 연산자 주변 공백 없음
`js
var result = a+b;
`
- 근거: GEN-001 코드 가독성
- 제안:  + b (공백 추가)

### [MAJOR] 에러 핸들링 없음
`js
function calculate(a, b) {
  // 입력값 검증 없음
`
- 근거: GEN-003 에러 핸들링은 발생 지점에서 처리
- 제안: a, b가 숫자인지 검증하는 로직 추가

### [MINOR] console.log 사이드이펙트
`js
console.log(result);
`
- 근거: GEN-001 단일 책임
- 제안: 함수는 값만 반환하고, 출력은 호출자에서 담당

---

## 총평
3개의 의도적 위반 사항이 모두 정확히 감지됨. 파이프라인 정상 동작 확인.
