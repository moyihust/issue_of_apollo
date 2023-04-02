# Apollo issues

可能出现的简写：

自动驾驶车辆，Autonomous Vehicle（AV）

自动驾驶，Autonomous Driving（AD）

#### [#5803](https://github.com/ApolloAuto/apollo/issues/5803)

- 自定义程序（自己编写的模块）可以通过编译但无法正常运行

#### [#14347](https://github.com/ApolloAuto/apollo/issues/14347)
- msf_localization组件启动失败，原因如下：反射贴图文件夹无效

应该是配置问题

#### [#14326](https://github.com/ApolloAuto/apollo/issues/14326)
- linux的perf对apollo-rt不起作用
- 请求帮助

#### [#14302 ](https://github.com/ApolloAuto/apollo/issues/14302)
- apollo5.0版本
- 配置drawview因为权限问题无法打开

#### [#14291](https://github.com/ApolloAuto/apollo/issues/14291)
- apollo6.0
- cyber_visualizer无法放大或缩小
- `export MESA_GL_VERSION_OVERRIDE=3.3`参数不对

#### [#14262](https://github.com/ApolloAuto/apollo/issues/14262)
- 为什么激光雷达探测结果偏航角减去四分之一 π
- 数学问题

#### [#14248](https://github.com/ApolloAuto/apollo/issues/14248)
- 如何获取模型源文件
- 在云服务器上训练项目的方法

#### [#14235](https://github.com/ApolloAuto/apollo/issues/14235)
- /reference_line模块，发现 QP 求解器可能会返回不满足约束的解
- 求解器可能无法找到最优解并返回次优解

#### [#14224](https://github.com/ApolloAuto/apollo/issues/14224)
- 需要改进描述深度图像的文档。
- 可以改进

#### [#14217](https://github.com/ApolloAuto/apollo/issues/14217)
- 启用D-kit时报错“MSF_LOCAL_LIDAR_OUT_OF_MAP
- 配置问题

#### [#14207](https://github.com/ApolloAuto/apollo/issues/14207)
- 询问延迟和模块延迟的定义和计算方法

#### [#14187 ](https://github.com/ApolloAuto/apollo/issues/14187)
- apollo 5.0
- 优化过程协方差矩阵Q和测度协方差矩阵R的分布

#### [] 

#### [#13440](https://github.com/ApolloAuto/apollo/issues/13440)
- 想要对Apollo各种模块的IO进行性能分析,请求指导建议。
- #学习问题

#### [#13439](https://github.com/ApolloAuto/apollo/issues/13439)

- 想要对特定模块启用或者禁用，请求指导建议。
- 不建议修改，Apollo项目的构建没有支持这种灵活性。
- #学习问题

#### [#13430](https://github.com/ApolloAuto/apollo/issues/13430)

- 障碍物存储在Point3D中，不知道如何获取障碍物的速度。
- 障碍物的速度可以通过消息中的`velocity`字段获取。
- #学习问题

#### [#13429](https://github.com/ApolloAuto/apollo/issues/13429)

- 1.询问相机坐标中x是前方还是右方。
- z轴表示前进方向，x轴表示右侧，y轴表示垂直方向。
- 2.代码中的参数顺序是否有问题
- 认为这里确实有错误，更改参数顺序效果更好
- #代码问题

#### [#13391](https://github.com/ApolloAuto/apollo/issues/13391)

- 感知模块启动失效
- Apollo 版本过低，对RTX2080不支持
- #配置问题

#### [#13385](https://github.com/ApolloAuto/apollo/issues/13385)

- 指出判断参考线是否重叠的代码可能存在逻辑问题
- #代码问题

#### [#13384](https://github.com/ApolloAuto/apollo/issues/13384)

- 询问为什么使用某个模块的某个函数计算距离
- #学习问题

#### [#13374](https://github.com/ApolloAuto/apollo/issues/13374)

- 询问如何将CyberRT的消息类型转换为ROS的消息类型以使用ROS接口
- 使用apollo_ros_bridge
- #学习问题

#### [#13372](https://github.com/ApolloAuto/apollo/issues/13372)

- 在点云中无法显示障碍物的minbox
- 认为是显卡驱动的问题
- #配置问题

#### [#13365](https://github.com/ApolloAuto/apollo/issues/13365)

- 在某个头文件中有边界和左边界计算存在问题，并给出建议
- #代码问题

#### [#13357](https://github.com/ApolloAuto/apollo/issues/13357)

- 训练cruise mlp模型数据不平衡问题
- 可能是特征和标签问题
- #学习问题

#### [#13351](https://github.com/ApolloAuto/apollo/issues/13351)

- 在aarch64架构下使用优化选项后，GetCurrentRoutine返回了旧值，导致程序出错。
- 需要在CMake中添加-fPIC选项，否则在一些arm64平台上会出现问题。
- #配置问题

#### [#13337](https://github.com/ApolloAuto/apollo/issues/13337)

- 代码元素类型不匹配
- #代码问题

#### [#13324](https://github.com/ApolloAuto/apollo/issues/13324)

- 不知道有一个循环如何进入
- #学习问题

#### [#13316](https://github.com/ApolloAuto/apollo/issues/13316)

- 发送路由请求汽车没有反应
- 可能是shrink调用不当
- #配置问题

#### [#13315](https://github.com/ApolloAuto/apollo/issues/13315)

- 想要用mpc控制器启动控制模块，但是系统依然使用Lat和Lon
- #学习问题

#### [#13308](https://github.com/ApolloAuto/apollo/issues/13308)

- 想要获取当前路段所有参考线的信息
- #学习问题

#### [#13302](https://github.com/ApolloAuto/apollo/issues/13302)

- 检测到交通锥，但是没有避开
- #代码问题

#### [#13301](https://github.com/ApolloAuto/apollo/issues/13301)

- Smoke3D模型改变相机或安装位置，导致训练模型失效
- 较难解决
- #学习问题

#### [#13298](https://github.com/ApolloAuto/apollo/issues/13298)

- 感知模块构建失败
- Apollo不完全支持aarch64架构
- #配置问题

#### [#13290](https://github.com/ApolloAuto/apollo/issues/13290)

- 成员内存泄漏问题，没有限制成员的增长
- 函数声明没有实现
- #代码问题

#### [#13288](https://github.com/ApolloAuto/apollo/issues/13288)

- 感知模块启动崩溃
- 分别启动模块，定位问题
- #配置问题

#### [#13266](https://github.com/ApolloAuto/apollo/issues/13266)

- 询问如何输出RSS信息
- #学习问题

#### [#13248](https://github.com/ApolloAuto/apollo/issues/13248)

- canbus通信的不同波特率之间有什么关系
- 给不同设备使用
- #学习问题

#### [#13228](https://github.com/ApolloAuto/apollo/issues/13228)

- 增加障碍物出现意外情况
- #代码问题

#### [#13205](https://github.com/ApolloAuto/apollo/issues/13205)

- 如何在vscode中调试apollo
- 在docker环境调试就不用其余配置
- #学习问题

#### [#13180](https://github.com/ApolloAuto/apollo/issues/13180)

- 某次代码提交将start_time移动到其他位置，感到困惑
- #学习问题
















