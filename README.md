# Vins-Simplified

**Description**:
This codes are mainly based on the most common Visual-Inertial Odometry (VIO) open source code VINS-MONO but with simplified backend algorithms. The codes do not necessarily rely on ROS and g2o. We replaced the origin backend parts into simplified vertex-edge optimization structure by only using C++ Eigen library. The main optimization algorithms is dogleg. The results are evaluated by the VIO common evaluation tool evo. 

The code support both Ubuntu and MacOS.

### Installation：

1. pangolin: <https://github.com/stevenlovegrove/Pangolin>

2. opencv

3. Eigen

4. Ceres

### Compilation

```c++
mkdir vins_simplified
cd vins_simplified
git clone https://github.com/Zhi29/VINS-simplified
mkdir build 
cd build
cmake ..
make -j4
```

### Run
#### 1. CurveFitting Example to Verify Our Solver.
```c++
cd build
../bin/testCurveFitting 
```

#### 2. VINs-Mono on Euroc Dataset
```c++
cd build
../bin/run_euroc /home/dataset/EuRoC/MH-05/mav0/ ../config/
```
![vins](doc/vins.gif)


### 感谢

我们使用了港科大沈老师组的 [VINS-Mono](https://github.com/HKUST-Aerial-Robotics/VINS-Mono) 作为基础代码，非常感谢该组的工作。

