<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:1D4ED8,100:38BDF8&height=140&section=header&text=&fontSize=0" width="100%" alt="Gradient header">

<div align="center">

# 도재우 | Jae Woo Do

**Embedded SW · Linux Driver · Qt HMI**

데이터시트와 코드, 실측을 바탕으로 센서·통신·구동부의 문제를 해결하는 임베디드 SW 개발자입니다.

<a href="mailto:herobine159@naver.com"><img src="https://img.shields.io/badge/Email-03C75A?style=flat-square&logo=naver&logoColor=white" alt="Email"></a>
<a href="https://kevin-jwd.github.io"><img src="https://img.shields.io/badge/Portfolio-222222?style=flat-square&logo=githubpages&logoColor=white" alt="GitHub Pages Portfolio"></a>
<a href="https://puzzle-bard-f1b.notion.site/783e70bea00444908a1be0d235f03e13"><img src="https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white" alt="Notion Portfolio"></a>

</div>

> **[포트폴리오 상세 보기 →](https://kevin-jwd.github.io)**
> 프로젝트별 구현 과정, 시스템 구조와 시연 자료는 포트폴리오에서 확인하실 수 있습니다.

## 👋 소개

- 한국공학대학교 전자공학부 전자공학과 졸업 (2025.02)
- **MCU 제어:** ATmega128A의 타이머·인터럽트·UART·PWM을 활용한 센서·모터 제어
- **Linux 드라이버:** Jetson 환경의 I2C 센서·LCD 커널 드라이버와 문자 장치 인터페이스 구현
- **HMI·비전 연동:** Qt 차량 제어 GUI, 인물 검출·재식별, 추적 좌표 기반 팬틸트 제어
- **RTL 설계:** Verilog 기반 I2C Master·Slave, 센서 측정 타이밍 및 표시 모듈 구현
- **문제 해결·기록:** 데이터시트 확인 → 코드·통신 점검 → 하드웨어 측정, 변경 내용과 점검 절차 문서화

## 🛠 Tech Stack

| 분야 | 사용 기술 |
| --- | --- |
| Languages | C · C++ · Python · Verilog HDL |
| MCU & Boards | ATmega128A · ESP32 · STM32 · ARM Cortex-M4 · Arduino · Raspberry Pi · Jetson Orin Nano |
| Linux & Interfaces | Linux Kernel · Device Tree · I2C · UART |
| HMI & Database | Qt Widgets · Qt SerialPort · PyQt · SQLite |
| AI & Vision | OpenCV · YOLO · TensorRT |
| FPGA & Tools | Vivado · Basys 3 · Git · GitHub |

---

## 💻 주요 프로젝트

### 01. [I2C Sensor RTL — 센서 수집·통신·표시 시스템](https://github.com/Kevin-jwd/i2c-sensor-driver)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/i2c-rtl.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.11.04 ~ 2026.11.06 | 2명 (본인 포함) | 팀 프로젝트 |

<img src="https://img.shields.io/badge/Verilog-654FF0?style=flat-square" alt="Verilog"> <img src="https://img.shields.io/badge/Vivado-ED1C24?style=flat-square&logo=amd&logoColor=white" alt="Vivado"> <img src="https://img.shields.io/badge/Basys%203%20%C3%97%202-555555?style=flat-square" alt="Basys 3 × 2"> <img src="https://img.shields.io/badge/I2C-0078D4?style=flat-square" alt="I2C"> <img src="https://img.shields.io/badge/DHT11-00897B?style=flat-square" alt="DHT11"> <img src="https://img.shields.io/badge/HC--SR04-00897B?style=flat-square" alt="HC-SR04"> <img src="https://img.shields.io/badge/SSD1306-555555?style=flat-square" alt="SSD1306">

- **개요:** 두 FPGA를 I2C로 연결해 온습도·거리 데이터를 수집하고 FND·OLED로 표시하는 시스템
- **담당:** I2C Master·Slave 양쪽과 센서 수집·FND·OLED 표시 등 RTL 전반 직접 구현
- **구현:** DHT11·HC-SR04 측정, FPGA 간 I2C 전송과 데이터 표시, 체크섬·타임아웃 검사, 센서 타이밍 파형 비교 및 모듈 테스트벤치 작성
- **관련 문서:** [설계 설명·검증 자료](https://github.com/Kevin-jwd/i2c-sensor-driver)

---

### 02. [Linux Driver — 스마트 선풍기 센서·LCD 드라이버](https://github.com/Electric-fan-driver/Fan_Linux_Driver/tree/feat/input-buttons)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/smart-fan.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.10.08 ~ 2026.10.13 | 4명 (본인 포함) | 팀 프로젝트 |

<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white" alt="C"> <img src="https://img.shields.io/badge/Linux%20Kernel-333333?style=flat-square" alt="Linux Kernel"> <img src="https://img.shields.io/badge/I2C-0078D4?style=flat-square" alt="I2C"> <img src="https://img.shields.io/badge/Device%20Tree-00897B?style=flat-square" alt="Device Tree"> <img src="https://img.shields.io/badge/Jetson%20Orin%20Nano-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Jetson Orin Nano">

- **개요:** Jetson Orin Nano에서 센서와 구동부를 연동하는 스마트 선풍기 시스템
- **담당:** BMP180 온도 센서·LCD1602 커널 드라이버 및 사용자 공간의 문자 장치 접근 인터페이스
- **구현:** 보정 계수·변환 완료 상태를 반영한 온도 읽기, `pwrite()` 기반 LCD 부분 갱신, `ioctl()` 기반 화면·백라이트 제어
- **관련 문서:** [담당 범위·드라이버 구조·트러블슈팅](https://github.com/Kevin-jwd/Lectures/tree/main/Linux/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8)

---

### 03. [Vision Tracker — 인물 추적 팬틸트 카메라](https://github.com/Vision-Tracker-Project/Vision_Tracker_Project)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/vision-tracker.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.09.02 ~ 2026.09.16 | 4명 (본인 포함) | 팀 프로젝트 |

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/YOLO11-111F68?style=flat-square" alt="YOLO11"> <img src="https://img.shields.io/badge/TensorRT-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="TensorRT"> <img src="https://img.shields.io/badge/BoT--SORT-654FF0?style=flat-square" alt="BoT-SORT"> <img src="https://img.shields.io/badge/OSNet-654FF0?style=flat-square" alt="OSNet"> <img src="https://img.shields.io/badge/Jetson%20Orin%20Nano-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Jetson Orin Nano"> <img src="https://img.shields.io/badge/UART-0078D4?style=flat-square" alt="UART">

- **개요:** 선택한 인물을 카메라로 자동 추적하고 게임패드로 차체를 수동 조작하는 Jetson 기반 팬틸트 시스템
- **담당:** 웹 실행 환경, AI 인물 추적·재식별, 팬틸트 제어 로직·MCU 명령 전송, 카메라·차체 제작. MCU 펌웨어는 팀원 담당
- **구현:** YOLO 검출·BoT-SORT 추적·OSNet 재식별, 최근 3개 검출 박스의 중앙값 필터, 팬틸트 동작 시작·정지 경계 분리 및 각도 제한
- **관련 문서:** [시스템 구조](https://github.com/Vision-Tracker-Project/Vision_Tracker_Project/blob/main/AI/ARCHITECTURE.md) · [프로젝트 소개·시연](https://github.com/Vision-Tracker-Project/Vision_Tracker_Project)

---

### 04. [Vehicle HMI — 운전자 인증 기반 차량 제어·모니터링](https://github.com/Kevin-jwd/HMI-qt)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/vehicle-hmi.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.08.14 ~ 2026.08.19 | 4명 (본인 포함) | 팀 프로젝트 |

<img src="https://img.shields.io/badge/C%2B%2B17-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++17"> <img src="https://img.shields.io/badge/Qt%20Widgets-41CD52?style=flat-square&logo=qt&logoColor=white" alt="Qt Widgets"> <img src="https://img.shields.io/badge/QSerialPort-41CD52?style=flat-square&logo=qt&logoColor=white" alt="QSerialPort"> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite">

- **개요:** 얼굴 인증 후 차량 조작을 활성화하고 센서·주행 상태를 모니터링하는 Qt HMI 시스템
- **담당:** PC 측 Qt HMI, UART 송수신, 얼굴 인증, 영상 처리 스레드 구성 및 이력 관리. 팀원이 구현한 STM32 펌웨어와 연동
- **구현:** Haar Cascade·LBPH 얼굴 인증과 동일 인물 5회 연속 확인, 카메라 획득·표시·인식 스레드 분리, 200ms 하트비트, 센서 상태 표시 및 SQLite 이력 조회
- **관련 문서:** [얼굴 인증](https://github.com/Kevin-jwd/HMI-qt/blob/main/FACE_RECOGNITION_GUIDE.md) · [데이터베이스](https://github.com/Kevin-jwd/HMI-qt/blob/main/DATABASE.md) · [설치·실행](https://github.com/Kevin-jwd/HMI-qt/blob/main/INSTALL.md)

---

### 05. [ATmega128A — LCD·RTC 드라이버](https://github.com/Kevin-jwd/atmega128-rtc-lcd-clock)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/lcd-rtc.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.07.01 ~ 2026.07.03 | 2명 (본인 포함) | 팀 프로젝트 |

<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white" alt="C"> <img src="https://img.shields.io/badge/Microchip%20Studio-EE2A24?style=flat-square&logo=microchip&logoColor=white" alt="Microchip Studio"> <img src="https://img.shields.io/badge/GPIO-555555?style=flat-square" alt="GPIO"> <img src="https://img.shields.io/badge/I2C-0078D4?style=flat-square" alt="I2C">

- **개요:** ATmega128A에서 RTC의 시간을 읽어 LCD에 표시하고 계산기 기능과 통합한 시스템
- **담당:** GPIO 4비트 LCD 드라이버와 I2C RTC 시간 읽기·표시. 계산기 기능은 팀원 담당
- **구현:** LCD 초기화·문자 출력, RTC 시간 읽기·표시, Slave 주소와 메모리 주소를 구분한 I2C 접근 절차 적용
- **관련 문서:** [LCD·RTC 구현 코드](https://github.com/Kevin-jwd/atmega128-rtc-lcd-clock) · [프로젝트 소개·자료](https://kevin-jwd.github.io/projects/lcd-rtc.html)

---

### 06. [ATmega128A — 자율주행 RC Car](https://github.com/Kevin-jwd/rc-car-control)

**[프로젝트 상세 보기 →](https://kevin-jwd.github.io/projects/rc-car.html)**

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 2026.06.22 ~ 2026.06.25 | 1명 (개별 차량) | 개인 구현 · 공동 발표 |

<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white" alt="C"> <img src="https://img.shields.io/badge/Microchip%20Studio-EE2A24?style=flat-square&logo=microchip&logoColor=white" alt="Microchip Studio"> <img src="https://img.shields.io/badge/Timer-555555?style=flat-square" alt="Timer"> <img src="https://img.shields.io/badge/Interrupt-555555?style=flat-square" alt="Interrupt"> <img src="https://img.shields.io/badge/UART-0078D4?style=flat-square" alt="UART"> <img src="https://img.shields.io/badge/PWM-0078D4?style=flat-square" alt="PWM">

- **개요:** 초음파 센서로 장애물에 대응하며 자율주행과 Bluetooth 수동 주행을 지원하는 ATmega128A RC Car
- **담당:** 개별 RC Car의 센서 수집, 주행 제어 및 상태 표시 전반
- **구현:** 초음파 센서 3개와 칼만 필터를 이용한 장애물 대응, 타이머·외부 인터럽트 기반 Echo 시간 측정, Bluetooth UART 명령 처리, PWM 모터 제어 및 FND 표시
- **관련 문서:** [프로젝트 소개·자료](https://kevin-jwd.github.io/projects/rc-car.html) · [소스 코드·구현 문서](https://github.com/Kevin-jwd/rc-car-control)

## 🔧 추가 프로젝트

### 07. IMU 기반 가정용 Personal Training 시스템

| 기간 | 참여 인원 | 구분 |
| --- | --- | --- |
| 기간 미기재 | 4명 (본인 포함) | 졸업작품 |

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/LSM9DS1%20%C3%97%204-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white" alt="LSM9DS1 × 4"> <img src="https://img.shields.io/badge/PCA9548A-555555?style=flat-square" alt="PCA9548A"> <img src="https://img.shields.io/badge/I2C-0078D4?style=flat-square" alt="I2C"> <img src="https://img.shields.io/badge/UDP%2FTCP-0078D4?style=flat-square" alt="UDP/TCP"> <img src="https://img.shields.io/badge/Unity-222222?style=flat-square&logo=unity&logoColor=white" alt="Unity">

- **개요:** 여러 IMU로 신체 움직임을 수집하고 Unity 모델과 연동하는 가정용 Personal Training 시스템
- **담당:** IMU 데이터 수집, 센서 보정·자세 추정 및 ESP32·서버·Unity 간 데이터 전달
- **구현:** I2C MUX를 통한 IMU 4개 수집, 쿼터니언 기반 자세 추정, 자력계 캘리브레이션·Low-pass 필터, ESP32 → UDP 로컬 서버 → TCP Unity 전달
- **관련 문서:** [프로젝트 소개·수상 내역](https://kevin-jwd.github.io/projects/imu-pt.html)

### 기타 구현·학습 프로젝트

| 프로젝트 | 기술 | 주요 내용 | 기간 · 인원 |
| --- | --- | --- | --- |
| [Jetson RPS Game](https://github.com/Kevin-jwd/Jetson-RSP-game) | Python · YOLO11 · TensorRT | 손동작 인식 기반 1·2인 가위바위보 게임, 0.4초 구간 다수결 판정 및 좌우 반전 추론 | YYYY.MM ~ YYYY.MM · __명 |
| [Motor Control](https://github.com/Kevin-jwd/motor_control_mini_project) | C · STM32F411 · GPIO · Timer2 | 버튼 입력 시간에 따른 정회전·역회전·정지 제어, FSM·흐름도 문서화 | YYYY.MM ~ YYYY.MM · __명 |
| [FPGA 기초 설계](https://github.com/Kevin-jwd/FPGA) | Verilog · Vivado · XSim | 가산기·MUX·ROM·비교기·디바운싱 회로, 테스트벤치와 회로도 정리 | YYYY.MM ~ YYYY.MM · __명 |

---

## 🎓 학력 · 교육

| 기간 | 소속 / 과정 |
| --- | --- |
| 2019.03 ~ 2025.02 | 한국공학대학교 전자공학부 전자공학과 졸업 |
| 2025.01 ~ 2025.07 | 프로그래머스 데브코스 6기 — 웹 풀 사이클 개발 |
| 2026.05 ~ 현재 | 대한상공회의소 서울기술교육센터 AI 시스템반도체 SW개발자 과정 |

## 🏆 수상

- **2024 한국통신학회 학술대회 학부 우수논문 장려상**  
  모션 트래킹 기반 가정용 Personal Training 시스템
- **한국공학대학교 로봇 프로그래밍 경진대회 동상**  
  햄스터로봇을 활용한 과제 해결

## 📫 연락처

- **Email**: [herobine159@naver.com](mailto:herobine159@naver.com)
- **Portfolio**: [GitHub Pages](https://kevin-jwd.github.io) · [Notion](https://puzzle-bard-f1b.notion.site/783e70bea00444908a1be0d235f03e13)

---

<details>
<summary><b>📊 GitHub Activity</b></summary>

<br>

<p align="center">
  <a href="https://github.com/Kevin-jwd">
    <img src="https://github-stats-extended.vercel.app/api/top-langs/?username=Kevin-jwd&layout=compact&theme=material-palenight&hide_border=true&bg_color=20232a&text_color=ffffff&title_color=58A6FF" width="40%" alt="Most used languages">
    <img src="https://github-stats-extended.vercel.app/api?username=Kevin-jwd&show_icons=true&theme=material-palenight&hide_border=true&bg_color=20232a&icon_color=58A6FF&text_color=ffffff&title_color=58A6FF" width="56%" alt="GitHub stats">
  </a>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Kevin-jwd&theme=react-dark&bg_color=20232a&hide_border=true&line=58A6FF&color=58A6FF" width="98%" alt="GitHub contribution activity">
</p>

</details>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0F172A,50:1D4ED8,100:38BDF8&height=40&section=footer&text=&fontSize=0" width="100%" alt="Gradient footer">

