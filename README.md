# Carrier Setup V6

## 핵심 변경
- 템플릿을 Firestore 공용 저장소로 이전
- 여러 PC와 사용자에게 같은 템플릿 실시간 표시
- 템플릿 수정 즉시 자동 저장
- 새 프로젝트 생성 시 Firestore 최신 템플릿 적용
- 그룹명/설명/그룹 순서 저장
- 항목명/필수·선택/항목 순서 저장
- 공용 템플릿 항목·그룹 추가 및 삭제
- admin 계정만 템플릿 수정, 일반 계정은 조회만 가능
- 최초 admin 로그인 시 기존 기본 템플릿을 자동 생성
- 기존 프로젝트 데이터는 유지
- 공용 템플릿 항목을 삭제해도 기존 프로젝트 체크항목은 유지

## 적용 방법
1. GitHub의 `index.html`을 V6 파일로 교체하고 Commit
2. Firebase → Firestore Database → 규칙에서 `firestore.rules` 내용으로 전체 교체 후 게시
3. GitHub Pages 배포 후 `Ctrl + F5`
4. admin 계정으로 템플릿 관리 화면 접속
5. 최초 1회 기본 템플릿이 Firestore에 자동 등록되는지 확인

## Firestore 컬렉션
- `scopeTemplates/{scopeKey}`
- `scopeTemplates/{scopeKey}/items/{itemId}`
- `carriers/{projectId}`
- `carriers/{projectId}/checklistItems/{itemId}`
