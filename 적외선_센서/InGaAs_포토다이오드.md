# 동작원리 
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




# 실물사진 및 설명  
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
\
APD 포토다이오드는 P⁺, P⁻, P층으로 구성된 다층 구조를 가지고 있으며, 각 층은 고유한 역할을 한다.    
캐리어 농도가 낮은 P⁻층에서 빛을 흡수하여 전자-정공 쌍이 생성되며, 생성된 전자는 전기장에 의해 P층으로 이동한다.    
이동 과정에서 전자는 반도체 내 원자와 충돌하며 추가적인 전자-정공 쌍을 생성한다.  
이렇게 새롭게 생성된 전자들도 같은 방식으로 이동하며 다시 충돌을 일으키고, 전자-정공 쌍을 연쇄적으로 만들어낸다.    
이러한 연쇄 반응은 전자-정공 쌍의 수를 눈사태처럼 증가시키며, 결과적으로 아주 약한 빛 신호도 강한 전류로 증폭해 감지할 수 있게 된다.   
  
APD는 PIN에 비해 감도가 높아 미약한 빛도 감지할 수 있지만, 노이즈 역시 함께 증폭되므로 주의가 필요하며, 더 높은 전압이 요구된다.   

# 데이터시트 및 설명  
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


# 구체적 응용사례



