# 周苓萱

**重庆邮电大学 · 2028 届本科｜嵌入式 Linux · 端侧 AI · 机器人软件**

> RDK Ecosystem Development Intern @ D-Robotics｜Developer Ecosystem Department
>
> RDK X5 机器人实机集成、X5/S100/S600 算法适配与开发者生态交付｜2026.08–至今

## 实习与近期工作

机器鸭项目更新于 **2026-10-23**（其余项目保留各自记录日期）。目前在地瓜机器人（D-Robotics）开发者生态部实习，主要工作为机器鸭实机集成、Roboto Origin 算法适配、课程样例交付及生态技术支持。

### 重点项目：RDK X5 Duck主线｜机载短距离前进取得突破

以 [Pollen Robotics 开源 MicroDuck](https://github.com/pollen-robotics/microduck) 为原型，复用 [机械行者Robo / fanhao375 的飞特版结构](https://github.com/fanhao375/microduck-replica-cad)，在团队支持下由我主导 RDK X5 + HD1910M 实体原型的方案选型、装配、软件控制与实机验证。原版使用 RK3566 与 XL330；更换计算平台和执行器后，需要重新核对总线、关节映射、IMU 坐标及承重跟随。

- **选型与整机**：协调物料和打印，处理托架、脚踝及舵盘装配问题；完成 15 舵机整机装配、编号、方向检查和站姿记录。
- **软件与排障**：打通 X5、微雪 Bus Servo Adapter (A) 和 JY901S IMU 链路，在 X5 跑通原策略 CPU 推理；比较相同目标在悬空与落地时的实际跟随，调整右腿总线支路，开发可逐轮记录参数的本机微调台。
- **突破性进展 · 2026-10-23**：RDK X5、微雪小板和电池全部安装到鸭子本体后，实现短距离前进，展示末段保持站立。完成从9月桌面外接短步、10月机载站立，到当前机载前进的跨越；这组现场微调配置已保存为默认并独立备份。
- **工程积累与开源**：持续迭代轻量化安装结构、负载布局、关节跟随和起停衔接；微调台将启动角、走动角与提前收颈时机独立设置。[最新完整视频与正侧实拍](https://github.com/Xiaomiju-x/rdk-x5-microduck/tree/main/progress/2026-10-23)、[控制模块与冻结参数](https://github.com/Xiaomiju-x/rdk-x5-microduck/tree/main/progress/2026-10-23/control)、[失败案例与复盘](https://github.com/Xiaomiju-x/rdk-x5-microduck/blob/main/PITFALLS.md)、[地瓜社区连续记录](https://forum.d-robotics.cc/t/topic/35728)持续更新。

本次实拍使用D历史目标片段＋11号颈根分段定角与提前收颈，自动前后倾反馈关闭，不混称为全身实时RL闭环成果。约13秒视频前段是短距离前进、后段是机载硬件展示；更长距离和重复起停稳定性继续优化。V2与硬件同事推进机内电控与电源集成，不继续外挂。

**两条副线围绕主线独立推进：**

- **陆吾 XGO-Duck / Arduino UNO Q**：完成独立整机装配、15轴标定、站立及短程行走现场验证，用于机械装配、控制链路和步态部署对照；直线保持、转向与抗扰继续验证。复用[陆吾官方硬件](https://github.com/LuwuDynamics/xgoduck_hardware)与[运行框架](https://github.com/LuwuDynamics/xgoduck_runtime_arduino)，不把其零位或实机结果直接等同RDK成果。
- **南瓜鸭 / 数字瓜园**：围绕主题打印装配、互动机构与数字场景展开；Web、Godot、MuJoCo及UE5可玩版已有阶段交付，实体装配与互动联调继续推进，仿真与实机进度分别记录。

[三线进度与验证范围](https://github.com/Xiaomiju-x/rdk-x5-microduck/blob/main/progress/2026-10-23/README.md) · [后续路线](https://github.com/Xiaomiju-x/rdk-x5-microduck/blob/main/ROADMAP.md)

### 实习项目：Roboto Origin × RDK X5 / S600

参与地瓜机器人公司领导牵头的萝博头正式项目，以实习生身份负责相关算法研发、适配与验证。复用团队已验证的 X5 官方行走、舞蹈底座，外挂 S600 承担高层感知与多模态推理，面向开发者展示 RDK 生态能力。

- **三模块实机接入**：Astra Pro 深度相机、STL-19P 激光雷达、M260C 麦克风完成联合采集；两分钟真实相机分割约 19.2 FPS，雷达 1189 圈、49914 个 CRC 正确包、0 CRC 错误候选。
- **S600 核心算力**：在 BPU 跑通 YOLO11x-Seg、Qwen3-VL-2B 场景问答与 Whisper-medium 通用中文转写；四核四实例固定图片回放合计 217.64 次/秒，约为单实例的 3.92 倍，不等同四台相机帧率。
- **RTX 5090 开发链**：完成真实 CUDA 浮点验证和官方十输出 ONNX 导出，10/10 张量数值检查通过；在线演示仍在 S600 执行，没有新增训练或个人声音训练。
- **开源交付**：2026 年 9 月 30 日已公开[源码、模型来源与部署步骤](https://github.com/Xiaomiju-x/roboto-origin-rdk-x5-s100/tree/main/apps/s600_coprocessor)、[阶段结果](https://github.com/Xiaomiju-x/roboto-origin-rdk-x5-s100/blob/main/docs/S600_COPROCESSOR_DEMO.md)，[发布 CI 通过](https://github.com/Xiaomiju-x/roboto-origin-rdk-x5-s100/actions/runs/36696623882)。网页演示支持真实场景问答和 5 秒麦克风录音→转写→图片问答。

当前是可运行的外挂算法原型，不是自主导航验收：RGB/深度及相机—雷达标定、现场语音准确率和长期稳定性仍待验证；算法演示不下发机器人运动指令。

### 其他实习工作

- **[RDK 课程与样例](https://github.com/D-Robotics/rdk-course-demos)**：交付显示、GPIO/PWM、UART/I²C、SPI、CAN 双语课程与实机演示。9 月新增交付 10 条中英文成片，配套课件已提交组织仓库；[CAN 课程贡献](https://github.com/D-Robotics/rdk-course-demos/commit/0ce864e93e8eaed061cebff69023e732961ea03e)分别记录 X5 内部回环和 S100 MCU 扩展板物理回环，不将两者混称。
- **生态技术支持**：围绕相机、多媒体、BPU 并发、启动介质及 MCU 接口进行复现或日志分析，提供公开诊断建议与必要的研发转交依据。代表答复：[BPU 并发](https://forum.d-robotics.cc/t/topic/35643/6)、[NAND 启动参数排查](https://forum.d-robotics.cc/t/topic/35730/22)。已回复、已定位和已修复分别记录。

## 个人扩展探索

- **[RDK Frontier Lab](https://github.com/Xiaomiju-x/rdk-frontier-lab)｜首版完成，当前未持续维护**：基于公司 RTX 5090 平台、RDK S600/S100/X5 及官方模型开展的自主算法扩展与部署探索，不属于主要实习交付。公开首版包含 CLI、数据与结果合同、74 项测试和跨平台 CI；仓库保留工具与历史研究快照，目录条目不等于成功部署模型数。详见 [v0.1.0](https://github.com/Xiaomiju-x/rdk-frontier-lab/releases/tag/v0.1.0)。

## 竞赛项目

- [双 RDK X5 材料合成 AI 预测与多机具身实验助理机器人](https://github.com/Xiaomiju-x/dual-rdk-x5-materials-ai-robot-lab)
- [RootScope｜RDK X5 固定式根区灌溉舱](https://github.com/Xiaomiju-x/RootScope-AdventureX2026)
- [Lab-Sentinel｜GD32H759 边缘 AI 烧结安全哨兵](https://github.com/Xiaomiju-x/Lab-Sentinel-CIMC2026)
- [Memory ATE/PAT Platform｜存储芯片自动化测试平台](https://github.com/Xiaomiju-x/memory-ate-pat-platform)
- [自主散料搬运机器人｜Jetson Orin Nano Super 视觉导航上位机](https://github.com/Xiaomiju-x/intelligent-vision-logistics-crane-2026)

