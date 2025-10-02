# 2025 - 2 Wiki for Sensor Engineering Group 1, Week 4 <br/> Topic: Hall IC <br/> *Members: 양범석, 성시원, 김인우, 박민규*
# 1. 동작 원리
---
홀 IC는 **자기장을 전기 신호로 바꾸는 센서**로, '홀 효과'를 핵심 원리로 사용합니다.  

* 전류가 흐르는 반도체(홀 소자)에 자기장이 가해지면, 여기에 수직 방향으로 **미세한 전압(홀 전압)** 이 발생합니다.
* 내장된 증폭기가 이 작은 전압을 **사용 가능한 수준**으로 크게 증폭시킵니다.  
* 증폭된 신호는 슈미트 트리거를 거치며 노이즈가 제거되고, **깨끗한 디지털(ON/OFF)** 신호로 변환됩니다.  

이러한 비접촉 방식으로 작동해 내구성이 뛰어나며, **자동차 속도 센서나 스마트폰 커버 감지** 등에 널리 활용됩니다.  

🖥️ 동작원리 설명 영상  
[![Watch the video](https://img.youtube.com/vi/R7yb6DDTGH0/hqdefault.jpg)](https://www.youtube.com/watch?v=R7yb6DDTGH0)  

# 2. 실물 사진 및 설명
## ACS70310 선형 홀 IC (Linear Hall IC)   
<img width="600" height="436" alt="Image" src="https://github.com/user-attachments/assets/77a08b1f-b227-458a-928d-5efc5985a012" />  

ACS70310은 소형(길이 약 5.5mm) 4핀 패키지에 **홀 센서**(자기장 감지용)와 **내장 전원/증폭회로**를 가진 전류 센서 IC입니다.

아날로그 전압으로 빠르고 정밀하게(±1% 이내) 자기장과 전류의 변화를 측정하며,  PCB 실장 및 전류 센싱용으로 사용됩니다.

Allegro MicroSystems에서 제조, 1개당 가격은 ₩6,086 입니다. 

---

# 3. 데이터시트 및 요약설명
## ACS70310 & ACS70311 선형 홀 IC
<img width="599" height="781" alt="스크린샷_20251002_101336" src="https://github.com/user-attachments/assets/48aaff23-f19b-4f54-9a46-8762a2c2a93b" />

**특징**  
□ 공장 프로그래밍된 선형 온도 보상(TC)으로 초저 온도 드리프트 실현  
□ 감도 오차: ±1%  
□ 오프셋 오차: ±5 mV  
□ 역배터리 보호 내장 전원 조절기로 높은 전기적 스트레스(EOS) 내성  
□ 매우 빠른 응답 시간(2μs 이하)  
□ 높은 작동 대역폭: DC ~ 240 kHz    
 
**설명**  
□ ACS70310 & ACS70311 IC는 BICMOS 집적 회로와 함께 홀 소자를 내장하여 완전한 선형 전류 센서 IC를 구성합니다.  
□ TC 홀 소자는 IC 표면에 수직인 자기장 흐름에 민감  
□ 출력은 자기 유속 밀도에 비례하는 아날로그 전압  
□ ACS70310/11은 페라자성 코어와 함께 사용되도록 설계되어 높은 정확도의 전류 측정 제공  
□ 전체 온도 범위(25°C ~ 150°C)에서 ±1% 감도 오차 및 ±5mV 오프셋 오차  

---

# 4. 응용사례
## BLDC 모터  

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/1fd4f5b6-2cf3-48d6-a060-d5a403c3bc30" />  
필즈모터 사의 BLDC 모터 90600원  

<img width="1620" height="1222" alt="image" src="https://github.com/user-attachments/assets/0e576c36-a063-446a-a932-e4ac3d1a9b6f" />  
BLDC 모터는 영구자석이 있는 회전자로 구성되며, 홀 IC는 회전자의 정확한 위치를 감지하여 코일에 전류를 적시에 전환하는(정류하는) 역할을 합니다. 이를 통해 모터의 회전 속도와 방향을 정밀하게 제어할 수 있습니다.
