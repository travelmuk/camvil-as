# 캠빌 AS 접수 페이지 정적 배포

이 폴더는 별도 백엔드 서버나 빌드 과정 없이 바로 배포할 수 있는 정적 파일 묶음입니다.

## 배포에 필요한 파일

- `index.html`
- `canopy-as-guide.png`
- `.nojekyll` GitHub Pages용 선택 파일

`as-reception.html`은 기존 파일명으로 접속했을 때 `index.html`로 이동시키는 보조 파일입니다.

## GitHub Pages

1. 새 저장소를 만들거나 기존 저장소에 이 폴더의 파일을 올립니다.
2. GitHub Pages 설정에서 배포 브랜치와 폴더를 선택합니다.
3. 루트에 `index.html`이 보이면 자동으로 첫 화면으로 열립니다.

## Vercel

1. Vercel에서 새 프로젝트를 만들고 이 폴더를 프로젝트 루트로 지정합니다.
2. Framework Preset은 `Other`로 두고 Build Command는 비워둡니다.
3. Output Directory도 비워두거나 `.`으로 설정합니다.

## 구글시트 저장

구글시트 자동 저장을 쓰려면 `google-apps-script.gs`를 Apps Script에 붙여넣고 웹앱으로 배포한 뒤,
발급된 웹앱 URL을 `index.html` 안의 `GOOGLE_SCRIPT_URL` 값에 넣어주세요.
URL이 비어 있으면 제출 데이터는 브라우저 콘솔에만 출력됩니다.
