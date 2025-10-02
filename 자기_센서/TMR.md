# 동작 원리 (핵심 개념을 잘 설명하고 있는 동영상을 넣을 것)  

# 실물사진 및 설명 (구성요소와 크기를 구체적으로 설명할 것)  

# 데이터시트 및 설명 (핵심 파라미터들을 자세히 설명할 것)  

| Parameters                          | Units | Min  | Typ  | Max  |
|-------------------------------------|-------|------|------|------|
| Average Supply Current (IDD AVG)    | nA    | 200  | -    | 700  |
| Switching Frequency (fsw)           | Hz    | 1    | 2    | 4    |
| Active Mode Time (tACT)             | µs    | 1.4  | -    | -    |
| Idle Mode Time (tIDLE)              | ms    | 500  | -    | -    |
| Operate Point (BOPN)                | G     | 27   | 30   | 38   |
| Operate Point (BOPS)                | G     | -38  | -30  | -27  |
| Release Point (BRPN)                | G     | -27  | -    | 27   |
| Release Point (BRPS)                | G     | -27  | -20  | -18  |
| Hysteresis (BHYST)                  | G     | 5    | 10  
** G : Gauss, 자기장의 세기를 나타내는 단위 
  
- Average Supply Current : 센서가 정상적으로 동작할 때 소비하는 평균 전류
- Switching Frequency : 센서가 얼마나 빠르게 상태를 전환할 수 있는지를 나타냄. 이 값이 높을 수록 센서는 더 빠르게 자기장 변화를 감지하고 반응할수 있음.
- Active Mode time : 센서가 동작하는 동안의 시간
- Idle Mode Time : 센서가 대기 모드로 전환하는데 걸리는 시간. 대기 모드는 센서가 데이터를 수집하지 않고, 전력소비를 최소화하는 상태
- Operate Point (BOPN, BOPS) : 센서가 자기장 신호를 받아 출력이 활성화(ON)되는 임계 자기장 값입니다. BOPN은 음극 방향 자기장, BOPS는 양극 방향 자기장을 의미합니다.  
- Release Point (BRPN, BRPS) : 센서가 자기장 신호가 약해져서 출력이 비활성화(OFF)되는 임계 자기장 값입니다. BRPN은 음극 방향, BRPS는 양극 방향 자기장에 대한 복구점입니다. 보통 BRP 값은 BOP 값보다 자기장 세기가 낮습니다.  
- Hysteresis (BHYST) : 동작점(BOP)과 복귀점(BRP) 사이의 자기장 차이로, 센서가 신호의 잦은 ON/OFF 전환 없이 안정적으로 동작하도록 돕는 기능입니다. 히스테리시스 값이 클수록 센서는 작은 자기장 변동에 덜 민감하게 반응합니다.
 * **Hysteresis**는 **자기장이 변할 때 센서의 반응이 다르게 일어나는** 현상을 나타냅니다. 즉, 센서가 **BOP (Operate Point)**에 도달하여 **HIGH** 상태로 바뀌고, 자기장이 다시 감소하여 **BRP (Release Point)**에 도달하면 **LOW** 상태로 변합니다. 하지만 자기장이 **BRP**로 감소했다고 해서 센서가 즉시 **LOW**로 전환되는 것은 아니며, **BOP**에 도달하기까지 센서는 일정한 자기장 변화 구간을 거치게 됩니다.
  
# 구체적 응용사례 (한가지 응용사례를 골라 사진 등을 통해 깊이있게 설명할 것)
