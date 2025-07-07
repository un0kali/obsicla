# obsicla


:root {
/* Everforest Dark Palette (from everforest-dark.json) /
--everforest-bg-hard: #272e33; / A bit darker for main components /
--everforest-bg-medium: #2d353b; / Main background /
--everforest-bg-soft: #3d484d; / Lighter background for elements */
--everforest-bg-selection: #475258;
--everforest-border: #4f585e;
--everforest-fg: #d3c6aa;
--everforest-fg-alt: #9aa79d;
--everforest-fg-grey: #859289;

--everforest-red: #e67e80;
--everforest-orange: #e69875;
--everforest-yellow: #dbbc7f;
--everforest-green: #a7c080;
--everforest-aqua: #83c092;
--everforest-blue: #7fbbb3;
--everforest-purple: #d699b6;
}

/* ===== Scrollbar Styling ===== */
::-webkit-scrollbar {
width: 10px;
height: 10px;
}
::-webkit-scrollbar-track {
background: var(--everforest-bg-medium);
}
::-webkit-scrollbar-thumb {
background-color: var(--everforest-bg-selection);
border-radius: 10px;
border: 2px solid var(--everforest-bg-medium);
}
::-webkit-scrollbar-thumb:hover {
background-color: var(--everforest-border);
}

/* 1. 전역 스타일: 기본 배경 및 텍스트 색상 */
body, main {
background-color: var(--everforest-bg-medium) !important;
color: var(--everforest-fg) !important;
}

/* 2. 시작 화면 및 헤더 /
/ "Claude와 함께..." 시작 메시지 */
.font-display, .text-text-200, .text-text-500, .text-text-300, .text-text-400 {
color: var(--everforest-fg) !important;
}

/* Claude 로고 (Sonnet, Opus 등) */
.claude-logo-model-selector {
color: var(--everforest-fg) !important;
}

/* 상단 헤더 */
header {
background-color: var(--everforest-bg-medium) !important;
}

/* 3. 프롬프트 입력창 /
/ 입력창 컨테이너 /
div[class="bg-bg-000"][class*="border-border-300"][class*="rounded-2xl"] {
background-color: var(--everforest-bg-hard) !important;
border: 1px solid var(--everforest-border) !important;
box-shadow: none !important;
}
div[class*="bg-bg-000"][class*="border-border-300"][class*="rounded-2xl"]:focus-within {
border-color: var(--everforest-green) !important;
}

/* 입력 중인 텍스트 /
.ProseMirror {
color: var(--everforest-fg) !important;
}
/ 입력창 플레이스홀더 텍스트 */
.ProseMirror p.is-editor-empty:first-child::before {
color: var(--everforest-fg-grey) !important;
}

/* 4. 각종 버튼 /
/ 전송 버튼 */
button[aria-label="메시지 보내기"], button[data-testid="send-button"] {
background-color: var(--everforest-green) !important;
color: var(--everforest-bg-hard) !important;
}
button[aria-label="메시지 보내기"]:hover, button[data-testid="send-button"]:hover {
filter: brightness(1.1);
}

/* 첨부파일(+) 및 도구 버튼 */
button[data-testid="input-menu-plus"],
button[data-testid="input-menu-tools"] {
background-color: var(--everforest-bg-soft) !important;
border: 1px solid var(--everforest-border) !important;
color: var(--everforest-fg) !important;
}
button[data-testid="input-menu-plus"]:hover,
button[data-testid="input-menu-tools"]:hover {
background-color: var(--everforest-bg-selection) !important;
}

/* 모델 선택 버튼 (Sonnet 4 등) */
button[data-testid="model-selector-dropdown"] {
border-color: transparent !important;
color: var(--everforest-fg) !important;
}
button[data-testid="model-selector-dropdown"]:hover {
background-color: var(--everforest-bg-soft) !important;
}

/* 추천 프롬프트 카테고리 버튼 */
button[role="tab"] {
background-color: var(--everforest-bg-soft) !important;
border: 1px solid var(--everforest-border) !important;
color: var(--everforest-fg) !important;
}
button[role="tab"][aria-selected="true"] {
border-color: var(--everforest-green) !important;
}
button[role="tab"]:hover {
background-color: var(--everforest-bg-selection) !important;
border-color: var(--everforest-green) !important;
}

/* 5. 대화 내용 (채팅 기록) /
/ 사용자 메시지 컨테이너 /
div[class^="group"][class="bg-bg-300"] {
background-color: var(--everforest-bg-hard) !important;
border: 1px solid var(--everforest-border) !important;
border-radius: 12px;
padding: 10px;
}

/* Claude 답변 컨테이너 (기본 답변) /
div[class="font-claude-message"] {
background-color: transparent !important;
}

/* 질문/답변의 배경이 되는 컨테이너 색상 조정 (기존) /
div[class="bg-bg-100"] {
background-color: var(--everforest-bg-soft) !important;
border-radius: 8px;
padding: 8px;
}
div[class*="bg-bg-000"] {
background-color: transparent !important;
}

/* 대화 텍스트 /
.ProseMirror-claude-renderer p,
.ProseMirror-claude-renderer li,
p.whitespace-pre-wrap { / 사용자 메시지 텍스트 */
color: var(--everforest-fg) !important;
}

