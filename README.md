# 美军舰船语义分割数据集 (US Navy Ship Segmentation Dataset)（USNSSD）

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC BY--NC 4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

![image-20260319105753914](C:\Users\LC922\AppData\Roaming\Typora\typora-user-images\image-20260319105753914.png)

## 📖 项目介绍

本项目提供了一个高精度的**美国海军舰船语义/实例分割数据集**。与传统的矩形框检测不同，本数据集提供了像素级的轮廓标注，能够更准确地分离舰船与背景（如海面、天空）；同时大部分图片选取了相对较低的视角，以满足特殊场景的需要。

该数据集适用于：

- **美军舰船识别与轮廓提取**
- **USV/UUV 视觉导航与避障**
- **合成孔径雷达 (SAR) 与光学图像的融合研究**

## 📊 数据集统计

- **图像总量：** 1496张
- **标注实例：** 1539个多边形
- **标注格式：** MS COCO 格式 (`.json`)

### 🏷️ 类别映射 (Category Mapping)

| 类别 ID | 英文名称            | 中文名称     | 数量 |
| ------- | ------------------- | ------------ | ---- |
| `0`     | Nimitz class        | 尼米兹级     | 240  |
| `1`     | Ford class          | 福特级       | 73   |
| `2`     | Arleigh Burke class | 阿利伯克级   | 277  |
| `3`     | Freedom class       | 自由级       | 109  |
| `4`     | Independence class  | 独立级       | 141  |
| `5`     | Ticonderoga class   | 提康德罗加级 | 230  |
| `6`     | San Antonio class   | 圣安东尼奥级 | 273  |
| `7`     | Wasp class          | 黄蜂级       | 101  |
| `8`     | Zumwalt class       | 朱姆沃特级   | 40   |
| `9`     | America class       | 美国级       | 55   |

![img](https://ncnhd3ekd3wp.feishu.cn/space/api/box/stream/download/asynccode/?code=MzNjMjNhNzhhMGE1MTI0Mzk1NjNjOGZhY2MzZDUyYWNfZjZxaEtwUENFN2czNU5wNUI3UDBHTGYzVnRWY3BoS1hfVG9rZW46V0R3cmJTbXZYb0JIdVl4bEhDSmM4V1lHblFmXzE3NzM4ODgwMTY6MTc3Mzg5MTYxNl9WNA)

## 📂 目录结构 (COCO 格式)

本数据集遵循标准的 **COCO 2017** 目录结构，方便直接使用 `pycocotools` 或 `MMDetection` 加载。

```Plain
USNSD_COCO/
├── images/
│   ├── train2017/      # 训练集原图
│   └── val2017/        # 验证集原图
├── annotations/
│   ├── instances_train2017.json  # 训练集标注 
│   └── instances_val2017.json    # 验证集标注
└── README.md
```

## 📜 License / 许可协议

This dataset is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

**Summary in Plain English:**

1. **You are free to:** Share and Adapt the data.
2. **Under the following terms:**
   1. **Attribution:** You must give appropriate credit to the author (cite this repository).
   2. **NonCommercial:** You may not use this material for commercial purposes.

**中文简述：**

本数据集遵循 [CC BY-NC 4.0 协议](https://creativecommons.org/licenses/by-nc/4.0/)。

您可以自由地分享、修改和使用本数据集，但必须遵守以下条件：

1. **署名：** 在您的文章或项目中引用本项目。
2. **非商业使用：** 严禁将本数据集用于任何商业用途（如售卖、商业模型训练等）。