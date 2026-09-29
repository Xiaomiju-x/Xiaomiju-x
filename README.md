# 周苓萱

**重庆邮电大学 · 2028 届本科｜嵌入式 Linux · 端侧 AI · 机器人软件**

> RDK Ecosystem Development Intern @ D-Robotics｜Developer Ecosystem Department
>
> RDK X5 机器人实机集成、X5/S100/S600 算法适配与开发者生态交付｜2026.08–至今

## 实习与近期工作

更新于 **2026-09-29**。目前在地瓜机器人（D-Robotics）开发者生态部实习，主要工作为机器鸭实机集成、Roboto Origin 算法适配、课程样例交付及生态技术支持。

### 重点项目：RDK X5 MicroDuck 复刻与实机适配

以 [Pollen Robotics 开源 MicroDuck](https://github.com/pollen-robotics/microduck) 为原型，复用 [机械行者Robo / fanhao375 的飞特版结构](https://github.com/fanhao375/microduck-replica-cad)，在团队支持下由我主导 RDK X5 + HD1910M 实体原型的方案选型、装配、软件控制与实机验证。原版使用 RK3566 与 XL330；更换计算平台和执行器后，需要重新核对总线、关节映射、IMU 坐标及承重跟随。

- **选型与整机**：协调物料和打印，处理托架、脚踝及舵盘装配问题；完成 15 舵机整机装配、编号、方向检查和站姿记录。
- **软件与排障**：打通 X5、微雪 Bus Servo Adapter (A) 和 JY901S IMU 链路，在 X5 跑通原策略 CPU 推理；比较相同目标在悬空与落地时的实际跟随，调整右腿总线支路，开发可逐轮记录参数的本机微调台。
- **阶段成果与公开**：2026 年 9 月 29 日取得受控平面短距离行走演示。[完整阶段视频](https://github.com/Xiaomiju-x/rdk-x5-microduck/blob/main/milestone-20260929.mp4)、[失败案例与复盘](https://github.com/Xiaomiju-x/rdk-x5-microduck/blob/main/PITFALLS.md)、[源码和装配记录](https://github.com/Xiaomiju-x/rdk-x5-microduck)已公开，并在[地瓜社区原帖](https://forum.d-robotics.cc/t/topic/35728/3)更新。

最新演示使用已记录的舵机目标片段、11 号颈根实时补偿与缓回站姿，并非在线完整强化学习策略持续行走。约 20 秒视频前段数秒是短步前移，后段展示桌面外挂的 X5、转接板和电源；带载、连续稳定行走及 HD1910M 专用策略训练仍待完成。

### 其他实习工作

- **[Roboto Origin 算法适配](https://github.com/Xiaomiju-x/roboto-origin-rdk-x5-s100)**：参与公司领导牵头的双足机器人项目，负责相关算法。已完成 X5/S100 单板离线部署及 X5/S100/S600 YOLO 真 BPU shadow 验证；近期在 S600 接入真实雷达并完成预训练语义导航网络的 CPU 扫描回放。现场采集到算法结果的联合验收仍在推进，尚未完成自主导航与运动闭环。公开仓库目前保留截至 9 月 2 日的算法版本，近期实机增量尚未同步公开。
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
