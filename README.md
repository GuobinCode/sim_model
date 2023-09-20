%**************************************************************
 % @Project sim_model
 % @Company SZU
 % @Author  Guobin Li
 % @Target  导航基础仿真环境
 % @data    2023-9-18
 % All rights reserved
%**************************************************************

version:
1.0: 包含一个四轮机器人模型(带运动控制器，16线激光雷达及IMU)以及两个world环境(平坦和非平坦).


程序依赖：
1. 小车模型相关依赖：
	sudo apt-get install ros-melodic-velodyne-gazebo-plugins
2. gazebo仿真环境依赖：
	将scout_model包中的models中的文件拷贝到Home/.gazebo/models中
3. 键盘控制节点：
	sudo apt-get install ros-melodic-teleop_twist_keyboard


程序编译：
	catkin_make


程序运行：
1. 启动gazebo仿真环境:
	roslaunch sim_model show_model.launch
2. 启动键盘控制节点：
	rosrun teleop_twist_keyboard teleop_twist_keyboard.py


其它问题：
1. 解决gazebo启动失败[gazebo_gui-3] process has died [pid 8683, exit code 134：
	killall gzserver && killall gzclient 

