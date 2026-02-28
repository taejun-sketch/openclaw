# MakeTeam Tag Taxonomy (v1)

## 목적

포지션별 프로젝트를 운영하면서도, 동일 이니셔티브/우선순위/고객 단위를 횡단 추적하기 위한 공통 태그 규칙.

## 네이밍 규칙

- 전부 소문자
- `prefix:value` 형식
- 공백 대신 `-` 사용

## 필수 태그

- `initiative:*` (반드시 1개)
  - 예: `initiative:mvp-launch`, `initiative:auth-v1`
- `position:*` (반드시 1개)
  - 예: `position:planning`, `position:development`, `position:design`, `position:marketing`

## 선택 태그

- `priority:*`
  - `priority:p0`, `priority:p1`, `priority:p2`
- `client:*`
  - 예: `client:internal`, `client:acme`
- `surface:*`
  - 예: `surface:web`, `surface:telegram`, `surface:api`
- `risk:*`
  - `risk:low`, `risk:medium`, `risk:high`
- `status:*` (보조 메타, 컬럼과 중복 최소화)
  - 예: `status:blocker`

## 포지션별 프로젝트 운영

프로젝트는 포지션별로 분리:

- Planning
- Development
- Design
- Marketing

각 태스크는 위 프로젝트 중 하나에 속하고, 공통 `initiative:*` 태그로 연결한다.

## 예시

- 프로젝트: Development
- 태스크: 로그인 API 구현
- 태그:
  - `initiative:auth-v1`
  - `position:development`
  - `priority:p0`
  - `surface:api`

## 운영 룰

1. Backlog 생성 시 제목 + `initiative:*` + `position:*`만 필수
2. Backlog -> Todo 전환 시 상세계획/승인 규칙 충족
3. Done 전환 시 결과 증빙 링크를 코멘트에 남김
