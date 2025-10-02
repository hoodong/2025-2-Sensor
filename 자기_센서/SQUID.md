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

## ✅ 특징 요약

- SQUID는 **“초전도 루프 + Josephson 접합 2개”**가 핵심 구조.  
- **루프 크기**는 응용 목적에 따라 달라져서, 고감도 자성 탐침은 µm 이하, 일반 센서는 수백 µm까지 가능.  
- **접합 크기**는 수십~수백 nm 수준이 일반적 (공정 기술 의존).  
- **유도성 + 저항 값**은 설계에서 노이즈 특성과 직결.  
- **Mr. SQUID** 같은 교육용 칩은 칩 크기 약 1 cm² 안에 루프·접합·코일이 모두 집적.  

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

### 배경
- 뇌 활동은 뉴런 전류로부터 fT(10⁻¹⁵ T) 수준의 미세 자기장을 발생시킵니다.
- 이를 비침습적으로 측정하는 장치가 **MEG (Magnetoencephalography)**입니다.

### 원리
- 다수의 SQUID 센서를 반구형 헬멧 구조로 배열
- 뇌에서 발생한 자기장을 감지하여 실시간 신호 수집
- 역문제(inverse problem)를 풀어 뇌 전류 분포를 지도화

### 특징
- **민감도**: 수십 fT 수준 감지 가능
- **용도**: 뇌전증 병소 탐지, 인지 기능 연구, 뇌신경망 지도화
- **환경**: 자기 차폐실 필요

---


---

