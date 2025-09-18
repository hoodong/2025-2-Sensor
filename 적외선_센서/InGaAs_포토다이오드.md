# 1.동작원리 
**인듐(In), 갈륨(Ga), 비소(As)** 를 혼합하여 만든 반도체 소자  
InGaAs 포토다이오드는 광전 효과를 활용하여 **빛** 을 **전기 신호** 로 변환하는 반도체 센서이다.  
광자가 InGaAs 물질에 닿으면 반도체 내에서 자유롭게 이동할 수 있는 전자-정공 쌍이 생성된다.  
InGaAs 포토다이오드는 **pin** 과 **APD** 구조로 만들어진다.  

## pin  
pn형 포토다이오드를 개량한 구조를 가진 광검출기이다.  
p형 반도체 층과 n형 반도체 층 사이에 **i형(Intrinsic)** 층을 사이에 둔 구조이다.   
pin형 포토다이오드 동작 시 i형 층에 역바이어스 전압을 인가하여 **강한 전기장** 을 형성한다.  
빛이 i형 층에 조사되면 전자와 홀 쌍이 생성되고, 전기장의 영향으로 전자와 홀이 각각 n형과 p형 층으로 이동하여 전류가 흐른다.
<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/23aaaf1c-e44f-4300-8869-8f66f5771fb8" />
 

## APD  
APD의 작동 원리는 **'애벌런시 증배(Avalanche multiplication)'** 라는 현상을 기반으로 한다.  
고전압을 가한 상태에서 광자가 전자-정공 쌍을 생성할 때, 내부 증폭 과정을 통해 큰 전류를 생성한다.  
이 과정을 통해 작은 빛의 신호도 강한 전기 신호로 증폭시킬 수 있다.  
<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/b3cae04a-db60-4eee-a767-871f05e342cf" /> <img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/f7db34bd-c0a5-4658-a2aa-f589ae67b712" />




# 2.실물사진 및 설명  
InGaAs 포토다이오드는 PIN구조와 APD구조로 나뉜다.   

## PIN  
---
<img width="291" height="564" alt="image" src="https://github.com/user-attachments/assets/82e2ad22-912b-4f21-ab3f-a8135e254e2b" />     
<img width="524" height="288" alt="image" src="https://github.com/user-attachments/assets/92741bb9-eadb-4ea3-8835-409aec5baa19" />      
<img width="563" height="416" alt="image" src="https://github.com/user-attachments/assets/7353ffbf-9ffa-4ba8-a6f5-e9f0b516f901" />  

\
PIN 포토다이오드는 P형과 N형 반도체 사이에 I층이 끼어 있는 구조이다.  
I층은 전자나 정공이 거의 없는 순수한 반도체층으로, 빛을 효율적으로 흡수할 수 있다.  
빛을 흡수하면 전자-정공 쌍이 생성되고, 이들이 전기장에 의해 이동하면서 전류가 생성된다.  

## APD
---
<img width="291" height="506" alt="image" src="https://github.com/user-attachments/assets/04bc4d77-cd2f-4e03-936d-34eb19da9cd8" />    
<img width="692" height="283" alt="image" src="https://github.com/user-attachments/assets/51080661-a5de-403b-a54a-f10f80a808d2" />    
<img width="700" height="388" alt="image" src="https://github.com/user-attachments/assets/c5248b2c-611d-4ce0-a339-e3488c56e85e" />  


APD 포토다이오드는 P⁺, P⁻, P층으로 구성된 다층 구조를 가지고 있으며, 각 층은 고유한 역할을 한다.

캐리어 농도가 낮은 P⁻층에서 빛을 흡수하여 전자-정공 쌍이 생성되며, 생성된 전자는 전기장에 의해 P층으로 이동한다.  

이동 과정에서 전자는 반도체 내 원자와 충돌하며 추가적인 전자-정공 쌍을 생성한다.  

이렇게 새롭게 생성된 전자들도 같은 방식으로 이동하며 다시 충돌을 일으키고, 전자-정공 쌍을 연쇄적으로 만들어낸다.  

이러한 연쇄 반응은 전자-정공 쌍의 수를 눈사태처럼 증가시키며, 결과적으로 아주 약한 빛 신호도 강한 전류로 증폭해 감지할 수 있게 된다.  

  
APD는 PIN에 비해 감도가 높아 미약한 빛도 감지할 수 있지만, 노이즈 역시 함께 증폭되므로 주의가 필요하며, 더 높은 전압이 요구된다.   

