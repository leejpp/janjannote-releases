# WORK SUMMARY - 2026-04-30

## 릴리즈 저장소 초기화

- 잔잔노트 Windows 설치 파일 전용 Public GitHub Releases 저장소를 생성했다.
- 저장소 주소: `https://github.com/leejpp/janjannote-releases`
- 소스 코드는 포함하지 않고, 릴리즈 자산과 공개 업데이트 메타데이터만 보관하는 목적임을 README에 명시했다.

## 테스트 릴리즈 업로드

- `v0.2.0` 테스트 릴리즈를 생성했다.
- 업로드한 파일:
  - `JanjanNote-0.2.0-setup.exe`
  - `JanjanNote-0.2.0-setup.exe.blockmap`
  - `latest.yml`
  - `latest.json`
- `latest.json`의 고정 조회 URL:
  - `https://github.com/leejpp/janjannote-releases/releases/latest/download/latest.json`
- 설치 파일 SHA-256:
  - `a08c568730821f3d2094ac91460a7b7eddcef41cb58b0171ed35105c5239ad7b`

## 검증

- GitHub CLI 로그인 토큰을 갱신했다.
- `gh release view v0.2.0 --repo leejpp/janjannote-releases --json url,tagName,assets`로 릴리즈 자산 업로드를 확인했다.
- `curl -L https://github.com/leejpp/janjannote-releases/releases/latest/download/latest.json`로 공개 `latest.json` 다운로드를 확인했다.

## 다음 작업 맥락

- 현재 `v0.2.0` 설치 파일은 업데이트 UI 구현 전 기존 빌드다.
- `theroot`의 업데이트 UI가 포함된 첫 설치 파일은 다음 버전 빌드에서 생성해 이 저장소에 새 릴리즈로 업로드해야 한다.
- Windows 실기기에서 다운로드, 설치, SmartScreen 경고, 기존 설치 위 재설치, 앱 내 업데이트 확인 UI를 검증해야 한다.
