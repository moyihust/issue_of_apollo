#### [#13817](https://github.com/ApolloAuto/apollo/issues/13817)
- 询问是否能将机器学习模型导出为其他格式，如ONNX等，他尝试了torch.onnx.export，但是没有成功.他想知道ScriptModule的神经网络架构
- apollo版本: 6.0
- 2021 年 5 月 29 日
- 学习问题

#### [#13812](https://github.com/ApolloAuto/apollo/issues/13812)
- 提出控制代码中计算的加速度公式和另一个文件中的公式不一致的问题
- 2021 年 5 月 27 日
- 代码问题
```
控制代码中计算加速度误差的公式为：
acc_error = reference_point.a() - lon_acceleration / one_minus_kappa_lat_error
其中
lon_acceleration = linear_a * cos(heading_error)
one_minus_kappa_lat_error = 1 - reference_point.path_point().kappa() * linear_v * sin(heading_error )

结果与 modules/common/math/cartesian_frenet_conversion.cpp 文件中的加速度计算不匹配。
```

#### [#13811](https://github.com/ApolloAuto/apollo/issues/13811)
- 使用aarch64运行 talker/listener 失败，排查问题后问题只出现在aarch64上，日志没有输出有用信息，询问如何排查问题
- apollo版本: 6.0
- 2021 年 5 月 27 日
- 配置问题

#### [#13807](https://github.com/ApolloAuto/apollo/issues/13807)
- 无人车在正常行驶过程中出现了失控，调试后发现lateral_error在得到一次NAN后，就会一直保持这个值。推荐使用std::isnan()进行判断。
- 2021 年 5 月 26 日
- 代码问题
```
lateral_error = lateral_error_filter_. 更新（横向错误）；

这里返回的值是什么并不重要，但有必要检查该值：
  if (std::isnan(x_insert)) {
    return x_insert;
  }
```

#### [#13792](https://github.com/ApolloAuto/apollo/issues/13792)
- 询问LaneDetectionComponent 类中的 project_matrix_ 和 pitch_diff_ 字段的作用。似乎 project_matrix_ 表示从一台相机中的像素坐标转换到另一个相机中的像素坐标。很可能，pitch_diff_表示同一字坐标系中两个相机之间的俯仰角差，是真的吗。
- 2021 年 5 月 20 日
- 学习问题


#### [#13772](https://github.com/ApolloAuto/apollo/issues/13772)
- 正在修改robosense激光雷达驱动模块，以支持最新出品的RS-M1激光雷达，首先发现一些点丢失，后来发现是太暗，然后增加强度到255，结果全部不见，将强度降低到0，全部正常显示，询问Apollo是否用低强度值代表高强度，还是说使用函数时出现问题。
- 2021 年 5 月 12 日
- 学习问题


#### [#13770](https://github.com/ApolloAuto/apollo/issues/13770)
- 询问如何将训练好的pointpillars模型转化为Apollo6.0需要的onnx模型，回答中给出了一个教程网址。
- 2021 年 5 月 12 日
- 学习问题
```
https://pytorch.org/tutorials/advanced/super_resolution_with_onnxruntime.html
```

#### [#13715](https://github.com/ApolloAuto/apollo/issues/13715)
- 从代码逻辑看，有两个周长：large_velocity_ratio：2.5，too_large_velocity_ratio：1.5参数貌似设置反了
- 代码位置: modules/perception/production/data/perception/camera/models/omt_obstacle_tracker/config.pt
- 2021 年 4 月 20 日
- 代码问题
```
从字面意思，包括从代码逻辑上推断，这两个参数是否设置反了。
target.cc 中的代码：
if (ratio > target_param_.too_large_velocity_ratio()) { // 1.5
world_center.MagicVelocity(vel);
ADEBUG << "速度太大";
} else if (ratio > target_param_.large_velocity_ratio()) { // 2.5
vel(0) = (x(2) + vel(0)) / 2;
速度（1）=（x（3）+速度（1））/ 2；
world_center.MagicVelocity(vel);
ADEBUG << "速度大";
} else {
ADEBUG << "速度正常";
}
```

#### [#13653](https://github.com/ApolloAuto/apollo/issues/13653)
- 通过激光雷达检测障碍物，如果树在路边，激光雷达是否将树叶识别为障碍物，如果是如何过滤。   
- 2021 年 4 月 2 日
- 学习问题




