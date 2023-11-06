# Awesome-PEFT-VLM
Aim for parameter-efficient fine-tuning (peft) vision model.

A curated list of **causality in computer vision**. Inspired by [awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-Causality-in-CV](https://github.com/Wangt-CN/Awesome-Causality-in-CV).

Please feel free to pull requests or open an issue to add papers.


## Table of Contents

- Type of PEFT for VLM
- 问答型多模态任务
- Grounding多模态任务
- 纯视觉分类
  
### VLM-G
| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Bridging Vision and Language Encoders: Parameter-Efficient Tuning for Referring Image Segmentation | ICCV2023 | 每个stage增加了Bridge模块做视觉文本融合，设计可训练解码器（分层对齐+全局对齐+投影）  |  多模态模型CLIP  |  RefCOCO, RefCOCO+, G-Ref指代分割|

### VLM-QA
| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Vl-adapter: Parameter-efficient transfer learning for vision-and-language tasks. | ICCV2023 | 微调语言部分的block，设计下采样+上采样形式的方案  | 多模态Bart-base/T5-base + CLIP  |  VQA, GQA, NLVR, COCO Cap 图文任务   |

### Vision only

| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Revisiting the Parameter Efficiency of Adapters from the Perspective of Precision Redundancy | ICCV2023 | 对lora和adaformer的参数做量化，进一步减少参数量  | 纯视觉VIT-B模型 | VTAB分类数据集 |
| VL-PET: Vision-and-Language Parameter-Efficient Tuning via Granularity Control | CVPR2022 | 微调语言部分的block，在adapter基础上增加粒度控制的G作为权重激活特征  |   多模态Bart-base/T5-base + CLIP; 对比VL-Adapter   |  VQA, GQA, NLVR, COCO Cap 图文任务 |

| A Unified Continual Learning Framework with General Parameter-Efficient Tuning|  | 纯视觉VIT-B |  Cifar100, ImageNetR分类数据集 |





