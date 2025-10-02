## 1. 동작 원리 

- 강자성체 물질의 전기 저항이 외부 자기장의 방향에 따라 변화하는 현상을 이용한다.
- 자성을 띠는 물질에 전류를 흘릴 때  
  - 외부에서 자기장이 가해지면 물질 내부의 자화 방향이 변화  
  - 저항 값 변화  
  - 자기장 세기와 방향을 감지  
- 저항 변화는 전류의 방향과 자화 방향에 따라 달라진다.  
  - 평행: 저항이 최대  
  - 수직: 저항이 최소  

→ 이 저항 변화를 측정하여 자기장의 세기와 방향을 감지한다.  

[설명 영상](https://www.youtube.com/watch?v=F8B8dm2HFME) (0:34~1:00)

---

## 2. 실물사진 및 설명  

![이미지 설명](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLkLeaY4PklzJP4iNfFM-N6boBq4ose8dFWw&s) MMC5603NJ  

- 단가 : 개당 969원  
- 축 : 3방향을 감지할 수 있는 X,Y,Z로 구성  
- 크기 : 0.82 mm × 0.82 mm × 0.40 mm  

---

## 3. 데이터시트 및 설명

### 3.1 주요 기능 및 측정 범위 

- ±30 G 측정 범위, 20비트 분해능, 2 mG RMS 노이즈, ±1° 방위각 정확도  
- 온칩 SET/RESET 자기소거, 감도 및 온도 보상 기능  
- I²C/I³C 인터페이스(≤400 kHz), 초저전력(대기 전류 1 μA)  
- 초소형 패키지(0.8 × 0.8 × 0.4 mm), 전원 1.62–3.6 V 지원  

### 3.2 주요 파라미터  

#### I²C Interface I/O Characteristics (VIO = 1.8 V)

| Parameter                          | Symbol   | Test Condition                  | Min   | Typ | Max        | Unit |
|-----------------------------------|----------|---------------------------------|-------|-----|------------|------|
| Logic Input Low Level             | VIL      |                                 | -0.5  |     | 0.3 * VIO  | V    |
| Logic Input High Level            | VIH      |                                 | 0.7*VIO |   | VIO        | V    |
| Hysteresis of Schmitt input       | VHYS     |                                 | 0.2   |     |            | V    |
| Logic Output Low Level            | VOL      |                                 |       |     | 0.4        | V    |
| Input Leakage Current             | II       | 0.1VIO < VIN < 0.9VIO           | -10   |     | 10         | μA   |
| SCL Clock Frequency               | fSCL     |                                 | 0     |     | 400        | kHz  |
| START Hold Time                   | tHD;STA  |                                 | 0.6   |     |            | μs   |
| START Setup Time                  | tSU;STA  |                                 | 0.6   |     |            | μs   |
| LOW period of SCL                 | tLOW     |                                 | 1.3   |     |            | μs   |
| HIGH period of SCL                | tHIGH    |                                 | 0.6   |     |            | μs   |
| Data Hold Time                    | tHD;DAT  |                                 | 0     |     | 0.9        | μs   |
| Data Setup Time                   | tSU;DAT  |                                 | 0.1   |     |            | μs   |
| Rise Time                         | tr       | From VIL to VIH                 |       |     | 0.3        | μs   |
| Fall Time                         | tf       | From VIH to VIL                 |       |     | 0.3        | μs   |
| Bus Free Time Between STOP & START| tBUF     |                                 | 1.3   |     |            | μs   |
| STOP Setup Time                   | tSU;STO  |                                 | 0.6   |     |            | μs   |

---

## 4. 구체적 응용사례

### AMR 휠 속도 센서 (Wheel Speed Sensor)

이방성 자기저항(Anisotropic Magnetoresistance, AMR) 소자는 자화(Magnetization) 방향과 전류 방향 사이의 각도에 따라 저항값이 정밀하게 변하는 특성을 활용합니다.  

이는 자동차의 안티록 브레이크 시스템(ABS) 및 전자식 자세 제어 장치(ESC)에서 휠 속도를 비접촉식으로 측정하는 핵심적인 역할을 수행합니다.  

<img width="259" height="195" alt="unnamed" src="https://github.com/user-attachments/assets/7ee5e11c-2b10-46ff-8b4d-55492efcd853" />

---

### 4.1 동작 과정

- **자기장 변화의 전기 신호 변환**  
  휠 속도 센서는 AMR 소자를 포함하는 센서 모듈과 휠 허브에 부착되어 회전하는 링 마그넷(혹은 톤 휠)의 상호작용을 통해 작동합니다.

- **기준 자기장 설정**  
  AMR 소자 주변에는 영구 자석이 배치되어 AMR 소자에 일정한 **기준 자기장(HB)** 을 공급합니다.

- **회전 및 외부 자기장**  
  휠이 회전함에 따라 휠에 부착된 링 마그넷 (N극과 S극이 교대로 배열됨)이 AMR 센서 앞을 주기적으로 지나갑니다.  

- **합성 자기장 변화**  
  링 마그넷의 극성 변화(HExt)는 센서의 AMR 소자에 가해지는 전체 **합성 자기장(HTotal = HB + HExt)** 의 방향을 주기적으로 변화시킵니다.  
  외부 자기장 변화에 따라 자화 방향(즉, 저항 변화의 원인이 되는 방향)을 조정함.

- **저항 변화 및 측정**  
  AMR 소자는 이 합성 자기장의 방향 변화에 대해 저항값이 정밀하게 변화합니다.  
  이 미세한 저항 변화는 휘트스톤 브리지 회로를 통해 증폭됩니다. 변화된 자기장 방향을 정확한 비례 저항으로 변환하는 변환기 역할.

- **신호 출력**  
  저항 변화는 휠의 회전에 맞춰 주기적인 구형파(Pulse) 전압 신호로 출력됩니다.  
  이 펄스 신호의 주파수를 분석하여 휠의 속도를 계산합니다.

---

### 4.2 AMR 센서의 핵심 역할: 정밀한 디지털 신호 발생

AMR 소자는 휠 속도 센서의 성능을 혁신적으로 향상시키는 '정밀 자기 계측기 및 디지털 신호 발생기' 역할을 수행합니다.

- **초저속 감지 능력**  
  AMR은 유도형 센서와 달리 자기장 **변화율**이 아닌 자기장 **방향** 자체에 반응하므로, 휠이 거의 정지한 초저속 상태에서도 정확한 펄스 신호를 안정적으로 생성합니다.  
  이는 **ABS 시스템이 정지 직전까지 작동**할 수 있게 하는 결정적인 요소입니다.

- **노이즈 내성 및 정확성**  
  AMR의 휘트스톤 브리지 출력은 깨끗한 디지털 형태의 구형파로 쉽게 가공될 수 있어, 전기적 노이즈나 환경적 변동에도 불구하고 높은 정확도와 신뢰성을 유지합니다.

- **높은 분해능**  
  AMR 기술의 높은 민감도는 링 마그넷의 작은 톱니(극성) 간격도 정확히 분해하여 측정할 수 있게 하며, 이는 차량의 속도 데이터를 더욱 세밀하게 제공하여 **ESC와 같은 복잡한 제어 시스템의 성능을 극대화**합니다.





 
