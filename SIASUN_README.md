## 1. use colcon build
    mkdir rslidar_ws && cd rslidar_ws
    mkdir src && cd src
    git clone -b dev_siasun_sensor_fusion https://github.com/tjsiasun/rslidar_sdk.git
    cd rslidar_sdk/
    git submodule update --init --recursive
    cd src/rs_driver/
    git checkout dev_siasun_sensor_fusion
    cd ../../../
    git clone https://github.com/RoboSense-LiDAR/rslidar_msg.git
    cd ..
    colcon build
    source install/setup.bash
    ./build/rslidar_sdk/rslidar_sdk_node

    