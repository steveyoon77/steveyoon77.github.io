# thesis: Motion tracking in field sports using GPS and IMU

- M. Roobeek, Delft university of technology

## 1. Introduction

### 1.2 Background

![](./img/2022-09-01-00.jpg)

## 2. Methods and materials

### 2.2. Sensors

#### 2.2.1 Inertial Measurement Unit(IMU)

![](./img/2022-09-01-01.jpg)

### 2.3 Filters

#### 2.3.1 Unscented Kalman Filter (UKF)

##### Unscented Transformation

![](./img/2022-09-02-00.jpg)

##### Update formular

![](./img/2022-09-02-01.jpg)

![](./img/2022-09-05-00.jpg)

##### Handling quaternions in the unscented tranformation

![](./img/2022-09-05-01.jpg)

![](./img/2022-09-05-02.jpg)

#### 2.3.2 Madgwick filter

![](./img/2022-09-05-03.jpg)

##### Orientation from angular velocity

##### Orientation from a homogeneous field

![](./img/2022-09-05-04.jpg)

![](./img/2022-09-05-05.jpg)

##### Orientation from a homogeneous field

![](./img/2022-09-06-00.jpg)

![](./img/2022-09-06-01.jpg)

##### Fusion process

![](./img/2022-09-06-02.jpg)

### 2-4 Models

![](./img/2022-09-07-00.jpg)

#### 2-4-1 Linear Kalmann filter

![](./img/2022-09-07-01.jpg)

#### 2-4-2 Translation UKF

![](./img/2022-09-07-02.jpg)

#### 2-4-3 Rotation UKF

![](./img/2022-09-07-03.jpg)

#### 2-4-4 Full state

![](./img/2022-09-07-04.jpg)

#### 2-4-5 Filter Configuration

![](./img/2022-09-07-05.jpg)