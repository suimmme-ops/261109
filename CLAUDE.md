# 프로젝트 작업 규칙

Vanilla JavaScript + Vite 프로젝트입니다. GitHub에 올린 뒤 Netlify와 연동해 배포합니다.
코드 작업을 시작하기 전에 아래 규칙을 확인하세요.

## 작업 규칙

1. HTML, CSS, JavaScript 코드는 각각 별도 파일로 작성한다.
2. `index.html`은 프로젝트 루트에 두고, 애플리케이션 CSS·JavaScript 파일은 `src` 폴더에 둔다. `vite.config.js` 등 설정 파일은 프로젝트 루트에 둔다.
3. JavaScript는 모듈 방식(`<script type="module" src="/src/main.js">`)으로 연결한다. CSS는 JavaScript 진입 파일(`src/main.js`)에서 `import './style.css'`처럼 import해 Vite 빌드에 포함되게 한다.
4. 외부 JavaScript 라이브러리는 `npm install`로 설치하고 import해서 쓴다. CDN은 사용하지 않는다.
5. 기존 파일과 설정을 먼저 확인하고 필요한 부분만 수정한다.

## 빌드 및 배포

- 개발 서버: `npm run dev`
- 빌드: `npm run build` (출력 폴더: `dist`)
- Netlify 설정
  - Build command: `npm run build`
  - Publish directory: `dist`
