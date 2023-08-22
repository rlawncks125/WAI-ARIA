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

**윈도우 ( 시스템 제공 )**
ctrl + win + Enter

**MAC (시스템 제공)**

- VoiceOver

**Android (시스템 제공)**

- Talkback
- Voice Assistant

**iOS (시스템 제공)**

- VoiceOver

# 시멘틱 태그가 아닌 태그 사용시 접근성 고려해야함

- div
- span
- p
- li
  ... 등

# 자주 사용하는 aria- 속성

---

`aria-label`: 요소의 **목적이나 기능을 설명**하는 짧은 텍스트를 제공합니다. 레이블이 없는 인터랙티브 요소나 그래픽 요소에 유용합니다.

예시:

```
<button aria-label="검색">🔍</button>
```

`aria-labelledby`: 다른 요소의 ID를 참조하여 레이블을 제공합니다. 여러 개의 레이블을 합칠 때 유용합니다.

예시:

```
// div 포커스시
// 네레이터 : 헤더 설명
<div aria-labelledby="header description" tabindex="0">0</div>
<p id="header">헤더</p>
<p id="description">설명</p>
```

`aria-describedby`: 다른 요소의 ID를 참조하여 보충 설명을 제공합니다.

예시:

```
// input 포커스시
// 네레이터 : 이름 편집 한글만 허용 합니다.
<label for="input_name">이름 :</label>
<input type="text" id="input_name" aria-describedby="name_tip" />
<p id="name_tip" role="tooltip">한글 만 허용합니다.</p>
```

`aria-hidden`: 스크린 리더에서 해당 요소를 무시하도록 지정합니다. 시각적으로 표시되지만 접근성 측면에서 중요하지 않은 요소에 사용됩니다.

예시:

```
<span aria-hidden="true">나무시해</span>
```

`aria-live`: 해당 영역의 동적 콘텐츠 업데이트를 스크린 리더가 발견할 수 있도록 지정합니다. 값으로 "polite", "assertive" 또는 "off"를 설정할 수 있습니다.

예시:

```
<div aria-live="polite">새로운 알림이 있습니다.</div>
```

`aria-expanded`: 요소가 확장되었는지 축소되었는지를 나타냅니다. `true` 또는 `false` 값을 사용합니다.

예시:

```
<button aria-expanded="false">메뉴 토글</button>
```

`aria-haspopup`:해당 요소가 하위메뉴를 포함하고 있다(팝업될 수 있다)는 정보를 제공함

예시:

```
<button aria-haspopup="true">더 보기</button>
```

`aria-controls`: 선택한 요소에 영향을 받는 하위 요소가 현재 포커스 한 라인과 떨어져 있을 경우 스크린리더 사용자가 하위 요소가 열린 위치를 파악하기 어려우므로 관련된 하위 요소로 바로 이동할 수 있도록 해 주는 역할을 합니다. Tab 역시 특정 tab을 선택한 경우 tab 패널이 시작되는 부분으로 바로 이동할 수 있도록 aria-controls를 포함할 수 있습니다.

예시:

```
<button aria-controls="menu-panel" aria-haspopup="true">메뉴 토글</button>
  <div>나떨어져</div>
  <div>나떨어져</div>
  ...
  <ul id="menu-panel" tabindex="0">
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
  </ul>
```
