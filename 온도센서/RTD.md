# RTD (Resistance Temperature Detector)
---

## 1. 동작 원리

RTD는 **온도에 따라 금속의 전기저항이 변하는 성질**을 이용한 온도센서이다.



### 🔹 핵심 개념
- **원리:** 온도가 상승하면 금속 내 **원자 진동이 증가**하여 **전자 이동이 방해**받고, **저항이 증가**한다.  
- **측정 방식:** RTD 소자에 일정 전류를 흘려 **전압 강하 → 저항값 계산 → 온도로 변환**



### 🔹 구조 형태
| 구분 | 설명 | 특징 |
|------|------|------|
| **권선형 (Wire-wound type)** | 백금선 등을 세라믹 또는 유리 코어에 **정밀하게 감아 제작** | - 높은 정확도와 안정성<br>- 내열성 우수<br>- 구조가 커서 응답속도 다소 느림 |
| **박막형 (Thin-film type)** | 백금 박막을 절연기판 위에 **증착 및 패턴 형성** | - 소형·응답속도 빠름<br>- 진동 내성 우수<br>- 장기 안정성은 권선형보다 다소 낮음 |



### 🔹 대표 재료
- **백금(Platinum, Pt):** 가장 널리 사용, 선형성과 안정성 우수 (예: **Pt100**, **Pt1000**)  
- **니켈(Ni)**, **구리(Cu)** 등도 일부 산업용으로 사용됨



### 🔹 장점
- 매우 **정확하고 반복성 우수**  
- **장기 안정성** 뛰어남 (드리프트 ≤ 0.1 °C/년)  
- **넓은 측정 범위:** –200 °C ~ 650 °C (특수형은 850 °C까지 가능)  
- **선형성 우수** (열전대·서미스터 대비)  
- **면 또는 점 단위 측정 가능**  
- **호환성 및 표준화**가 잘 되어 있음  
- **산업계 표준화 확립** (IEC 751 등)


### 🔹 단점
- **가격이 비싸고 크기가 큼** (열전대·서미스터보다)  
- **동작 전류가 필요**하며, **자가발열** 가능성 있음  
- **저항값이 작음** → 정밀 측정 회로 필요  
- **진동·충격에 약함** (특히 권선형)  
- **비직선성 보정을 위한 보정회로** 필요  
- **열전대보다 내구성 떨어짐**



---


## 2. 실물 사진 및 구성 요소

