# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트

박태빈(루덴스페이스)의 한 페이지짜리 소개 웹사이트다. 빌드, 패키지, 테스트가 없는 정적 사이트이고 파일은 `index.html`과 `style.css` 두 개뿐이다. 사용자는 코딩을 처음 배우는 초보자다. 설명은 쉬운 한국어로 하고, 코드에는 각 부분을 설명하는 짧은 한글 주석을 단다.

## 지켜야 할 제약 (처음 요청에서 정한 것)

- 파일은 `index.html`, `style.css` 두 개만 쓴다.
- JavaScript, 외부 라이브러리, 이미지, 복잡한 애니메이션은 쓰지 않는다.
- 색은 배경 `#0a0a0a`, 글씨 `#e0e0e0`, 포인트 `#00e5ff`. `style.css` 맨 위 `:root` 변수에 모여 있다.
- 휴대폰에서 깨지지 않아야 한다. 좁은 화면 규칙은 `style.css` 맨 아래 `@media (max-width: 640px)`에 있다.
- 사용자가 "index.html만" 또는 "style.css만"이라고 하면 다른 파일은 건드리지 않는다.

## 구조

- `index.html`: 위에서 아래로 이름과 한 줄 소개(`.hero`) → 자기소개 → 관심 분야 카드 3개(`.cards`) → 연락처(`.contact`) → `.footer`. 각 영역은 `.section`이다.
- `style.css`: 섹션 사이 간격은 `.section`의 `padding-top: 80px`으로 만든다(구분선 없음). 카드는 평소 회색 테두리이고 마우스를 올리면 시안색 테두리가 된다.

## 미리보기

앱의 파일 목록에서 `index.html`을 클릭해 여는 간이 미리보기는 `style.css`를 불러오지 않아 디자인이 빠져 보인다. 확인할 때는 이 폴더를 로컬 서버로 띄워 `http://localhost:포트/`로 열거나, 탐색기에서 `index.html`을 더블클릭해 평소 브라우저로 연다.

## 배포

- 깃허브 공개 저장소 `taebimbag-boop/taebimbag-boop.github.io`와 연결되어 있다. 이름이 `아이디.github.io`라 GitHub Pages가 자동으로 켜져 있고, `main` 갈래의 맨 위 폴더(`/`)가 https://taebimbag-boop.github.io 로 공개된다.
- `main`에 푸시하면 1~2분 뒤 웹사이트에 반영된다. 이 폴더에 넣는 파일은 이 `CLAUDE.md`까지 모두 인터넷에 공개된다.
- 커밋과 푸시는 할 때마다 사용자에게 먼저 묻고, 허락을 받은 뒤에만 한다.

## 개인정보

공개 저장소이자 공개 웹사이트다.

- 페이지의 이메일은 일부러 예시 주소 `tb@example.com`으로 둔다. 실제 이메일이나 전화번호를 넣지 않는다.
- 이 폴더의 Git은 로컬 설정으로 깃허브 대체 이메일(`...@users.noreply.github.com`)로 커밋한다. 실제 이메일로 바꾸지 않는다.
