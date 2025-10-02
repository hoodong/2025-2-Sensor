동작 원리


실물사진 및 설명

 
데이터시트 및 설명
  
# I²C Interface I/O Characteristics (VIO = 1.8 V)

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
  
구체적 응용사례 (한가지 응용사례를 골라 사진 등을 통해 깊이있게 설명할 것)


 
