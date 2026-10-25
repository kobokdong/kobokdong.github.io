# kobokdong Portfolio

C++·Qt 통신 스레드, STM32 제어, Linux Device Driver 프로젝트를 소개하는 한국어 정적 포트폴리오입니다.

## 구성

- `index.html`: 외부 빌드 도구 없이 열 수 있는 반응형 단일 페이지
- 차량 프로젝트: 팀 전체 기능과 개인 담당인 **C++ 기반 Qt UART 통신 스레드 구현** 구분
- 모터 프로젝트: UART·버튼 입력, 타이머, PWM 및 상태 처리 설명
- Linux 프로젝트: Jetson Orin Nano 스마트 선풍기의 드라이버·사용자 앱·Device Tree 구조 소개. 개인 담당은 BMP180 센서 드라이버와 사용자 앱 통합. 모터·EC11·LED 바 드라이버는 시스템 연동 맥락으로 구분
- 키보드 탐색, 본문 바로가기, 모바일 레이아웃, 인쇄 스타일 지원

## GitHub Pages 게시

이 저장소의 **Settings → Pages → Build and deployment**에서 다음과 같이 설정합니다.

1. Source: **Deploy from a branch**
2. Branch: **main**, Folder: **/ (root)**
3. Save

배포가 완료되면 `https://kobokdong.github.io/`에서 확인할 수 있습니다. 저장소에 파일을 추가하는 것만으로 Pages 활성화 여부가 보장되지는 않습니다.

## 내용의 근거

- [MINI_MOTOR_PROJECT](https://github.com/kobokdong/MINI_MOTOR_PROJECT): README, main.c, exception.c, timer.c
- [Qt_ARM-Vehicle_Control_System](https://github.com/kobokdong/Qt_ARM-Vehicle_Control_System): README, project_qt/mainwindow.cpp, mainwindow.h, serialworker.cpp, project_arm/handler.c, state_manager.c, motor.c, uart.c
- [linux_driver_project](https://github.com/Kyuhyeon34/linux_driver_project): Application/fan_app.c, fan_app.h, drivers/dc_motor/motor.c, motor_ioctl.h, motor-overlay.dts, drivers/ec11/ec11.c, drivers/bmp180/bmp180.c, drivers/ledbar/ledbar.c
- 개인 담당: 저장소 소유자가 제공한 역할 설명 — Qt 앱에서 C++로 UART 통신을 위한 스레드 구현; Linux 프로젝트에서 BMP180 센서 및 사용자 앱 통합

차량 프로젝트의 화면·영상은 원본 README의 GitHub 첨부 자료를 참조합니다. 화면 이미지는 원본 저장소의 외부 URL을 사용하므로 링크 접근 상태에 영향을 받으며, 원본 README 링크를 함께 제공합니다.

성과 수치, 개발 기간, 실측 속도, 개인이 담당하지 않은 팀 기능을 개인 성과로 기재하지 않았습니다. 모터 제어의 약 1초 대기 및 듀티 범위는 소스 설정을 설명하며, 이 포트폴리오 작성 중 펌웨어 빌드·실물 보드 검증은 수행하지 않았습니다.

## 수정

`index.html`의 문구와 스타일을 수정하면 됩니다. 별도 설치나 JavaScript 의존성은 없습니다. 현재 개인 이름과 이메일은 제공되지 않아 GitHub 계정명과 프로필 링크를 사용합니다.

Linux 프로젝트는 저장소 소스코드 기준이며, 대상 Jetson 보드에서 커널 모듈 빌드·적재·실물 시험을 수행하지 않았습니다. 자동 모드 온도 임계값과 듀티는 코드의 설정값입니다.
