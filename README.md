# Eco-sight: 自动驾驶智能视觉感知 🍀 

Eco-sight 项目是一个致力于自动驾驶的智能视觉感知系统。项目团队深入学习和实践了数据集的选择与制作、YOLO 模型的训练以及智能帧率调节，以确保在各种驾驶环境下实现快速而准确的目标检测。

## 目录
- [项目简介](#项目简介)
- [数据集选择与处理](#数据集选择与处理)
- [功能实现](#功能实现)
- [项目结果展示](#项目结果展示)
- [挑战与提升](#挑战与提升)
- [Q&A](#q-a)
- [贡献者](#贡献者)

## 项目简介

随着新能源汽车在中国的快速普及，预计到 2025 年，新能源汽车的渗透率将趋于 40%。自动驾驶技术的发展对于推动这一转变至关重要。Eco-sight 项目通过采用深度学习和人工智能技术，提高了自动驾驶汽车的安全性和效率。

本项目积极响应“碳达峰碳中和”的国家战略，通过优化算法和提升能效，减少能源消耗，降低碳排放，为实现绿色低碳的智能交通系统做出贡献。

## 数据集选择与处理

本项目使用了多种自动驾驶数据集，并最终选择了 **nuScenes** 数据集。以下是数据集的分析对比：

| 数据集  | 优点 | 缺点 |
|---------|------|------|
| KITTI   | 历史悠久，数据多样 | 数据量小，场景单一，传感器技术较旧 |
| Waymo   | 数据量大，场景多样，传感器数据高质量 | 标注复杂，存在隐私和法律问题，获取限制 |
| nuScenes | 传感器数据全面，场景标注详细 | 数据量相对较小，标注一致性问题 |

**最终选择：nuScenes** 数据集，结合雷达云图与摄像机数据，通过预处理后获得了训练、验证和测试数据集。

![训练结果对比](assets/nuScenes.png)

### 数据预处理流程

- 原始数据：11,584 条
- 处理后数据：8,763 条
- 使用工具：`Python`、`labelimg` 库、`X-AnyLabeling`、`yolo10x`
- 预处理操作包括：手动标注和自动识别 + 人工筛选

![训练结果对比](assets/preprocessing.png)

## 功能实现

### 模型训练

模型基于 YOLO V10 进行训练，适应自动驾驶场景下的实时目标检测需求。训练过程包括：

- 数据集加载与清洗
- YOLO 模型参数优化
- 模型评估与迭代

### 智能帧率调节方法

智能帧率调节旨在通过动态调整模型的帧率和能耗模式，实现系统资源的高效利用。

- **核心逻辑**：根据目标物体数量调整使用的能耗模型（低、中、高）。
- **帧率调整**：
  - 无目标物体时：低能耗模式，节省资源
  - 目标物体 ≤ 3：高能耗模式，快速响应
  - 目标物体 ≥ 3：中等能耗模式，兼顾反应速度与准确性

## 项目结果展示

训练后的模型在多种场景下表现出色，尤其是在实时性和精度上的提升：

- **检测性能对比**：原模型 VS 训练后模型结果对比，展示了在多数情况下，训练后模型能够在不损失精确度的前提下识别更多种物体。
  
![训练结果对比](assets/result_comparison.jpg)

- **性能指标**：
  - 响应时间：平均20-25毫秒，达到行业标准性能。
  - 这一成就不仅展示了我们一定的专业能力，也为我们的技术在实时性和安全性要求极高的自动驾驶应用中提供了有力的支持。
 
![训练结果对比](assets/recognition_system.png)

## 挑战与提升

项目过程中遇到的主要挑战以及对应的提升方案：

1. **环境配置**：确保深度学习框架与硬件环境的兼容性，优化训练速度。
2. **训练日志与图表分析**：通过可视化的日志记录（在图表结果文件夹里），对模型训练过程中的性能变化进行分析和优化。

## Q&A

如果有任何问题，欢迎在此处提出，我们的团队将及时解答。

## 贡献者

- 许焕桦 (组长)
- 慕容元
- 钟子诚
- 刘桸泽
- 江创泓 (组长)

---

**项目链接**：[Eco-sight on GitHub](https://github.com/RichardJiang-collab/Eco-sight/tree/main)

