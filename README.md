# Carrier Setup STEP 2

1. Firebase Console > Firestore > 규칙에서 `firestore.rules` 전체 내용을 붙여넣고 게시합니다.
2. `index.html`을 GitHub 저장소에 올리고 GitHub Pages를 켭니다.
3. Firebase Console > Authentication > 설정 > 승인된 도메인에 `사용자명.github.io`를 추가합니다.
4. Google 로그인 후 사용합니다. `allowedUsers`에 있고 `active: true`인 계정만 접근됩니다.

포함 기능: 배송사 추가/삭제, 100개 내외 체크리스트 자동 생성, 담당자/상태, 자동 저장, 실시간 공동 편집, 진행률, OneDrive 링크.
