# Awesome-PEFT-VLM
Aim for parameter-efficient fine-tuning (peft) vision model.

A curated list of **causality in computer vision**. Inspired by [awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-Causality-in-CV](https://github.com/Wangt-CN/Awesome-Causality-in-CV).

Please feel free to pull requests or open an issue to add papers.


## Table of Contents

- [Type of PEFT for VLM]
- [ICCV 2023 Venues](#iccv2023)



### iccv2023

| Title | 方法 | 模型 | 实验对象 |
|:-------------------------------------------------------------------------------------------------------------------------------- |:-----:|:-------:|:----:|
| Revisiting the Parameter Efficiency of Adapters from the Perspective of Precision Redundancy |  对lora和adaformer的参数做量化，进一步减少参数量  | 纯视觉VIT-B模型  | VTAB分类数据集   |
| VL-PET: Vision-and-Language Parameter-Efficient Tuning via Granularity Control |     |   多模态Bart-base,T5-base   |  VQA, GQA, NLVR, COCO Cap 图文任务 |
| [Learning Causal Representation for Training Cross-Domain Pose Estimator via Generative Interventions](https://openaccess.thecvf.com/content/ICCV2021/papers/Zhang_Learning_Causal_Representation_for_Training_Cross-Domain_Pose_Estimator_via_Generative_ICCV_2021_paper.pdf) | ICCV | `IT/CR`     | -  |

### cvpr2022
| Title | 方法 | 模型 | 实验对象 |
|:-------------------------------------------------------------------------------------------------------------------------------- |:-----:|:-------:|:----:|
| Vl-adapter: Parameter-efficient transfer learning for vision-and-language tasks. |  对lora和adaformer的参数做量化，进一步减少参数量  | 多模态  |  VQA, GQA, NLVR, COCO Cap 图文任务   |