# 3.데이터시트 및 설명  
## 주요 사양  
| 사양 | 설명 | 단위 및 일반적인 값 |
|:---|:---|:---|
| **Spectral Response Range** | 감지 가능한 빛의 파장 범위. 광통신에 적합한 900nm~1700nm에 특화 | nm, µm |
| **Responsivity** | 입사된 광파워(W)에 대한 출력 전류(A)의 비율. 이 값이 높을수록 빛에 대한 감도 좋음 | A/W |
| **Dark Current** | 빛이 없을 때 흐르는 누설 전류. 낮은 값일수록 노이즈가 적어 미약한 신호 감지 유리 | nA, µA |
| **Capacitance** | 다이오드의 정전용량. 낮을수록 응답 속도가 빠름 | pF |
| **Bandwidth** | 포토다이오드가 처리할 수 있는 신호의 최대 주파수. 고속 데이터 전송 시 중요 | MHz, GHz |

### FGA10 InGaAs photodiode datasheet  
<img width="327" height="194" alt="image" src="https://github.com/user-attachments/assets/f6608f6d-4ba9-4b33-a46a-9b78cacc1cdf" />


## Responsivity vs Wavelength  
<img width="358" height="250" alt="image" src="https://github.com/user-attachments/assets/4fbc8377-12ac-43a6-b655-3657936822ae" />


## Dark Current vs Reverse Voltage  
<img width="554" height="423" alt="image" src="https://github.com/user-attachments/assets/b0ab9080-dac0-44b9-905d-f8dd1c42db58" />


# 4.구체적 응용사례
[InGaAs PIN]_빛이 충분히 들어올 때, 빠르게 신호를 처리하는 기본 센서  
얘는 단순하다. 데이터가 안정적인 환경에서 제 성능을 낸다.  
1. 광섬유 통신  
   광섬유를 통한 데이터 전송은 대용량 데이터 전송에 유리하며, 장거리 전송에서도 효율  
   PIN 다이오드의 낮은 노이즈 특성과 빠른 응답 속도 덕분에 고속 통신과 대규모 데이터 전송에 사용  

2. 광학 센서_레이저 거리측정기, 온도 센서, 산업용 센서  

어디에 사용되는가?  
<<케이블 티비, 데이터 센터>>  
1. 광신호를 전기 신호로 바꾸는 기본 소자. 빠른 응답속도, 적은 노이즈, 안정적인 신호처리  
2. APD에 비해 저렴 & 회로 간단_굳이 민감할 필요 없음  
<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/e200d2f7-4138-4305-a8b1-8edb53051654" />  

[InGaAs APD]_빛이 약하거나 신호가 작을 때도, 증폭해서 알아챌 수 있는 고감도 센서  
얘는 민첩하다. 버퍼층이 데이터를 증폭시키기 때문에, 비교적 약한 데이터, 빠른 데이터를 처리해야하는 일에 유리하다.  
그래서 고속통신 및 원거리 감지, Lidar에 사용된다  
  
1. 원거리 감지_헬리콥터, 드론, 위성  
   위성 통신에서의 원거리 탐지 및 영상 분석.  
   지구 관측 및 기후 변화 연구에 중요한 역할  
   드론은 이용한 모니터링과 안전 감시  
  
2. Lidar  
   LiDAR 시스템은 자동차 자율주행, 지리 정보 시스템(GIS), 3D 모델링 등 다양한 분야에서 사용  
   특히 자율주행차의 주변 환경 인식에 필수적이며, 지형 분석과 건축 설계에 중요한 역할  
   미약한 신호를 증폭시켜 3D맵상에 표시해야 하기 때문에 높은 민감도 요구  
  
어디에 사용되는가?  
<< 전쟁용 드론 >>  
1. Lidar 센서_APD는 라이다의 핵심 부품  
2. 적외선 카메라_병력식별  
3. 레이저 거리 측정/목표 조준기_고감도 수광  
4. 고속 통신_광수신기  
<img width="512" height="236" alt="image" src="https://github.com/user-attachments/assets/f8f8b7a5-2f6c-408b-aeb7-b1e72834bbb6" />  


미군의 MQ-9 Reaper 드론,  
이스라엘의 Heron, Harop 드론,  
우크라이나 전장에서 쓰인 중국·이란제 드론들  
→ 다수는 LiDAR 기반 센서 또는 적외선 감지 시스템 탑재  


