## 简介
这个组件主要是用于利用unity本身的物理系统，在相机定位过程中 对相机的位置进行修正

---
### 常用参数介绍
[官方文档](https://docs.unity.cn/Packages/com.unity.cinemachine@2.8/manual/CinemachineCollider.html)

---
### 进阶解析 请先熟悉官方文档对各个参数的解释

在物理处理过程中 本质上也是对原本的位置（在cinemachine核心流水线处理过后的位置） 依据设置的参数 **一步步**进行修正

#### Strategy 这是修正过程的第一步
官方文档中解释这个用于控制 collider 如何执行避障
> **pull camera forward**
> > 这种策略时 cinemachine会通过从lookat点朝相机所在位置打一根射线 射线的hit点将直接作为 这一步（strategy）的最终位置
