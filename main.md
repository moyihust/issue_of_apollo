## Apollo issues

可能的简写：AV（Autonomous Vehicle），AD（Autonomous Driving），

### [#编号](链接)

- （尽量）一句话问题描述
- 一些比较有用的信息（日期，版本信息、操作系统、环境、...）
- 什么类型的问题

问题更详细一点的描述。。。描述。。。描述。。。（不用把社区中全部的讨论都记下来，但是尽量使得关于问题的信息比较全面，方便其他人理解问题是什么样的，或者可能由什么办法解决）

### [#14863](https://github.com/ApolloAuto/apollo/issues/14863)

- 存放release的仓库可能是丢失文件了
- 日期：2023-3-30；
- 代码问题

```bash
~/apollo/docker/build$ sudo ./build_docker.sh -f cyber.x86_64.dockerfile -m build -g cn
```

报错信息如下：(实际上，看上去并不是丢失文件，而是获取该文件需要授权，`401 Unauthorized`)

```
#0 692.5 2023-03-30 05:21:41 (22.3 KB/s) - Connection closed at byte 15384576. Retrying.
#0 692.5 
#0 693.5 --2023-03-30 05:21:42--  (try: 2)  https://objects.githubusercontent.com/github-production-release-asset-2e65be/537699/8eeafe00-7692-11eb-99e2-866ffc7c1394?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20230330%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230330T051009Z&X-Amz-Expires=300&X-Amz-Signature=fbe4c8ad7f57ff47cf3093f95eec13cdfd26e333c2cb3ce3878f9c0d6bb44550&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=537699&response-content-disposition=attachment%3B%20filename%3Dcmake-3.19.6-Linux-x86_64.sh&response-content-type=application%2Foctet-stream
#0 693.5 Connecting to objects.githubusercontent.com (objects.githubusercontent.com)|185.199.109.133|:443... connected.
#0 693.6 HTTP request sent, awaiting response... 401 Unauthorized
#0 693.9 
#0 693.9 Username/Password Authentication Failed.
------
cyber.x86_64.dockerfile:19
--------------------
  17 |     
  18 |     RUN bash /opt/apollo/installers/install_minimal_environment.sh ${GEOLOC}
  19 | >>> RUN bash /opt/apollo/installers/install_cmake.sh
  20 |     RUN bash /opt/apollo/installers/install_cyber_deps.sh ${INSTALL_MODE}
  21 |     RUN bash /opt/apollo/installers/install_llvm_clang.sh
--------------------
```

### [#14861](https://github.com/ApolloAuto/apollo/issues/14861)

- Apollo 8.0部署Paddle3D训练的CenterPoint模型编译报错
- 日期：2023-3-29；版本：8.0；系统：Ubuntu 18.04；编译器：gcc7.5.0；cmake：3.10.2
- 配置问题

按照[https://github.com/PaddlePaddle/Paddle3D/tree/develop/docs/models/centerpoint](https://github.com/PaddlePaddle/Paddle3D/tree/develop/docs/models/centerpoint)部署，执行compile.sh时编译报错

![error](https://user-images.githubusercontent.com/47803962/228524591-67262320-9993-4156-9178-1e3bf844d4d7.png)

![e](https://user-images.githubusercontent.com/47803962/228524621-3676c05b-35fa-42bb-9c54-64d49db3539a.png)

### [#14859](https://github.com/ApolloAuto/apollo/issues/14859)

- 如何调整Apollo 7.0的转弯半径
- 日期：2023-3-28；版本：7.0；模拟器：carla
- 代码问题

在carla模拟器中测试Apollo 7.0，自动驾驶车辆转弯时总是倾向于接近路肩，有没有可能更改配置文件（或者其他方式）来使得自动驾驶汽车转弯时更靠近路的中心？该问题可能与地图、规划、控制模块有关。

### [#14858](https://github.com/ApolloAuto/apollo/issues/14858)

- 是否可以在apollo docker中升级CUDA和TensorRT的版本？
- 日期：2023-3-27；版本：8.0；显卡：RTX 4090；CUDA：11.1；TensorRT：7.2.1
- 代码问题

使用RTX 4090和Apollo 8.0时遇到很多与GPU架构（如sm89、compute_89、nvcc）相关的报错，因此希望可以通过升级到最新版的CUDA和TensorRT尝试解决这些报错。在启动docker之后删除并重新安装CUDA和TensorRT会遇到很多依赖相关的问题，并且高版本的CUDA对于低版本的CUDA不是向后兼容的，因此当升级CUDA时，相应的Apollo中使用的接口也应该更新。Apollo&CUDA&RTX 4090必须具有版本对应的关系，4090无法使用低版本的CUDA，Apollo（暂时）无法使用高版本的CUDA。可以通过升级Apollo来支持更高版本的CUDA的接口。