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

---

# 3. 데이터시트 요약설명

---

# 4. 응용사례
