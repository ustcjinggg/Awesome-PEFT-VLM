# Awesome-PEFT-VLM
Aim for parameter-efficient fine-tuning (peft) vision-language model.

A curated list of **causality in computer vision**. Inspired by [awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-Causality-in-CV](https://github.com/Wangt-CN/Awesome-Causality-in-CV).

Please feel free to pull requests or open an issue to add papers.


## Table of Contents

- Type of PEFT for VLM
- 多模态QA任务
- 多模态Visual任务
- 纯视觉模型
- 纯语言模型
  
### VLM-Visual-Task
| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Bridging Vision and Language Encoders: Parameter-Efficient Tuning for Referring Image Segmentation | ICCV2023 | 每个stage增加了Bridge模块做视觉文本融合，设计可训练解码器（分层对齐+全局对齐+投影）  |  多模态模型CLIP  |  RefCOCO, RefCOCO+, G-Ref指代分割|
| Multi-modal Queried Object Detection in the Wild | NIPS2023 |  固定模型，增加视觉query分支，并将query融入文本编码器做cross-att |  多模态定位模型GLIP(Swin+Bert+Dyhead)  |  COCO, ODinW, LVIS数据集 目标检测  |
| Self-regulating Prompts: Foundational Model Adaptation without Forgetting | ICCV2023 |  结合可学习的prompt和定制的loss学习task-agnostic和task-speicifc信息  |  CLIP-ViT-B16  |  FGVC分类数据集 |

### VLM-QA
| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Vl-adapter: Parameter-efficient transfer learning for vision-and-language tasks. | ICCV2023 | 改造文本部分的block，设计下采样+上采样形式的方案设计adapter  | 多模态Bart-base/T5-base + CLIP  |  VQA, GQA, NLVR, COCO Cap 图文任务   |
| VL-PET: Vision-and-Language Parameter-Efficient Tuning via Granularity Control | CVPR2022 | 改造文本部分的block，在adapter基础上增加粒度控制的G作为权重对特征激活  |  多模态Bart-base/T5-base + CLIP; 对比VL-Adapter |  VQA, GQA, NLVR, COCO Cap 图文任务 |
| LST: Ladder Side-Tuning for Parameter and Memory Efficient Transfer Learning | NIPS2022 | 设计侧边网络，由本身参数初始化，微调过程中固定主干网络并且无需其中梯度，节省50%以上显存 | T5, CLIP-T5 | GLUE NLP任务; VQA, GQA, NLVR, COCO Cap 图文任务 |
| Tem-adapter: Adapting Image-Text Pretraining for Video Question Answer |  ICCV2023 | 在视觉和文本编码器对齐处，使用transformer层进行对齐 | CLIP-ViT-B32模型 | SUTD-TrafficQA (Video) |

### Vision Only

| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| Visual Prompt Tuning | ECCV2022(455引) |  固定模型，在每一层都增加可学习的prompt作为额外token进行训练  |  ViT-B, ViT-L | VTAB分类数据集 |
| Revisiting the Parameter Efficiency of Adapters from the Perspective of Precision Redundancy | ICCV2023 | 对lora和adaformer的参数做量化，进一步减少参数量  | 纯视觉VIT-B模型 | VTAB分类数据集 |
| Sensitivity-Aware Visual Parameter-Efficient Fine-Tuning | ICCV2023 | 利用梯度分析不同层的参数敏感性，依次使用LoRA | 纯视觉VIT-B模型 | VTAB分类数据集 |
| A Unified Continual Learning Framework with General Parameter-Efficient Tuning | ICCV2023| 叠加使用lora,prefix,adapeter设计了PET模块 | 纯视觉VIT-B |  Cifar100, ImageNetR分类数据集 |
| DiffFit: Unlocking Transferability of Large Diffusion Models via Simple Parameter-Efficient Fine-Tuning | ICCV2023 |  打开bias, bn, class token, 加入可学习γ用作block权重 |  Diffusion Transformer(DiT) | Food101等细粒度数据集做生成 |


### Language Only
| Title | 发表情况 | 方法描述 | 基线模型 | 实验对象 |
|:--------------- |:-------:|:----------:|:-------:|:-----------:|
| LoRA: Low-rank adaptation of large language models| ICLR2022(1k+引) | 用低秩逼近的方法拟合模型微调过程中W的变化 | DeBERTa, GPT-2, GPT-3 | WikiSQL,MultiNLI等 |
| BitFit: Simple Parameter-efficient Fine-tuning for Transformer-based Masked Language-models | ACL2022(360引) | 仅微调bias项 | Bert 模型 | GLUE benchmark |
| Parameter-efficient Multi-task Fine-tuning for Transformers via Shared Hypernetworks | ACL2021(150引) | - | T5-base | GLUE benchmark |