### 📸 실물 예시
![PT100 RTD Probe](https://upload.wikimedia.org/wikipedia/commons/5/5c/PT100_Resistance_Temperature_Detector.jpg)
![PT100 Thin Film Element](https://upload.wikimedia.org/wikipedia/commons/6/69/PT100_Thin_film_element.jpg)

---

### ⚙️ 주요 구성 요소

| 구성 요소 | 설명 | 대표 크기 / 사양 |
|------------|------|----------------|
| **감지 소자 (Platinum Element)** | 백금선을 세라믹 기판에 감거나, 박막 형태로 제작된 온도 감지부 | Thin-film: `2.3×1.2×1.1 mm` ~ `5.0×2.0×1.1 mm`<br>Wire-wound: `Ø 1.5×15 mm` |
| **보호관 (Sheath)** | 감지 소자를 보호하는 금속관. 외부 충격·습기·부식 방지 | 재질: 316L 스테인리스<br>외경: `1.5 – 8 mm` |
| **절연 충전재 (MgO)** | 내부 리드선을 절연하고 열전달 효율을 높임 | 고순도 산화마그네슘 분말 |
| **트랜지션 (Epoxy Potting)** | 보호관과 케이블 접합부를 수지로 밀봉하여 방수·인장 보호 | 길이 `15 – 25 mm` |
| **리드선 / 케이블** | 2·3·4선식 연결 방식, 절연재는 고온 대응(FEP/PFA) | 기본 길이 `1 m` |
| **종단부 (Termination)** | 회로 연결용 단자 (M12 커넥터, 포크 단자 등) | 선택 사양 |
| **써모웰 (옵션)** | 교체 및 내압성 향상을 위한 외부 보호관 | 나사형 / 플랜지형 |

---

### 📏 크기 예시

| 타입 | 외경 | 길이 | 온도 범위 |
|------|------|------|------------|
| 소형 프로브 | Ø 3 mm | 76 mm | −70 ~ 200 °C |
| 산업용 프로브 | Ø 6.35 mm (¼″) | 152 mm | −70 ~ 500 °C |
| 엘리먼트 단품 | 2.3 ~ 5 mm (길이) | — | −200 ~ 600 °C |

---

### 🧩 형태별 예시

| 타입 | 특징 | 예시 이미지 |
|------|------|--------------|
| **리드선형 프로브** | 케이블 일체형, 기계·3D프린터 등에 사용 | ![Lead Wire RTD](https://cdn.omega.com/Images/Temperature/RTD/PT100-SENSOR.jpg) |
| **M12 커넥터형** | 탈착이 쉬우며 IP67 방수 | ![M12 RTD](https://cdn.shopify.com/s/files/1/0266/0561/9888/files/m12_rtd_sensor.jpg) |
| **헤드형 터미널** | 플랜트 공정용, 단자박스 결선 가능 | ![Terminal Head RTD](https://www.labfacility.com/media/catalog/product/cache/pt100-head-assembly.jpg) |
| **엘리먼트 단품** | 세라믹 위 백금 박막칩 형태 | ![Thin Film Element](https://upload.wikimedia.org/wikipedia/commons/6/69/PT100_Thin_film_element.jpg) |

---

### 💰 가격 정보 (2025년 기준 대략가)

| 제품명 / 형태 | 제조사 | 주요 사양 | 가격(₩, 부가세 제외) | 판매처 |
|----------------|---------|-------------|------------------|---------|
| **PT100 기본형 RTD 프로브** | G마켓 (OEM) | Ø6mm × 100mm, 3선식 | 약 **₩30,000** | [G마켓](https://www.gmarket.co.kr) |
| **Adam Tech CA-TS-003 RTD PT100** | DigiKey | 산업용, 3선식, 500°C | 약 **₩78,000** | [DigiKey](https://www.digikey.kr) |
| **Labfacility PT100 Probe (3×50mm)** | Labfacility | 소형, Class A | 약 **₩79,000** | [element14](https://kr.element14.com) |
| **PT100 NPT 터미널 헤드형** | 국내 유통 (산업용) | ¼″ NPT, IP67 헤드 | 약 **₩30,000** | [G마켓](https://www.gmarket.co.kr) |
| **PT100 NPT 스레드형** | AliExpress | 6mm × 100mm, 3선 | 약 **₩11,000** | [AliExpress](https://www.aliexpress.com) |
| **Pico SE011 Pt100 Probe** | Pico Tech | 데이터로거용, Class A | 약 **₩64,000** | [element14](https://kr.element14.com) |
| **OMEGA RTD-805-B 고정밀형** | OMEGA | 산업용, Class A, SS 시스 | 약 **₩510,000** | [DigiKey](https://www.digikey.kr) |

> 💡 가격은 제조사/길이/정확도 등급(Class A·B)에 따라 크게 달라지며,  
> **일반형은 1–3만원대**, **정밀형·산업용은 5–50만원대**까지 다양합니다.

## 3. 데이터시트 및 핵심 파라미터
---
# RTD Sensor Datasheet: TE Connectivity PTS060301B100RPU00

---

### 1. 일반 사양 (General Specifications)
* **모델명**: `PTS060301B100RPU00`
* **제조사**: TE Connectivity
* **종류**: 백금 박막 RTD (Platinum Thin Film RTD)
* **공칭 저항**: 100 Ω at 0°C
* **측정 온도 범위**: -55°C ~ 155°C

---

### 2. 저항 및 온도 특성 (Resistance & Temperature Characteristics)
* **온도 저항 계수 (TCR / α)**: 3850 ppm/K (`0.00385 Ω/Ω/°C`)
* **표준**: IEC 60751

---

### 3. 정확도 및 공차 (Accuracy & Tolerance)
* **공차 등급**: Class B (F0.3)
* **허용 오차**: `±(0.3 + 0.005|T|) °C`
    * **0°C 에서의 오차**: ±0.3°C
    * **100°C 에서의 오차**: ±(0.3 + 0.005 × 100) = ±0.8°C

---

### 4. 동적 및 전기적 특성 (Dynamic & Electrical Characteristics)
* **응답 시간 (Response Time, τ_0.63)**:
    * **공기 중 (v=1m/s)**: 약 3초
    * **물 속 (v=0.4m/s)**: 약 0.15초
* **자가 발열 계수 (Self-heating)**: 0.4 K/mW at 0°C
* **최대 측정 전류**: 1mA
* **절연 저항**: > 100 MΩ at 25°C

---

### 5. 물리적 사양 (Physical Specifications)
* **크기 (Dimensions)**: 0603 패키지 (1.6mm x 0.85mm x 0.45mm)
* **리드선 (Termination)**: 니켈 배리어 위의 100% 무광 주석 도금 (솔더링용)
* **안정성 (Long-term Stability)**: 최대 저항 변화 < 0.04% (1000시간, 155°C 노출 후)

## 4. 구체적 응용 사례 — MEG (뇌자기파 측정)
---
