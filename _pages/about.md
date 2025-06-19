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

I am currently a Research Assistant in the Department of Computing at The Hong Kong Polytechnic University (PolyU). Starting September 2025, I will begin my PhD at PolyU, supervised by [Prof. Lei Zhang](https://www4.comp.polyu.edu.hk/~cslzhang/). Previously, I received my B.Eng. from Harbin Institute of Technology and my M.Sc. from Peking University.

### Research Interests
- **Low-level computer vision**. A major challenge in super-resolution is the uncontrollable artifacts stemming from its intrinsically ill-posed nature. I am particularly interested in how to exploit ***multi-frame information*** to generate higher-quality and controllable outputs from degraded inputs.  
- **Computational Imaging**.I view imaging as a transformation from natural, continuous signals to discrete digital measurements. My focus is on ***how we sample the continuous world*** so that the resulting discrete data still permits faithful reconstruction of the underlying scene. Rethinking the sensing stage in this way can fundamentally reshape downstream processing pipelines such as super-resolution.


# 🔥 News
- *2025-09 | New Start* — I will join **VCLab** at PolyU and work alongside many outstanding PhD students 🎉.

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICCV 2023</div><img src='images/realbsr_eg.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Towards Real-World Burst Image Super-Resolution: Benchmark and Method](https://openaccess.thecvf.com/content/ICCV2023/papers/Wei_Towards_Real-World_Burst_Image_Super-Resolution_Benchmark_and_Method_ICCV_2023_paper.pdf)

Pengxu Wei, **Yujing Sun**, Xingbei Guo, Chang Liu, Guanbin Li, Jie Chen, Xiangyang Ji, Liang Lin

[**Github**](https://github.com/yjsunnn/FBANet) [**Zhihu**](https://zhuanlan.zhihu.com/p/663561967)
- Establish a Real-world Burst SuperResolution benchmark, *i.e*., RealBSR
- Propose a Federated Burst Affinity network to address real-world burst image super-resolution.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arxiv</div><img src='images/DLoRAL_pipeline.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[One-Step Diffusion for Detail-Rich and Temporally Consistent Video Super-Resolution](https://arxiv.org/abs/2506.15591)

**Yujing Sun***, Lingchen Sun* , Shuaizheng Liu, Rongyuan Wu, Zhengqiang Zhang, Lei Zhang  
\* Equal contribution

[**Github**](https://github.com/yjsunnn/DLoRAL)
- Propose a Dual LoRA Learning (DLoRAL) paradigm for Real-VSR.
</div>
</div>

# 🎖 Honors and Awards
- National scholarship at Harbin Institute of Technology. 

# 📖 Educations
- *2021.09 - 2024.06*, Peking University, School of Electronic and Computer Engineering 
- *2017.09 - 2021.06*, Harbin Institute of Technology, School of Computer Science and Technology. 

# 💻 Internships
- *2025.01 - 2025.09*, OPPO, China.
