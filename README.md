# VLM_Attack_Paper_List
[VLM-Attack-Survey-2024] Paper list and projects for VLM attacks
本仓库整理了综述论文 **"Attacks on Vision-Language Models: A Survey and Beyond"** 中提到的相关研究文章及信息。本综述围绕视觉语言模型（VLMs）的攻击与防御方法展开，涵盖了攻击目标、数据操作方法以及相关评估指标。

## 调研范围
- **研究主题**: VLM的攻击分类与防御策略。
- **涉及模型**: 包括 CLIP、BLIP、MiniGPT-4、GPT-4V 等。
- **主要分类**:
  1. **攻击目标**: Jailbreak、Camouflage、Exploitation。
  2. **数据操作方法**: Visual Perturbation、Gradient-Driven Prompts、Human-Like Deceptive Prompts、Typography。
  3. **评估指标**: 转移性、效率、效果。

---

## 核心研究文章列表

| 序号 | 标题                               | 作者            | 目标攻击类型        | 模型           | 发表时间 | 来源       |
|------|------------------------------------|-----------------|---------------------|----------------|----------|------------|
| 1    | **A Study of Visual Perturbations** | Zhao et al.     | Camouflage          | CLIP, MiniGPT-4 | 2024     | NeurIPS    |
| 2    | **Gradient-Driven Prompts**         | Liu et al.      | Jailbreak           | GPT-4          | 2024     | MM         |
| 3    | **Typography Attacks**              | Ma et al.       | Jailbreak           | LLaVA          | 2024     | arXiv      |
| 4    | **Exploitation via Visual Inputs**  | Gao et al.      | Exploitation        | InstructBLIP   | 2024     | ICLR       |

---

## 数据集概览

| 数据集名称           | 年份  | 数据量       | 适用场景              | 是否与安全相关 |
|----------------------|-------|--------------|-----------------------|---------------|
| ImageNet            | 2009  | 14M          | 图像分类             | ✗             |
| MS-COCO             | 2014  | 164K         | 图像描述             | ✗             |
| Realtoxicityprompts | 2020  | 100K         | 仇恨言论检测         | ✓             |
| SafeBench           | 2023  | 500          | 多任务场景测试       | ✓             |

---

## 主要研究贡献
1. **分析了 VLM 攻击的独特特征**，包括与单模态模型的区别。
2. **提出了系统的攻击分类方法**，涵盖不同的目标与数据操作策略。
3. **评估了 VLM 攻击的防御方法**，并探讨未来的研究方向。

---

## 链接
- [项目主页](https://github.com/AobtDai/VLM_Attack_Paper_List)
- [论文地址](https://arxiv.org/abs/XXXXXX)

---

## 贡献方式
欢迎通过 PR 提交相关的研究文章或改进建议。

---

## 许可
本仓库遵循 [MIT License](LICENSE)。
