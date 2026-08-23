---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

**I am applying for a Ph.D. program to further my research. My research interests include artificial intelligence and computer vision.** I completed my Master's degree at South China University of Technology (SCUT), where I was supervised by **[Prof. Wenxiong Kang](https://www.scholat.com/auwxkang)** and collaborated with **[Dr. Junduan Huang](https://www.scholat.com/junduanhuang)**. My master's research focused on **biometrics, computer vision, and neural network compression**. 

<!-- I have published 2 papers at the IEEE Transactions <a href='https://scholar.google.com/citations?user=GYHA_S8AAAAJ&hl=zh-CN'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>, co-operated with **[Dr. Junduan Huang](https://www.scholat.com/junduanhuang)**. -->

Prior to my master's studies, I received my Bachelor's degree in Automation from South China University of Technology in 2021. During my undergraduate years, I worked on intelligent edge devices under the guidance of **[Dr. Xiaoyan Deng](https://ieeexplore.ieee.org/author/37086300159)**.


# 📖 Educations
- *2021.09 - 2024.06*, Master of Electronic Information in School of Automation Science and Engineering, SCUT, Guangzhou. GPA: 3.62 / 4.0.
- *2017.09 - 2021.06*, Bachelor of Automation in School of Automation Science and Engineering, SCUT, Guangzhou. Direct Postgraduate Admission. Direct Master's Admission (Exam-Exempt).


# 💼 Projects
## Hip‑Assist Exoskeleton
- **Assistive torque curve optimization.** Lower-limb exoskeletons suffered from mismatched assistance and unnatural motion during gait transitions. We designed a start-stop gating mechanism and leveraged the hip-joint motion angle difference to adaptively tune the assistive torque curve. Then, improved assistance coordination and reduced wearer effort by **[XX%]**.
- **Gait-adaptive AI algorithm.** Developed and optimized a gait-adaptive AI algorithm that automatically adjusts assistance in real time to the user's walking pattern. Increased gait-adaptation accuracy / smoothness by **[XX%]**.
- **Scene-adaptive recognition.** Tuned scene-adaptive recognition algorithms to robustly identify terrains and environments across varying scenarios. Boosted recognition accuracy in unseen scenarios from **[XX%]** to **[YY%]**.

<!-- 中文对照
- **助力曲线优化。** *[背景]* 下肢助力外骨骼在步态切换时存在助力不匹配、运动不自然的问题。 *[任务/行动]* 设计了启停门控机制，并利用髋关节运动角度差自适应调优助力曲线。 *[结果]* 改善了助力协调性，使穿戴者费力降低 **[XX%]**。
- **步态自适应AI算法。** *[任务/行动]* 开发并优化了一种步态自适应AI算法，可依据用户行走姿态实时自动调整助力。 *[结果]* 步态自适应准确率/流畅度提升 **[XX%]**。
- **场景自适应识别。** *[任务/行动]* 调优场景自适应识别算法，以在不同场景下稳健识别地形与环境。 *[结果]* 未知场景识别准确率由 **[XX%]** 提升至 **[YY%]**。 -->


## Neural Network Compression and Finger Vein(FV) Authentication
- **CNN Pruning for FV Authentication.** FV authentication CNNs suffer from large parameter counts, high computational cost, and feature-embedding corruption under conventional pruning. Designed a structured pruning method tailored to FV CNNs: (1) proposed an **Embedding Protection layer (EP)** to isolate pruned layers from the output embedding, keeping the feature dimension unchanged; (2) used filter importance evaluation to remove redundant filters; (3) applied an **improved ADMM (Alternating Direction Method of Multipliers)** for deep alternating optimization; (4) retrained the network to recover performance. Params and FLOPs dropped by over 50%; on 9 public datasets, pruned DenseNet121-EP via PCFV achieved a weighted-average EER as low as 0.82%.
- **ViT Pruning for FV Authentication.** FV ViTs are parameter-heavy and computationally expensive. Compressed the FV ViT with minimal accuracy loss: (1) pretrained a FV Transformer; (2) built a **dependency graph** to group network components; (3) evaluated group-norm importance and pruned redundant attention heads and feed-forward networks at the group level; (4) fine-tuned with a small learning rate. Params and FLOPs were substantially reduced with only slight accuracy loss, yielding a lightweight Transformer-based FV model.
- **3D FV Reconstruction.** 2D FV recognition is vulnerable to finger pitch and axial rotation. Reconstructed textured 3D finger models from three views, solving cross-sections via ellipse-prior constrained optimization, stitching them into a 3D finger shape, and fusing multi-view textures with region-weighted mapping. Cross-section fitting error ranged 0.1317–0.3674; on the reconstructed unwrapped image, EER for multi-pose data dropped from 22.32% to 6.64%.

<!-- 中文对照 -->
<!-- - **指静脉认证网络CNN剪枝。** *[背景]* 指静脉认证CNN参数量大、计算开销高，且传统剪枝会破坏特征嵌入维度、适配性差。 *[任务/行动]* 设计适配指静脉认证CNN的结构化剪枝方法：①提出**嵌入保护层EP**，隔离剪枝层与输出嵌入，保证剪枝后特征维度不变；②使用滤波器重要性评估筛选冗余滤波器；③采用**改进ADMM交替方向乘子法**做深层次交替优化；④重训练网络恢复性能。 *[结果]* 参数量、FLOPs下降50%以上；9个公开数据集上，DenseNet121-EP经PCFV剪枝后加权平均EER低至0.82%，优于L1-Prune、FPGM-Prune等经典剪枝算法，适合边缘设备部署。 -->
<!-- - **指静脉认证网络ViT剪枝。** *[背景]* ViT参数量大、计算成本高。 *[任务/行动]* 在尽量少损失精度前提下对指静脉ViT剪枝压缩：①预训练指静脉Transformer模型；②构建**依赖图**梳理组件依赖并分组；③按组范数评估重要性，组级别剪枝冗余注意力头与前馈网络；④小学习率重训练微调。 *[结果]* 参数量、FLOPs大幅削减，仅带来轻微识别性能损失，实现Transformer指静脉模型轻量化。 -->
<!-- - **三维指静脉重建。** *[背景]* 二维指静脉识别易受手指俯仰、轴向旋转影响。 *[任务/行动]* 利用三视角图像重建带静脉纹理的手指三维模型，以椭圆为先验做约束优化求解截面，拼接得到三维指形，分区域加权融合多视角纹理完成手指纹路映射。 *[结果]* 截面拟合误差0.1317–0.3674；重建展开图识别中，多位姿数据EER从22.32%降至6.64%。  -->


## Mathematical Modeling
- **System fuel mass balance model.** Proposed a system-level fuel mass balance model to characterize the mass variation relationship within the high-pressure oil pipe.
- **Needle-valve motion and flow-area modeling.** Modeled the relationship between needle-valve motion and fluid flow area to solve for the cam angular velocity and the injector opening/closing timing.
- **Monte Carlo-based volume integration.** Solved the total fuel volume discharged from the injector via nonlinear integration based on the Monte Carlo method.

<!-- 中文对照 -->
<!-- - **系统燃油质量衡算模型。** 提出系统级燃油质量衡算模型，以表征高压油管内质量变化关系。 -->
<!-- - **针阀运动与流体面积建模。** 建模针阀运动与流体面积的关系，用于求解凸轮角速度与喷油嘴开关时间。 -->
<!-- - **基于蒙特卡洛的体积积分。** 基于蒙特卡洛法，通过非线性积分求解喷油嘴流出的燃油总体积。 -->


# 📝 Publications 

## Biometrics
- "FV-Prune: CNN Compression Based on Network Pruning for FV Authentication." (**<u>Draft</u>**) **<u>Zheng, A. </u>** et al.

- "FVFSNet: Frequency-spatial coupling network for FV authentication." Huang, J., **<u>Zheng, A.</u>**, Shakeel, M. S., Yang, W., & Kang, W. (2023). [[link]](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=GYHA_S8AAAAJ&citation_for_view=GYHA_S8AAAAJ:9yKSN-GCB0IC)

- "FVT: FV transformer for authentication". Huang, J., Luo, W., Yang, W., **<u>Zheng, A.</u>**, Lian, F., & Kang, W. IEEE Transactions on Instrumentation and Measurement. (2022) [[link]](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=GYHA_S8AAAAJ&citation_for_view=GYHA_S8AAAAJ:d1gkVwhDpl0C)


# ⚙️ Academic Activities
- Reviewer for IEEE Signal Processing Letters.


# 🎖 Honors and Awards

**Competition Awards** 
- Second Prize in the Challenge Cup Technology Competition at SCUT, Full-View 3D FV High-Security Identification System.

- National First Prize in the College Students Mathematical Contest in Modeling, [report](https://github.com/Sahala08/CUMCM2019-A/blob/master/docs/A201919002111.pdf), [code](https://github.com/Sahala08/CUMCM2019-A).

- National Second Prize in the NXP Cup College Students Intelligent Car Competition, [our car](/images/Intelligent_Vehicle.jpeg).

**Scholarship** 
- Goodix Technology Scholarship
- Postgraduate Scholarship
- Hongping-Changqing Fund Scholarship ✖ 2
- Innovation Cultivation Fund-Scholarship in School of Automation Science and Engineering

# 💻 Skills
- Familiar with deep learning algorithms, including deep feature extraction and neural network compression algorithms.
- Familiar with Python, C/C++, and PyTorch, experienced in developing deep learning algorithms on Linux.
- Familiar with the basic knowledge of intelligent devices.
# ☘️ Social Practice Experience
- *2023.09 - 2024.01*, [Momenta](https://www.momenta.cn/ch/), Guangzhou, software engineer for Autonomous Driving System.
<!-- L2 Level Mass Production Autonomous Driving System-->
<!-- - 2025.07-now, Algorithm Engineer - Exoskeleton Robotics, in [LEQI](https://www.lqwheel.com/). -->
- 2018, 2019, and 2020, Outstanding Volunteer in Shantou Winter Vacation Social Practice for High School Promotion (Alma Mater Visit Campaign), responsible for organization and promotion.


<!-- 还差：1、绩点  2、助力算法各种算法指标  3、陶瓷的语音方向、efficient ai方向的总结 -->