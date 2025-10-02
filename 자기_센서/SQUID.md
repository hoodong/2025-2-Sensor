# SQUID (초전도 양자 간섭계, Superconducting Quantum Interference Device)

---

## 1. 동작 원리

SQUID는 **매우 미세한 자기장**을 감지할 수 있는 세계에서 가장 민감한 센서 중 하나입니다.  
원리는 **플럭스 양자화(Flux Quantization)**와 **Josephson 접합(Josephson junction)** 효과에 기반합니다.

- **DC SQUID**: 두 개의 Josephson 접합을 병렬로 연결한 구조. 루프 내부 자속 변화에 따라 간섭 패턴이 바뀌며 전압 응답이 달라짐.  
- **RF SQUID**: 하나의 Josephson 접합과 공진 회로를 결합. 구조가 단순하나 감도는 DC SQUID보다 낮음.  

수식적으로는 루프 내부 총 자속 Φ가 항상 양자화되어  
\[
\Phi = n \Phi_0 \quad (\Phi_0 = h / 2e)
\]  
를 만족합니다.  
이 조건 때문에 외부 자기장이 변하면 보상 전류가 발생하고, 그 결과 SQUID 출력 전압이 변하게 됩니다.

📺 **동작 원리 설명 영상**  
[![SQUID 동작 영상](https://img.youtube.com/vi/ql2Yo5LgU8M/0.jpg)](https://www.youtube.com/watch?v=ql2Yo5LgU8M)

---

## 2. 실물 사진 및 구성 요소

![SQUID Sensor](https://tse1.mm.bing.net/th/id/OIP.-HfI9Px4IGdy3bTAqUyX2gHaE6?pid=Api)

### 구성 요소
| 구성요소 | 역할 / 특징 | 크기 |
|---|---|---|
| 초전도 루프 | 자속을 모집하고 간섭 효과 유도 | mm ~ µm |
| Josephson 접합 | Cooper pair 터널링, 위상 간섭 매개 | 수 nm 절연막 두께 |
| Shunt 저항 | 비선형 거동 완화 | 수 Ω |
| 루프 유도성 L | screening current 결정 | 수 pH |
| 입력/피드백 코일 | 외부 자속 결합 및 보상 | mm급 코일 |
| 냉각 시스템 | 초전도 상태 유지(액체 헬륨/질소) | 수십 cm 크기 |
| 자기 차폐 | 외부 노이즈 차폐 | cm 단위 쉴드 |

예: **Mr. SQUID 키트**에서는 1 cm² 칩 위에 제작된 SQUID가 프로브와 냉각기 안에 장착됩니다.  
([Mr. SQUID 매뉴얼](https://starcryo.com/wp-content/themes/education-pro/manuals/MrSQm66.pdf))

---

## 3. 데이터시트 및 핵심 파라미터

SQUID의 성능은 주로 아래 파라미터들로 정의됩니다.

| 파라미터 | 기호/단위 | 설명 | 예시 값 |
|---|---|---|---|
| 자속 잡음 | \(S_\Phi^{1/2}\) (Φ₀/√Hz) | 감도 지표 | 10⁻⁶ Φ₀/√Hz (fT 수준) |
| 전압 변조 깊이 | ΔV (µV) | 출력 전압 변동 폭 | 수 µV ~ 수십 µV |
| 임계 전류 | Ic (µA) | Josephson 접합 초전도 최대 전류 | 수 µA |
| 정규 저항 | Rn (Ω) | 접합 비초전도 상태 저항 | 수 Ω |
| 루프 유도성 | L (pH) | 전류-자속 관계 | 수 pH |
| βL | 무차원 | 선형성·감도 조건 (≈1 적합) | ~1 |
| 바이어스 전류 | Ibias | 동작 전류 | ~2Ic |
| 동작 온도 | K | 초전도 재료에 따라 | 4 K (Nb), 77 K (YBCO) |

참고: [Mr. SQUID 데이터시트](https://starcryo.com/wp-content/themes/education-pro/manuals/MrSQm66.pdf)

---

## 4. 구체적 응용 사례 — MEG (뇌자기파 측정)

![MEG 장비 예시](https://tse2.mm.bing.net/th/id/OIP.FimiPA-fO1hkQ9UZa0ujkQHaHo?pid=Api)
<img width="217" height="314" alt="image" src="https://github.com/user-attachments/assets/3f106c3a-4ed7-4f7a-be10-c189a42b1508" />



MEG(Magnetoencephalography)는 뇌의 활동으로 인해 발생하는 미세한 자기장을 측정하여 뇌 기능을 비침습적으로 영상화하는 기술. 
뇌에서 뉴런들이 전기 신호를 주고받을 때 미세한 자기장이 발생하는데, 이 자기장은 매우 약하기 때문에 이를 측정하기 위해서는 극도로 민감한 센서가 필요-> SQUID는 이러한 미세한 자기장을 감지하는 데 사용되는 초고감도 자력계이.

### 원리
- 센서들은 헬멧 내부 곳곳에 배열되어 뇌의 다양한 영역에서 나오는 신호를 동시에 측정
초전도체 고리: 이 그림은 초전도체로 만들어진 고리 모양의 센서
조셉슨 접합: 고리에는 전류가 흐르기 어려운 조셉슨 접합이라는 아주 좁은 통로가 두 개 있습니다.
자기장 감지: 뇌에서 발생한 미세한 자기장이 이 고리를 통과하면, 고리를 흐르던 전류에 변화가 생깁니다.
전압 신호: 이 변화는 그래프처럼, 고리에서 측정되는 전압을 주기적인 파동으로 바꿉니다. 자기장이 강해질수록 이 파동의 변화도 커집니다.

### 특징
- **민감도**: 극도로 미세한 자기장(10⁻¹³에서 10⁻¹⁵ 테슬라)
- **용도**: 뇌전증(간질) 환자, 뇌종양 및 기타 뇌질환 수술 환자, 또는 치매, 파킨슨병, 정신 질환 등 다양한 신경 및 정신 질환의 진단과 연구에도 사용
- **환경**: 자기 차폐실 필요(외부 자기장 간섭 차단)

---


---

