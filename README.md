# 🚀 STLEller v1.0.0 - Premium Local 3D STL/3MF Viewer
> **STLEller**는 Tauri v2와 Three.js 기반의 빠르고 아름다운 데스크톱 3D 파일 뷰어입니다.  
> 오프라인 환경에서도 인터넷 연결 없이 STL 및 3MF 파일을 로드하고, 모델의 물리적인 치수, 부피, 무게 등을 실시간으로 계산 및 시각화할 수 있습니다.
---
## ✨ 핵심 기능 (Key Features)
### 🎨 프리미엄 UI/UX & 테마
- **글래스모피즘(Glassmorphism)**: 트렌디하고 세련된 반투명 다크 모드 인터페이스.
- **다중 테마 지원**: 눈이 편안한 **Dark Mode**와 화사한 **Light Mode**를 완벽하게 지원하며, UI 테마 변경에 따라 3D 뷰포트 배경 및 그리드 색상이 동기화됩니다.
- **반응형 대시보드**: 슬라이딩 드로어(Sliding Drawer) 패턴을 사용한 좌측(설정)/우측(정보) 패널로 화면 공간을 극대화합니다.
### 📐 강력한 3D 모델 및 물리 분석 (Analytics)
- **정밀 치수 측정**: 모델의 가로(X), 세로(Y), 높이(Z) 치수를 mm 단위로 실시간 측정.
- **부피 & 표면적 계산**: 업로드된 메쉬의 정확한 부피($mm^3$)와 표면적($mm^2$)을 실시간 연산.
- **소재별 무게 계산기**: 
  - 3D 프린팅에서 자주 사용되는 다양한 재료(PLA, ABS, PETG, Resin, Nylon 등) 지원.
  - 금속 및 귀금속(Steel, Aluminum, Gold, Silver, Copper) 재질 무게 제공.
  - 사용자가 직접 밀도($g/cm^3$)를 입력할 수 있는 커스텀(Custom) 모드 지원.
### 🔍 다채로운 3D 시각화 제어 (Visualization)
- **렌더링 스타일**: Solid(솔리드), Wireframe(와이어프레임), Points(점구름) 모드 지원.
- **셰이딩 필터**: Flat(로우폴리 스타일) 및 Smooth(부드러운 음영) 지원.
- **커스터마이징**: 모델의 표면 색상, 와이어프레임 색상, 배경 색상을 자유롭게 변경.
- **광원(Light) 제어**: 3D 공간 내의 조명 세기 및 반사율을 조절하여 디테일한 관찰 가능.
- **보조 가이드 장치**: 그리드(Grid), X/Y/Z 축(Axes), 바운딩 박스(Bounding Box), 그림자(Shadow) 토글 지원.
- **카메라 프리셋**: 원클릭으로 정면(Front), 측면(Right), 평면(Top), 등각투영(ISO) 뷰로 카메라 위치 조정.
### ⚡ 하이브리드 & 오프라인 퍼스트 (Offline-First)
- **네이티브 & 브라우저 듀얼 모드**: Tauri 데스크톱 앱과 웹 브라우저 환경 양쪽에서 문제없이 빌드되고 동작하는 듀얼 아키텍처.
- **100% 로컬 독립 실행**: Three.js, STLLoader, 3MFLoader, fflate 등 모든 핵심 라이브러리를 내장하여 네트워크가 차단된 오프라인 환경에서도 원활하게 실행됩니다.
- **강력한 포트백(Fallback)**: Tauri v2 Native API 및 일반 웹 파일 API의 하이브리드 파일 감지 시스템 내장.
---
## ⌨️ 키보드 단축키 (Keyboard Shortcuts)
앱 내에서 빠르게 기능을 제어할 수 있는 다양한 핫키를 지원합니다.
| 단축키 | 기능 설명 |
| :--- | :--- |
| `R` | 카메라 뷰포트 초기화 (Reset View) |
| `F` | 3D 모델에 포커스 (Focus Model) |
| `S` | 솔리드(Solid) 렌더링 모드 전환 |
| `W` | 와이어프레임(Wireframe) 렌더링 모드 전환 |
| `P` | 포인트(Points) 렌더링 모드 전환 |
| `I` | 우측 정보(Information) 패널 열기/닫기 |
| `O` | 좌측 설정(Options) 패널 열기/닫기 |
| `H` | 그리드, 축 등 헬퍼 가이드 일괄 토글 |
| `Space` | 자동 회전(Auto-Rotate) 토글 |
| `Esc` | 로드된 모델 제거 및 초기 화면으로 복귀 |
---
## 🛠 기술 스택 (Tech Stack)
### Desktop App Client
- **Framework**: [Tauri v2](https://v2.tauri.app/) (Rust backend)
- **Frontend Core**: Vanilla HTML5, Vanilla CSS3 (Custom Variables), ES6 Javascript
- **3D Engine**: [Three.js](https://threejs.org/) (Local bundled v0.128.0)
- **Parsers**: `STLLoader.js`, `3MFLoader.js`, `fflate.min.js` (for 3MF unzip)
---
