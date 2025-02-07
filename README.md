
# When Data Manipulation Meets Attack Goals: An In-depth Meta-Survey of Attacks for VLMs

This repository organizes the relevant research papers and information mentioned in the review paper **"When Data Manipulation Meets Attack Goals: An In-depth Meta-Survey of Attacks for VLMs"** The review focuses on the attacks and defense methods for Vision-Language Models (VLMs), covering attack goals, data manipulation methods, and relevant evaluation metrics.

Here, we've summarized existing VLM Attack methods in our survey paper.
[Paper Link](https://arxiv.org/abs/XXXXXX)


If you find some important work missed, it would be super helpful to let me know (adai590@connect.hkust-gz.edu.cn). Thanks!

If you find our survey useful for your research, please consider citing:
(这里放论文的引用)

---
## **Table of Contents**
* [Taxonomy of Attack Goal](#taxonomy-of-attack-goal)
  - [Jailbreak](#jailbreak)
  - [Camouflage](#camouflage)
  - [Exploitation](#exploitation)
* [Attacks based on Data Manipulation Strategy](#attacks-based-on-data-manipulation-strategy)
  - [Visual Perturbation](#visual-perturbation)
  - [Gradient-Driven Prompts](#gradient-driven-prompts)
  - [Human-Like Deceptive Prompts](#human-like-deceptive-prompts)
  - [Typography](#typography)
* [Evaluation Strategies](#evaluation-strategies)
  - [Effectiveness](#effectiveness)
  - [Stealthiness](#stealthiness)
  - [Transferability](#transferability)
  - [Efficiency](#efficiency)


# **Taxonomy of Attack Goal**
## **Jailbreak**
#### **NSFW images**
- **To generate or not? safety-driven unlearned diffusion models are still easy to generate unsafe images ... for now** | [GitHub](https://github.com/OPTML-Group/Diffusion-MU-Attack)
  - Zhang, Yimeng and Jia, Jinghan and Chen, Xin and Chen, Aochuan and Zhang, Yihua and Liu, Jiancheng and Ding, Ke and Liu, Sijia
  - Michigan State University, Intel
  - [ECCV2024]https://arxiv.org/abs/2310.11868
- **Ring-a-bell! how reliable are concept removal methods for diffusion models?** | [Github](https://github.com/chiayi-hsu/Ring-A-Bell)
  - Yu-Lin Tsai, Chia-Yi Hsu, Chulin Xie, Chih-Hsun Lin, Jia-You Chen, Bo Li, Pin-Yu Chen, Chia-Mu Yu, Chun-Ying Huang
  - National Yang Ming Chiao Tung University, University of Illinois at Urbana Champaign, National Yang Ming Chiao Tung University, University of Illinois at Urbana Champaign,University of Chicago, IBM Research, National Yang Ming Chiao Tung University
  - [ICLR2024]https://arxiv.org/abs/2310.10012
- **MMA-diffusion: Multimodal attack on diffusion models** | [Github](https://github.com/cure-lab/MMA-Diffusion)
  - Yijun Yang, Ruiyuan Gao, Xiaosen Wang, Tsung-Yi Ho, Nan Xu, Qiang Xu
  - The Chinese University of Hong Kong, Huawei Singular Security Lab, Institute of Automation, Chinese Academy of Sciences,  Beijing Wenge Technology Co. Ltd
  - [CVPR2024]https://arxiv.org/abs/2311.17516
#### **Hateful Memes**
- **Unsafe diffusion: On the generation of unsafe images and hateful memes from text-to-image models** | [GitHub](https://github.com/yitingqu/unsafe-diffusion)
  - Yiting Qu, Xinyue Shen, Xinlei He, Michael Backes, Savvas Zannettou, Yang Zhang
  - CISPA Helmholtz Center for Information Security, Delft University of Technology
  - [ACM CCS2023]https://arxiv.org/abs/2305.13873
#### **NSFW Text**
- **Are aligned neural networks adversarially aligned?** |
  - Nicholas Carlini, Milad Nasr, Christopher A. Choquette-Choo, Matthew Jagielski, Irena Gao, Anas Awadalla, Pang Wei Koh, Daphne Ippolito, Katherine Lee, Florian Tramer, Ludwig Schmidt
  - Google DeepMind, Stanford, University of Washington, ETH Zurich
  - [NeurIPS2023]https://arxiv.org/abs/2306.15447
- **Figstep: Jailbreaking large vision-language models via typographic visual prompts** | [Github](https://github.com/ThuCCSLab/FigStep)
  - Yichen Gong, Delong Ran, Jinyuan Liu, Conglei Wang, Tianshuo Cong, Anyu Wang, Sisi Duan, Xiaoyun Wang
  - Tsinghua University, Carnegie Mellon University, Zhongguancun Laboratory, National Financial Cryptography Research Center, Shandong Institute of Blockchain, Shandong University
  - [AAAI2025]https://arxiv.org/abs/2311.05608
- **MM-safetybench:A benchmark for safety evaluation of multimodal large language models** | [Github](https://github.com/isXinLiu/MM-SafetyBench)
  - Xin Liu, Yichen Zhu, Jindong Gu, Yunshi Lan, Chao Yang, Yu Qiao
  - Shanghai AI Laboratory, East China Normal University, Midea Group, University of Oxford
  - [ECCV2023]https://arxiv.org/abs/2311.17600
- **Jailbreaking multimodal large language models via shuffle inconsistency** |
  - Shiji Zhao, Ranjie Duan, Fengxiang Wang, Chi Chen, Caixin Kang, Jialing Tao, YueFeng Chen, Hui Xue, Xingxing Wei
  - Beihang University
  - [Arxiv2025]https://arxiv.org/abs/2501.04931
- **White-box multimodal jailbreaks against large vision-language models** | [Github](https://github.com/roywang021/UMK)
  - Ruofan Wang, Xingjun Ma, Hanxu Zhou, Chuanjun Ji, Guangnan Ye, Yu-Gang Jiang
  - FudanUniversity, Shanghai Jiaotong University
  - [ACM MM2024]https://arxiv.org/abs/2405.17894
- **Jailbreak in pieces:Compositional adversarial attacks on multi-modal language models** | 
  - Erfan Shayegani, Yue Dong, Nael Abu-Ghazaleh
  - University of California
  - [ICLR2023]https://arxiv.org/abs/2307.14539
#### **Private Data**
- **Extracting training data from large language models** | [Github](https://github.com/ftramer/LM_Memorization)
  - Nicholas Carlini, Florian Tramer, Eric Wallace, Matthew Jagielski, Ariel Herbert-Voss, Katherine Lee, Adam Roberts, Tom Brown, Dawn Song, Ulfar Erlingsson, Alina Oprea, Colin Raffel
  - Google, Stanford, UC Berkeley, Northeastern University, OpenAI, Harvard, Apple
  - [USENIX2020]https://arxiv.org/abs/2012.07805
- **Va3: Virtually assured amplification attack on probabilistic copyright protection for text-to-image generative models** | [Github](https://github.com/South7X/VA3)
  - Xiang Li, Qianli Shen, Kenji Kawaguchi
  - National University of Singapore
  - [CVPR2024]https://arxiv.org/abs/2312.00057
- **Jailbreaking gpt-4v via self-adversarial attacks with system prompts** | 
  - Yuanwei Wu, Xiang Li, Yixin Liu, Pan Zhou, Lichao Sun
  - Huazhong University of Science and Technology,  Lehigh University
  - [Arxiv2023]https://arxiv.org/abs/2311.09127 

## **Camouflage**
#### **Perceptual Deception**
- **On evaluating adversarial robustness of large vision-language models** | [GitHub](https://github.com/yunqing-me/AttackVLM)
  - Yunqing Zhao, Tianyu Pang, Chao Du, Xiao Yang, Chongxuan Li, Ngai-Man Cheung, Min Lin
  - Singapore University of Technology and Design, Sea AI Lab, Tsinghua University, Renmin University of China
  - [NeurIPS2023]https://arxiv.org/abs/2305.16934
- **Badclip:Dual-embedding guided backdoor attack on multimodal contrastive learning**
  - Siyuan Liang, Mingli Zhu, Aishan Liu, Baoyuan Wu, Xiaochun Cao, Ee-Chien Chang
  - National University of Singapore, The Chinese University of Hong Kong, Beihang University, Sun Yat-sen University-Shenzhen
  - [CVPR2024]https://arxiv.org/abs/2311.12075
- **Badclip: Trigger-aware prompt learning for backdoor attacks on clip** |
  - Jiawang Bai, Kuofeng Gao, Shaobo Min, Shu-Tao Xia, Zhifeng Li, Wei Liu
  - Tsinghua University, Tencent Data Platform, 3Research Center of Artificial Intelligence
  - [CVPR2024]https://arxiv.org/abs/2311.16194
- **Vlattack: Multimodal adversarial attacks on vision-language tasks via pre-trained models** | [Github](https://github.com/ericyinyzy/VLAttack)
  - Ziyi Yin, Muchao Ye, Tianrong Zhang, Tianyu Du, Jinguo Zhu, Han Liu, Jinghui Chen, Ting Wang, Fenglong Ma
  - The Pennsylvania State University, Zhejiang University, Xi'an Jiaotong University, Dalian University of Technology, Stony Brook University
  - [NeurIPS2023]https://arxiv.org/abs/2310.04655
- **An image is worth 1000 lies: Adversarial transferability across prompts on vision-language models** | [GitHub](https://github.com/Haochen-Luo/CroPA)
  - Haochen Luo, Jindong Gu, Fengyuan Liu, Philip Torr
  - University of Oxford,
  - [ICLR2024]https://arxiv.org/abs/2403.09766
- **Break the visual perception: Adversarial attacks targeting encoded visual tokens of large vision-language models** | 
  - Yubo Wang, Chaohu Liu, Yanqiu Qu, Haoyu Cao, Deqiang Jiang, Linli Xu
  - University of Science and Technology, Tencent YouTu lab
  - [ACMMM2024]https://arxiv.org/abs/2410.06699
- **Adversarial illusions in multi-modal embeddings** | [Github](https://github.com/ebagdasa/adversarial_illusions)
  - Tingwei Zhang, Rishi Jha, Eugene Bagdasaryan, Vitaly Shmatikov
  - Cornell University, University of Massachusetts Amherst, Cornell Tech
  - [USENIX2024]https://arxiv.org/abs/2308.11804
#### **Operational Hijacking**
- **Physical backdoor attack can jeopardize driving with vision-large-language models** | [Github](https://github.com/vincentni0107/badvlmdriver)
  - Zhenyang Ni, Rui Ye, Yuxi Wei, Zhen Xiang, Yanfeng Wang, Siheng Chen
  - Shanghai Jiao Tong University, University of Illinois Urbana-Champaign, Shanghai AI Laboratory, Multi-Agent Governance & Intelligence Crew,
  - [Arxiv2024]https://arxiv.org/abs/2404.12916
- **Misusing tools in large language models with visual adversarial examples** | [Github](https://github.com/ZihanWangKi/VLMToolMisuse) 
  - Xiaohan Fu, Zihan Wang, Shuheng Li, Rajesh K. Gupta, Niloofar Mireshghallah, Taylor Berg-Kirkpatrick, Earlence Fernandes
  - University of California San Diego, University of Washington, University of California San Diego
  - [Arxiv2023]https://arxiv.org/abs/2310.03185
## **Exploitation**
- **Inducing high energy-latency of large vision-language models with verbose images** | [Github](https://github.com/KuofengGao/Verbose_Images)
  - Kuofeng Gao, Yang Bai, Jindong Gu, Shu-Tao Xia, Philip Torr, Zhifeng Li, Wei Liu
  - Tsinghua University, Tencent Technology, University of Oxford, Tencent Data Platform, Peng Cheng Laboratory
  - [ICLR2024]https://arxiv.org/abs/2401.11170



# **Attacks based on Data Manipulation Strategy**
## **Visual Perturbation**
- **On the adversarial robustness of multimodal foundation models** | [Github](https://github.com/chs20/robustvlm)
  - Christian Schlarmann, Matthias Hein
  - University of Tubingen 
  - [ICCV2023]https://arxiv.org/abs/2308.10741
- **On evaluating adversarial robustness of large vision-language models** | [Github](https://github.com/yunqing-me/AttackVLM)
  - Yunqing Zhao, Tianyu Pang, Chao Du, Xiao Yang, Chongxuan Li, Ngai-Man Cheung, Min Lin
  - Singapore University of Technology and Design, Sea AI Lab, Tsinghua University,Renmin University of China 
  - [NeurIPS2023]https://arxiv.org/abs/2305.16934
- **Vlattack: Multimodal adversarial attacks on vision-language tasks via pre-trained models** | [Github](https://github.com/ericyinyzy/VLAttack)
  - Ziyi Yin, Muchao Ye, Tianrong Zhang, Tianyu Du, Jinguo Zhu, Han Liu, Jinghui Chen, Ting Wang, Fenglong Ma
  - The Pennsylvania State University, Zhejiang University, Xi'an Jiaotong University, Dalian University of Technology, Stony Brook University
  - [NeurIPS2023]https://arxiv.org/abs/2310.04655
- **Transferable multimodal attack on vision-language pre-training models** | 
  - Haodi Wang, Kai Dong, Zhilei Zhu, Haotong Qin, Aishan Liu, Xiaolin Fang, Jiakai Wang, Xianglong Liu
  - Southeast University, Zhongguancun Laboratory, Data Space Research Institute of Hefei Comprehensive National Science Centre, Beihang University
  - [S&P2024]https://ieeexplore.ieee.org/document/10646738
- **Set-level guidance attack: Boosting adversarial transferability of vision-language pre-training models** | [Github](https://github.com/Zoky-2020/Set-level_Guidance_Attack)
  - Dong Lu, Zhiqiang Wang, Teng Wang, Weili Guan, Hongchang Gao, Feng Zheng
  - Southern University of Science and Technology, The University of Hong Kong, Monash University, Temple University, Peng Cheng Laboratory
  - [ICCV2023]https://arxiv.org/abs/2307.14061
- **Boosting transferability in vision-language attacks via diversification along the intersection region of adversarial trajectory** | [Github](https://github.com/SensenGao/VLPTransferAttack)
  - Sensen Gao, Xiaojun Jia, Xuhong Ren, Ivor Tsang, Qing Guo
  - Nankai University, Nanyang Technological University, CFAR and IHPC
  - [ECCV2024]https://arxiv.org/abs/2403.12445
- **Badclip:Dual-embedding guided backdoor attack on multimodal contrastive learning** | 
  - Siyuan Liang, Mingli Zhu, Aishan Liu, Baoyuan Wu, Xiaochun Cao, Ee-Chien Chang
  - National University of Singapore, The Chinese University of Hong Kong, Beihang University, Sun Yat-sen University-Shenzhen
  - [CVPR2024]https://arxiv.org/abs/2311.12075
- **Advclip:Downstream-agnostic adversarial examples in multimodal contrastive learning** | [GitHub](https://github.com/cgcl-codes/advclip)
  - Ziqi Zhou, Shengshan Hu, Minghui Li, Hangtao Zhang, Yechao Zhang, Hai Jin
  -  Huazhong University ofScience and Technology
  - [ACMMM2023]https://arxiv.org/abs/2308.07026
- **Text-to-image diffusion models can be easily backdoored through multimodal data poisoning** | [Github](https://github.com/sf-zhai/BadT2I)
  - Shengfang Zhai, Yinpeng Dong, Qingni Shen, Shi Pu, Yuejian Fang, Hang Su
  - Peking University,  Tsinghua University
  - [ACMMM2023]https://arxiv.org/abs/2305.04175
- **Vl-trojan: Multimodal instruction backdoor attacks against autoregressive visual language models** | 
  - Jiawei Liang, Siyuan Liang, Man Luo, Aishan Liu, Dongchen Han, Ee-Chien Chang, Xiaochun Cao
  - [Arxiv2024]https://arxiv.org/abs/2402.13851
- **Transferable multimodal attack on vision-language pre-training models** | 
  - Haodi Wang, Kai Dong, Zhilei Zhu, Haotong Qin, Aishan Liu, Xiaolin Fang, Jiakai Wang, Xianglong Liu
  - Southeast University, Zhongguancun Laboratory, Data Space Research Institute of Hefei Comprehensive National Science Centre, Beihang University
  - [S&P2024]https://ieeexplore.ieee.org/document/10646738
## **Gradient-Driven Prompts**
- **MMA-diffusion: Multimodal attack on diffusion models** | [Github](https://github.com/cure-lab/MMA-Diffusion)
  - Yijun Yang, Ruiyuan Gao, Xiaosen Wang, Tsung-Yi Ho, Nan Xu, Qiang Xu
  - The Chinese University of Hong Kong, Huawei Singular Security Lab, Institute of Automation, Chinese Academy of Sciences,  Beijing Wenge Technology Co. Ltd
  - [CVPR2024]https://arxiv.org/abs/2311.17516
- **Arondight: Red teaming large vision language models with auto-generated multi-modal jailbreak prompts** | 
  - Yi Liu, Chengjun Cai, Xiaoli Zhang, Xingliang Yuan, Cong Wang
  - City University of Hong Kong, University of Science and Technology, The University of Melbourne
  - [ACMMM2024]https://arxiv.org/abs/2407.15050
- **Prompt-driven contrastive learning for transferable adversarial attacks** | [Github](https://pdcl-attack.github.io/)
  - Hunmin Yang, Jongoh Jeong, Kuk-Jin Yoon
  - KAIST, ADD
  - [ECCV2024]https://arxiv.org/abs/2407.20657
- **Vlattack: Multimodal adversarial attacks on vision-language tasks via pre-trained models** | [Github](https://github.com/ericyinyzy/VLAttack)
  - Ziyi Yin, Muchao Ye, Tianrong Zhang, Tianyu Du, Jinguo Zhu, Han Liu, Jinghui Chen, Ting Wang, Fenglong Ma
  - The Pennsylvania State University, Zhejiang University, Xi'an Jiaotong University, Dalian University of Technology, Stony Brook University
  - [NeurIPS2023]https://arxiv.org/abs/2310.04655
- **An image is worth 1000 lies: Adversarial transferability across prompts on vision-language models** | [Github](https://github.com/Haochen-Luo/CroPA)
  - Haochen Luo, Jindong Gu, Fengyuan Liu, Philip Torr
  - University of Oxford,
  - [ICLR2024]https://arxiv.org/abs/2403.09766
- **Transferable multimodal attack on vision-language pre-training models** | 
  - Haodi Wang, Kai Dong, Zhilei Zhu, Haotong Qin, Aishan Liu, Xiaolin Fang, Jiakai Wang, Xianglong Liu
  - Southeast University, Zhongguancun Laboratory, Data Space Research Institute of Hefei Comprehensive National Science Centre, Beihang University
  - [S&P2024]https://ieeexplore.ieee.org/document/10646738
## **Human-Like Deceptive Prompts**
- **Jailbreaking gpt-4v via self-adversarial attacks with system prompts** | 
  - Yuanwei Wu, Xiang Li, Yixin Liu, Pan Zhou, Lichao Sun
  - Huazhong University of Science and Technology,  Lehigh University
  - [Arxiv2023]https://arxiv.org/abs/2311.09127 
## **Typography**
- **Figstep: Jailbreaking large vision-language models viatypographic visual prompts** | [Github](https://github.com/ThuCCSLab/FigStep)
  - Yichen Gong, Delong Ran, Jinyuan Liu, Conglei Wang, Tianshuo Cong, Anyu Wang, Sisi Duan, Xiaoyun Wang
  - Tsinghua University, Carnegie Mellon University, Zhongguancun Laboratory, National Financial Cryptography Research Center, Shandong Institute of Blockchain, Shandong University
  - [AAAI2025]https://arxiv.org/abs/2311.05608
- **Visual-roleplay: Universal jailbreak attack on multimodal large language models via role-playing image character** | 
  - Siyuan Ma, Weidi Luo, Yu Wang, Xiaogeng Liu
  - University of Wisconsin-Madison, The Ohio State University, Peking University, University of Wisconsin-Madison
  - [Arxiv2024]https://arxiv.org/abs/2405.20773
- **Jailbreak in pieces: Compositional adversarial attacks on multi-modal language models** | 
  - Erfan Shayegani, Yue Dong, Nael Abu-Ghazaleh
  - University of California
  - [ICLR2023]https://arxiv.org/abs/2307.14539
- **Vision-llms can fool themselves with self-generated typographic attacks** | [Github](https://github.com/mqraitem/Self-Gen-Typo-Attack)
  - Maan Qraitem, Nazia Tasnim, Piotr Teterwak, Kate Saenko, Bryan A. Plummer
  - Boston University
  - [Arxiv2024]https://arxiv.org/abs/2402.00626
- **Empirical analysis of large vision-language models against goal hijacking via visual prompt injection** | 
  - Subaru Kimura, Ryota Tanaka, Shumpei Miyawaki, Jun Suzuki, Keisuke Sakaguchi
  - Tohoku University, NTT Human Informatics Laboratories
  - [NAACL2024]https://arxiv.org/abs/2408.03554

# **Evaluation Strategies**
## **Effectiveness**
- **Figstep: Jailbreaking large vision-language models viatypographic visual prompts** | [Github](https://github.com/ThuCCSLab/FigStep)
  - Yichen Gong, Delong Ran, Jinyuan Liu, Conglei Wang, Tianshuo Cong, Anyu Wang, Sisi Duan, Xiaoyun Wang
  - Tsinghua University, Carnegie Mellon University, Zhongguancun Laboratory, National Financial Cryptography Research Center, Shandong Institute of Blockchain, Shandong University
  - [AAAI2025]https://arxiv.org/abs/2311.05608
- **White-box multimodal jailbreaks against large vision-language models** | [Github](https://github.com/roywang021/UMK)
  - Ruofan Wang, Xingjun Ma, Hanxu Zhou, Chuanjun Ji, Guangnan Ye, Yu-Gang Jiang
  - FudanUniversity, Shanghai Jiaotong University
  - [ACM MM2024]https://arxiv.org/abs/2405.17894
- **MMA-diffusion: Multimodal attack on diffusion models** | [Github](https://github.com/cure-lab/MMA-Diffusion)
  - Yijun Yang, Ruiyuan Gao, Xiaosen Wang, Tsung-Yi Ho, Nan Xu, Qiang Xu
  - The Chinese University of Hong Kong, Huawei Singular Security Lab, Institute of Automation, Chinese Academy of Sciences,  Beijing Wenge Technology Co. Ltd
  - [CVPR2024]https://arxiv.org/abs/2311.17516
- **Are aligned neural networks adversarially aligned?** | 
  - Nicholas Carlini, Milad Nasr, Christopher A. Choquette-Choo, Matthew Jagielski, Irena Gao, Anas Awadalla, Pang Wei Koh, Daphne Ippolito, Katherine Lee, Florian Tramer, Ludwig Schmidt
  - Google DeepMind, Stanford, University of Washington, ETH Zurich
  - [NeurIPS2023]https://arxiv.org/abs/2306.15447
- **Figstep: Jailbreaking large vision-language models via typographic visual prompts** | [Github](https://github.com/ThuCCSLab/FigStep)
  - Yichen Gong, Delong Ran, Jinyuan Liu, Conglei Wang, Tianshuo Cong, Anyu Wang, Sisi Duan, Xiaoyun Wang
  - Tsinghua University, Carnegie Mellon University, Zhongguancun Laboratory, National Financial Cryptography Research Center, Shandong Institute of Blockchain, Shandong University
  - [AAAI2025]https://arxiv.org/abs/2311.05608
## **Stealthiness**
- **On the adversarial robustness of multimodal foundation models** | [Github](https://github.com/chs20/robustvlm)
  - Christian Schlarmann, Matthias Hein
  - University of Tubingen 
  - [ICCV2023]https://arxiv.org/abs/2308.10741
- **Inducing High Energy-Latency of Large Vision-Language Models with Verbose Images** | [GitHub](https://github.com/KuofengGao/Verbose_Images) 
  - Kuofeng Gao, Yang Bai, Jindong Gu, Shu-Tao Xia, Philip Torr, Zhifeng Li, Wei Liu
  - Tsinghua University, Tencent Technology, University of Oxford, Tencent Data Platform,  Peng Cheng Laboratory
  - [ICLR2024]https://arxiv.org/abs/2401.11170
## **Transferability**
#### **Among Tasks**
- **Vlattack: Multimodal adversarial attacks on vision-language tasks via pre-trained models** | [Github](https://github.com/ericyinyzy/VLAttack)
  - Ziyi Yin, Muchao Ye, Tianrong Zhang, Tianyu Du, Jinguo Zhu, Han Liu, Jinghui Chen, Ting Wang, Fenglong Ma
  - The Pennsylvania State University, Zhejiang University, Xi'an Jiaotong University, Dalian University of Technology, Stony Brook University
  - [NeurIPS2023]https://arxiv.org/abs/2310.04655
#### **Among Models**
- **Transferable multimodal attack on vision-language pre-training models** | 
  - Haodi Wang, Kai Dong, Zhilei Zhu, Haotong Qin, Aishan Liu, Xiaolin Fang, Jiakai Wang, Xianglong Liu
  - Southeast University, Zhongguancun Laboratory, Data Space Research Institute of Hefei Comprehensive National Science Centre, Beihang University
  - [S&P2024]https://ieeexplore.ieee.org/document/10646738
#### **Among Inputs**
- **Set-level Guidance Attack: Boosting Adversarial Transferability of Vision-Language Pre-training Models** | [Github](https://github.com/Zoky-2020/Set-level_Guidance_Attack)
  - Dong Lu, Zhiqiang Wang, Teng Wang, Weili Guan, Hongchang Gao, Feng Zheng
  - Southern University of Science and Technology, The University of Hong Kong, Monash University, Temple University, Peng Cheng Laboratory
  - [ICCV2023]https://arxiv.org/abs/2307.14061
## **Efficiency**








