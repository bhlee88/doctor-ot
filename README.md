# 닥터 OT 웹앱 1차 버전

기능: 이메일 로그인, 병원 구성원 확인, OT 분 단위 입력, 본인 기록 수정/삭제, 월별 실시간 집계.

## 현재 조건
- Firebase 프로젝트 `doctor-ot` 사용
- Firestore `hospitals/main/members/{UID}` 문서에 `name`(string), `role`(string), `active`(boolean=true) 필요
- Firestore 규칙 탭에 `firestore.rules` 내용을 게시해야 앱이 동작합니다. **기존 전체 차단 규칙을 그대로 두면 앱에서 저장할 수 없습니다.**
- 앱은 아직 배포되지 않았습니다. Firebase Hosting 또는 다른 HTTPS 정적 호스팅에 `index.html`, `app.js`, `manifest.webmanifest`, `icon.svg`, `sw.js`를 올려야 합니다.
- Firebase Hosting의 일반적인 CLI 배포는 개발환경이 필요합니다. 스마트폰만 사용할 경우 GitHub 웹사이트로 파일을 업로드하고 GitHub Actions를 통한 Firebase Hosting 배포를 별도 구성하는 방법을 권장합니다. GitHub Secrets에는 서비스 계정 키를 넣지 않고, Firebase의 공식 GitHub 통합 절차 또는 최소권한 인증을 사용하세요.
- 관리자 초대코드/가입 승인 및 관리자 타인 기록 수정 기능은 아직 미구현입니다. 회원 문서는 Firebase 콘솔에서만 추가 가능합니다.
- 이 코드는 실행/배포 테스트를 마치지 않은 초기 버전입니다. 실사용 전에 테스트 계정으로 보안 규칙과 데이터 분리를 검증하세요.
