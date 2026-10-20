# ✅ URL2QR 작업 목록 (Task List)

본 문서는 URL2QR 웹사이트의 전체 요구사항 및 추가 개선 작업의 진행 현황과 구현 상태를 추적하는 체크리스트입니다.

---

## 📌 기능별 작업 진행 현황

| 번호 | 작업 항목 | 상태 | 관련 파일 | 세부 내용 |
| :--: | :--- | :---: | :--- | :--- |
| **01** | 상단 좌측 로고 배치 | **완료 (100%)** | [index.html](file:///c:/Users/SON/바이브코딩/프로젝트04/index.html)<br>[style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | `img/logo.png` 로고를 좌측 상단 헤더에 배치, 클릭 시 초기 화면 리셋 기능 구현 |
| **02** | 중앙 심플 URL 입력창 구현 | **완료 (100%)** | [index.html](file:///c:/Users/SON/바이브코딩/프로젝트04/index.html)<br>[style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | 화면 중앙에 프로스티드 글래스모피즘 입력 바, 링크 아이콘, 지우기 버튼 및 [생성하기] 버튼 배치 |
| **03** | 입력창 하단 이동 & QR 중앙 생성 애니메이션 | **완료 (100%)** | [style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css)<br>[script.js](file:///c:/Users/SON/바이브코딩/프로젝트04/js/script.js) | URL 입력 후 생성 시 부드러운 `cubic-bezier` 트랜지션으로 인풋 독이 하단으로 슬라이드 다운, 중앙에 QR 카드 팝업 |
| **04** | QR 코드 클릭 시 JPG 다운로드 | **완료 (100%)** | [script.js](file:///c:/Users/SON/바이브코딩/프로젝트04/js/script.js) | QR 카드 클릭 시 1200×1200 고해상도 백색 여백 캔버스 생성 후 `.jpg` 포맷 자동 다운로드 |
| **05** | QR 라이브러리 용량 초과 버그 수정 | **완료 (100%)** | [qrcode.min.js](file:///c:/Users/SON/바이브코딩/프로젝트04/js/qrcode.min.js)<br>[script.js](file:///c:/Users/SON/바이브코딩/프로젝트04/js/script.js) | 구형 `qrcodejs`를 가변 길이 자동 감지 및 `UTF-8` 한글 지원 `qrcode-generator`로 전면 교체하여 "오류가 발생했습니다" 예외 완벽 해결 |
| **06** | 로고 맞춤 밝은 톤 테마 리뉴얼 | **완료 (100%)** | [style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | 옐로우 로고와 어우러지는 따뜻한 샴페인 아이보리(`--bg-base: #FAF8F3`) 및 웜 앰버 골드 테마 적용 |
| **07** | 파스텔 앰비언트 그라데이션 적용 | **완료 (100%)** | [style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | 선샤인 옐로우, 소프트 피치, 스카이 아쿠아 톤의 부유형 앰비언트 오브 3종 배치 |
| **08** | 마우스 커서 위치 반응형 그라데이션 | **완료 (100%)** | [script.js](file:///c:/Users/SON/바이브코딩/프로젝트04/js/script.js)<br>[style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | `mousemove` 감속 보간(Lerp) 기반 실시간 커서 스포트라이트 및 방사형 그라데이션 색조(`hue-rotate`) 동적 전환 |
| **09** | 토스트 알림 및 사용자 인터랙션 피드백 | **완료 (100%)** | [index.html](file:///c:/Users/SON/바이브코딩/프로젝트04/index.html)<br>[style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | 빈 값 입력 시 흔들림(Shake) 경고, 다운로드 완료 시 감각적인 토스트 팝업 알림 노출 |
| **10** | 반응형 모바일 최적화 | **완료 (100%)** | [style.css](file:///c:/Users/SON/바이브코딩/프로젝트04/css/style.css) | 640px 이하 모바일 디바이스에서도 인풋 바 너비 및 QR 카드 크기 자동 조절 |

---

## 🔍 상세 세부 작업 항목

- [x] **UI/마크업 설계**
  - [x] [index.html](file:///c:/Users/SON/바이브코딩/프로젝트04/index.html) 시맨틱 태그 구조화 (`<header>`, `<main>`, `<section>`)
  - [x] 상단 좌측 [img/logo.png](file:///c:/Users/SON/바이브코딩/프로젝트04/img/logo.png) 로고 마크업
  - [x] 화면 중앙 Hero 타이틀 & 설명 문구 배치
  - [x] 마우스 인터랙티브 그라데이션 배경 레이어 (`interactive-bg`) 컨테이너 구성
  - [x] QR 카드 뷰 & 호버 오버레이 마크업

- [x] **스타일링 & 모션**
  - [x] 로고 옐로우에 최적화된 라이트 테마 변수(`:root`) 팔레트 정의
  - [x] 커서 반응형 그라데이션 메쉬 및 480px 스포트라이트 스타일링
  - [x] 부드러운 하단 슬라이드 다운 애니메이션 (`transition: 0.65s var(--ease-spring)`)
  - [x] QR 카드 팝업 효과 (`@keyframes qrPopAnim`) 및 호버 플로팅 효과
  - [x] 모바일 반응형 미디어 쿼리

- [x] **로직 & 알고리즘**
  - [x] `qrcode-generator` 라이브러리 연동 및 `UTF-8` 한글 인코딩 보장
  - [x] 에러 정정 레벨(`H` → `Q` → `M` → `L`) 단계별 자동 폴백 로직
  - [x] 60fps 부드러운 마우스 커서 추적 Lerp 보간 루프 구현
  - [x] 1200×1200 순백색 배경 오프스크린 Canvas 렌더링 및 JPG 다운로드
  - [x] 상단 좌측 로고 클릭 시 상태 리셋 및 입력 초기화
