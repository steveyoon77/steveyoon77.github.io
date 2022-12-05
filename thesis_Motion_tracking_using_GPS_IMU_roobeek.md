# thesis: Motion tracking in field sports using GPS and IMU

## 1. Introduction

### 1.2 Background

- GPS: GPS는 지구상 추적장치의 위치를 측정하기 위해 인공위성을 이용한다. 위치 측정에서 On-Chip 필터가 무향(directionless) 속도 추정을 유도한다. 필터링 동작 때문에 위치 추정 오차는 zero-mean-white-noise(ZMWN)이 아니다.
- IMU: 3축 가속도 센서는 추적 장치 좌표계에서 가속도를 측정한다. 가속도 센서는 중력 가속도와 운동 가속도를 모두 측정한다. 정확한 추적 장치의 3차원 추정을 위해서는 중력 성분을 구분할 필요가 있다. 자이로스코프와 전자 나침반은 설명을 생략한다.
0 Filtering techniques: 추적 정치의 회전 운동은 시스템을 비선형화한다. 아마도 가장 넓게 응용되는 필터링 테크닉은 Extended Kalman Filter(EKF)일 것이다. EKF는 비선형 모델을 선형화하여 칼만 필터를 적용한다. Unscented Kalman Filter는 Vander Merwe와 Julier에 의해 개발됐는데, 똑똑하게 선택된 포인트들을 비선형 모델을 통해 전파시킨다. 변환된 포인트들로부터 새로운 상태 추정이 전통적인 칼만 필터와 유사한 방법으로 계산된다. 또 다른 기술로 IMU에서 기원된 Madgwick 필터가 있다. 이 필터는 자이로스코프, 가속도계, 전자나침반에 최고로 최적화된 시작점을 찾기 위해 One-step gradient discent 최적화를 사용한다. Unscented Kalman Filter는 한 번에 모든 상태를 추정하도록 설계될 수 있다. 그러나 상태 추정을 회전과 평행이동 파트로 분리할수도 있다. 방향 추정에서는 가속도 센서를 중력 센서로 사용할 수 있고 상태 벡터의 평행 이동 파트에서는 가속도 센서로 사용할 수 있다는 것이 이득이다. [^1] 회전 상태는 Kraft 필터나 Madgwick 필터를 참고하여 UKF로 추정할 수 있다. 평행 이동 운동 모델은 쉽게 선형화하여 선형 칼만 필터를 이용할 수 있도록 한다. 측정 모델로 GPS 수신기에서 제공하는 directionless 속도 추정을 추가함으로써 전통적인 모델도 비선형화된다. UKF는 상태 벡터의 이 파트를 위해서 사용될 수 있다.

## 2. Methods and Materials

### 2.2 Sensors

#### 2.2.1 Inertial Measurement Unit(IMU)

##### Accelerometer

MEMS 가속도계는 전기 피에조를 통해 각 축의 방향에 가해지는 힘으로부터 가속도를 계산해낸다. MEMS는 가장 중요한 Scale Factor가 되는, 축의 misalignment와 bias에 의해 Factor에 결합하게 되는 다양한 에러를 동반한다.

##### Gyroscope

자이로스코프는 3개의 축 각각에서 코리올리 효과를 이용하여 각속도를 측정한다.

##### Calibration

가속도계와 자이로스코프를 조정하기 위해 세밀하게 지향성과 각도를 조절 할 수 있는 기계적인 플랫폼을 일반적으로 이용한다.

$$
RMSE_{acc} = \sqrt{\cfrac{\sum_{i=1}^{n}(\|a_i\|-g)^2}{n}}\\\ \
a_{bias} = \cfrac{\sum_{i=1}^{n} a_i-R_g}{n}
$$

# Foot note

[^1]: The possible advantage is that the accelerometer can be used as a 'gravity sensor' in the orientation estimation and as an 'acceleration sensor' in estimating the translational part of the state vector.