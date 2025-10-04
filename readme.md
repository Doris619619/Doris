以下步骤编译
```bash
# 解压压缩包
unzip pb2025_infantry_ws.zip
# 进入工作空间
cd pb2025_infantry_ws/
# 完成依赖安装
sudo rosdep init
rosdep update
rosdep install -r --from-paths src --ignore-src --rosdistro $ROS_DISTRO -y
# 开始编译
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=Release --parallel-workers 10
# 如果编译卡住，说明电脑性能不行，把10改小
```