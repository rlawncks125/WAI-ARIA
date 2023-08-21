## WAI-ARIA를 준수하여 웹 접근성 향상

# 웹 접근성 진단 도구와 스크린더

## 웹 접근성 진단 도구

**Colour Contrast Analyser (CCA) :** https://www.tpgi.com/color-contrast-checker/

- 전경 색과 배경색의 명도 대비를 체크해주는 프로그램
- 현재까지 최신 버전 2.5.0
- 명도 대비는 최소 3:1 이상이 되도록 구현

**KWCAG a11y inspector**

- 컨트롤의 대각선 길이를 측정해주는 프로그램
- **크롬 웹** 스토어에서 설치 가능
- 웹에서의 컨트롤 크기는 대각선 **6mm 이상**으로 구현

**OpenWAX**

- 접근성을 자동으로 진단해주는 프로그램
- **크롬 웹** 스토어에서 설치 가능
- 자동 진단이 정확하지는 않아 수동 진단 병행 필요

**W3C Validation :** https://validator.w3.org/

- 웹 표준을 검사하는 사이트
- 접근성 오류, 특히 마크업 오류 확인 시 많이 사용

## 스크린더

**윈도우 (내장)**
ctrl + win + Enter

**윈도우 (설치형)**

- 센스리더 베이직 6.5
- NVDA Version 2018.4

**MAC (시스템 제공)**

- VoiceOver

**Android (시스템 제공)**

- Talkback
- Voice Assistant

**iOS (시스템 제공)**

- VoiceOver

# 자주 사용하는 aria- 속성

---

**`aria-label`: 요소의 목적이나 기능을 설명하는 짧은 텍스트를 제공합니다. 레이블이 없는 인터랙티브 요소나 그래픽 요소에 유용합니다.
예시: `<button aria-label="검색">🔍</button>`**

\*\*`aria-labelledby`: 다른 요소의 ID를 참조하여 레이블을 제공합니다. 여러 개의 레이블을 합칠 때 유용합니다.

예시: `<h1 id="header">헤더</h1><p id="description">설명</p><div aria-labelledby="header description"></div>`\*\*

\*\*`aria-describedby`: 다른 요소의 ID를 참조하여 보충 설명을 제공합니다.

예시: `<input type="text" id="name" aria-describedby="nameHelp"><div id="nameHelp">당신의 이름을 입력하세요.</div>`\*\*

\*\*`aria-hidden`: 스크린 리더에서 해당 요소를 무시하도록 지정합니다. 시각적으로 표시되지만 접근성 측면에서 중요하지 않은 요소에 사용됩니다.

예시: `<span aria-hidden="true">✓</span>`\*\*

\*\*`aria-live`: 해당 영역의 동적 콘텐츠 업데이트를 스크린 리더가 발견할 수 있도록 지정합니다. 값으로 "polite", "assertive" 또는 "off"를 설정할 수 있습니다.

예시: `<div aria-live="polite">새로운 알림이 있습니다.</div>`\*\*

\*\*`aria-expanded`: 요소가 확장되었는지 축소되었는지를 나타냅니다. `true` 또는 `false` 값을 사용합니다.

예시: `<button aria-expanded="false">메뉴 토글</button>`\*\*

\*\*`aria-haspopup`: 해당 요소가 팝업을 가지고 있는지 여부를 나타냅니다.

예시: `<button aria-haspopup="true">더 보기</button>`\*\*

\*\*`aria-controls`: 한 요소가 다른 요소를 제어하는 관계를 나타냅니다. 대상 요소의 ID를 참조합니다.

예시: `<button aria-controls="menu-panel">메뉴 토글</button><div id="menu-panel"></div>`\*\*