/* 링크 텍스트 */
.ProseMirror-claude-renderer a {
color: var(--everforest-green) !important;
text-decoration: underline;
}

/* 6. 코드 블록 /
pre, [class="CodeBlock-codeContainer"] {
background-color: var(--everforest-bg-hard) !important;
border-radius: 8px !important;
border: 1px solid var(--everforest-bg-selection) !important;
}
pre code, .token-line {
background: transparent !important;
color: var(--everforest-fg) !important;
}

/* 7. 아이콘 색상 /
svg[fill="currentColor"],
svg[class="text-text-"] {
color: var(--everforest-fg) !important;
}

/* 8. 도구 사용 및 검색 결과 (Search Mode) /
/ 도구 사용 전체 컨테이너 /
div[class="border-border-300"][class*="min-h-"][class*="hover:bg-bg-000"] {
background-color: var(--everforest-bg-hard) !important;
border: 1px solid var(--everforest-border) !important;
border-radius: 8px;
}

/* 도구 사용 제목 (e.g., "CSS selector ... 검색 중") /
button.group/row div[class="text-left"] {
color: var(--everforest-fg) !important;
}
button.group/row:hover div[class*="text-left"] {
color: var(--everforest-fg) !important;
}

/* 도구 사용 로딩 아이콘 및 시간 */
button.group/row p, button.group/row svg {
color: var(--everforest-fg-grey) !important;
opacity: 1 !important;
}

/* 검색 결과 펼쳤을 때 컨테이너 /
div[class="overflow-y-auto"][class*="!max-h-"] {
background-color: var(--everforest-bg-hard) !important;
}

/* 검색 결과 각 항목 버튼 /
div[class="overflow-y-auto"] button[disabled] {
transition: background-color 0.2s ease-in-out;
}
div[class*="overflow-y-auto"] button[disabled]:hover {
background-color: var(--everforest-bg-selection) !important;
}

/* 검색 결과 제목 /
div[class="overflow-y-auto"] p[class*="text-text-000"] {
color: var(--everforest-aqua) !important;
}

/* 검색 결과 출처(도메인) /
div[class="overflow-y-auto"] p[class*="text-text-500"] {
color: var(--everforest-fg-grey) !important;
}

/* 9. 사이드바 */
nav[aria-label="사이드바"] {
background-color: var(--everforest-bg-soft) !important;
border-right: 1px solid var(--everforest-border) !important;
}

/* 사이드바 내부 텍스트 및 아이콘 */
nav[aria-label="사이드바"] a,
nav[aria-label="사이드바"] button,
nav[aria-label="사이드바"] h3,
nav[aria-label="사이드바"] span,
nav[aria-label="사이드바"] svg {
color: var(--everforest-fg-alt) !important;
transition: color 0.2s ease-in-out;
}

/* 사이드바 호버 및 활성 상태 */
nav[aria-label="사이드바"] a:hover,
nav[aria-label="사이드바"] button:hover {
background-color: var(--everforest-bg-selection) !important;
}
nav[aria-label="사이드바"] a:hover span,
nav[aria-label="사이드바"] button:hover span,
nav[aria-label="사이드바"] a:hover svg,
nav[aria-label="사이드바"] button:hover svg {
color: var(--everforest-fg) !important;
}

/* 새 채팅 버튼 /
nav[aria-label="사이드바"] a[aria-label="새 채팅"] div[class="bg-accent-main-000"] {
background-color: var(--everforest-green) !important;
}
nav[aria-label="사이드바"] a[aria-label="새 채팅"] div[class*="text-accent-main-100"] {
color: var(--everforest-green) !important;
}

/* 10. 기타 UI 요소 /
/ 알림 (토스트) */
div[role="status"] > ol > li {
background-color: var(--everforest-bg-hard) !important;
border: 1px solid var(--everforest-border) !important;
color: var(--everforest-fg) !important;
}

/* 드롭다운 메뉴 (모델 선택 등) */
div[role="menu"] {
background-color: var(--everforest-bg-hard) !important;
border: 1px solid var(--everforest-border) !important;
}
div[role="menuitem"] {
color: var(--everforest-fg-alt) !important;
}
div[role="menuitem"]:hover {
background-color: var(--everforest-bg-selection) !important;
color: var(--everforest-fg) !important;
}

/* 사용자 메뉴 /
button[data-testid="user-menu-button"] div[class="bg-bg-400"] {
background-color: var(--everforest-bg-selection) !important;
}
button[data-testid="user-menu-button"]:hover {
background-color: var(--everforest-bg-hard) !important;
}
span[class*="text-text-300"] {
color: var(--everforest-fg-grey) !important;
}
