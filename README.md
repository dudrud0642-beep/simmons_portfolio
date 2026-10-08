# Simmons Portfolio Renewal

시몬스의 수면 기술과 라이프스타일을 블랙 콘셉트로 재해석한 반응형 웹 리뉴얼 포트폴리오입니다.

## Structure

```text
.
├─ index.html
├─ README.md
├─ docs/
│  ├─ 가이드.md
│  └─ simmons-renewal-proposal.html
└─ assets
   ├─ css/
   │  ├─ base.css         # 변수(색·여백)·기본 스타일·섹션 제목·등장 효과
   │  ├─ layout.css       # 헤더·모바일 메뉴·퀵메뉴·푸터
   │  ├─ sections.css     # 히어로 → 매장까지 섹션별 스타일 (반응형 포함)
   │  ├─ closing.css      # 마지막 브랜드 메시지
   │  └─ popup.css        # 이벤트 팝업 (PC 카드 · 모바일 바텀시트)
   ├─ images/simmons/
   └─ js/main.js
```

## Features

- 반응형 헤더와 모바일 전체 메뉴
- 대형 풀 와이드 제품 및 브랜드 섹션
- 자동 재생·키보드 조작이 가능한 히어로·컬렉션 슬라이드
- 스크롤해도 고정되는 배경 이미지(좋은 밤 기준 섹션)
- 스크롤 리빌 인터랙션과 모션 저감 설정 지원
- 비주얼 아카이브 및 자동 재생 매장 카드 슬라이더
- 진행 막대가 있는 이벤트 팝업(PC 카드 · 모바일 바텀시트, 오늘 하루 보지 않기)과 카카오톡·챗봇 퀵메뉴

## Editing guide

- 페이지 문구와 섹션 순서: `index.html`
- 색상·좌우 여백·섹션 여백: `assets/css/base.css` 상단의 `:root`
- 섹션 제목 6개 크기: `assets/css/base.css`의 `.section-title`
- 섹션별 스타일·반응형: `assets/css/sections.css` (섹션 번호 순서)
- 헤더·퀵메뉴·푸터: `assets/css/layout.css`
- 마지막 브랜드 메시지: `assets/css/closing.css`
- 이벤트 팝업: `assets/css/popup.css` (문구는 `index.html`의 `<aside class="event-popup">`)
- 반응형 기준: `1200px`, `1100px`, `900px`, `600px`
- 슬라이드·메뉴·팝업 동작: `assets/js/main.js` (맨 위 목차 번호로 찾기)
- 제품 및 공간 이미지: `assets/images/simmons/`
- 이미지·글자 크기·여백·움직임 편집 가이드: `docs/가이드.md`
- 리뉴얼 기획안: `docs/simmons-renewal-proposal.html`

HTML은 `header`, `main`의 개별 `section`, 고정 퀵메뉴, `footer` 순서로 구성되어 있습니다. JavaScript는 요소가 존재할 때만 실행되므로 섹션을 제거해도 다른 인터랙션이 중단되지 않습니다.

현재 GNB·본문 CTA·푸터·팝업·퀵메뉴(카카오/챗봇)는 포트폴리오 검토용으로 **어디로도 이동하지 않습니다**. 실제 서비스 연결 시 `index.html`의 `href`를 연결하고 `main.js` 9번(Prototype-only behaviour) 구간을 원하는 동작으로 바꾸면 됩니다.

프로젝트 폴더명은 **`simmons_portfolio`** 입니다. 최종 검토 체크리스트와 기획안은 `docs/simmons-renewal-proposal.html`을 브라우저로 열어 확인하세요.

## Local preview

프로젝트 루트에서 정적 서버를 실행한 뒤 `index.html`을 엽니다.

```bash
npx serve .
```

시몬스를 주제로 제작한 비공식 포트폴리오 리뉴얼 콘셉트입니다.
