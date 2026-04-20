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

Hello~ I am Xinyi, a Ph.D. candidate at University College London (UCL), luckily supervised by [Prof. Jing-Hao Xue](http://www.homepages.ucl.ac.uk/~ucakjxu/). Before that, I received my master's degree with honors from Xiamen University (XMU), fortunately supervised by [Dr. Yang Lu](https://jasonyanglu.github.io/).

You can reach me at <a href="mailto:xinyi.shang.23@ucl.ac.uk">xinyi.shang.23@ucl.ac.uk</a>, or find my publications on <a href='https://scholar.google.com/citations?hl=zh-CN&user=pkfBYHAAAAAJ'>Google Scholar</a> <a href='https://scholar.google.com/citations?hl=zh-CN&user=pkfBYHAAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>.


# 🔥 News
- *2026.04*: &nbsp;📄 We release a technical report *"A Systematic and Comprehensive Analysis of Claude Code"*. [[paper]](https://github.com/VILA-Lab/Dive-into-Claude-Code)
- *2026.02*: &nbsp;🎉 Two papers are accepted by **CVPR 2026**.
- *2025.09*: &nbsp;Started as a **visiting student** at MBZUAI, supervised by [Prof. Zhiqiang Shen](https://zhiqiangshen.com/).
- *2023.05*: &nbsp;🎉 Received the **Outstanding Master Thesis** Award.
- *2023.03*: &nbsp;🎉 Received the PhD offer from **University College London (UCL)**, supported by full scholarship!
- *2022.11*: &nbsp;Started a research internship at Westlake University, supervised by [Prof. Tao Lin](https://tlin-taolin.github.io/).
- *2022.09*: &nbsp;Awarded the China National Scholarship.
- *2022.04*: &nbsp;One IJCAI paper is accepted.
- *2022.03*: &nbsp;One ICME paper is accepted as oral.

# 🎯 Research Interests

My research centers on **generalized** and **efficient** deep learning. Numbers in brackets link to the corresponding entries in [Publications](#-publications) below.

- **Deep Learning Under Imperfect Data — Federated Learning (FL).** A privacy-preserving distributed framework that lets multiple devices or organizations collaboratively train a global model without sharing raw data.
  - *Imperfect global data scenarios:* tackling long-tailed class distributions [[1](#pub-1),[2](#pub-2)] and limited labeled data [[5](#pub-5),[6](#pub-6)] to improve robustness and reliability.
  - *Personalization:* enhancing local-model personalization while preserving global performance [[3](#pub-3)].
  - *Generalization & optimization:* improving global-model generalization through the lens of training dynamics [[4](#pub-4)].

- **Efficient Deep Learning — Dataset Distillation.** Compressing a large dataset into a much smaller distilled one while preserving downstream accuracy.
  - *Efficient distillation:* methods that scale from CIFAR-10 to ImageNet-1K [[8](#pub-8)] and privacy-preserving variants [[11](#pub-11)].
  - *Enhanced utilization:* unlocking the full label potential of distilled data [[7](#pub-7)], revealing key advantages beyond training efficiency [[9](#pub-9)], and novel usage paradigms [[10](#pub-10)].
  - *Survey:* the first comprehensive, stage-wise review of dataset distillation in the large-scale-data era [[12](#pub-12)].

- **Efficient Deep Learning — Data-Efficient Learning.** A data-centric perspective on which data improves training efficiency, and how to acquire it.
  - *Understanding efficient data:* analyzing how samples (X) and targets (Y) jointly shape training efficiency [[13](#pub-13)].
  - *Data optimization:* leveraging publicly pre-trained models to optimize large-scale unlabeled data [[14](#pub-14)].


# 📝 Publications 

<sub><em><sup>*</sup> denotes equal contribution; <sup>†</sup> denotes corresponding author.</em></sub>

<div class='paper-box' id='pub-1'><div class='paper-box-image'><div><div class="badge">IJCAI 2022</div><img src='images/500x300.png' alt="creff" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[1]** [Federated Learning on Heterogeneous and Long-Tailed Data via Classifier Re-Training with Federated Features](https://arxiv.org/pdf/2204.13399.pdf) \| [[code]](https://github.com/shangxinyi/CReFF-FL)

**Xinyi Shang**, Yang Lu<sup>†</sup>, Gang Huang, Hanzi Wang.

- We first find that the biased classifier is the primary factor behind the poor performance of the global model, then propose **CReFF** to optimize a small set of learnable features for classifier re-training.
</div>
</div>

<div class='paper-box' id='pub-2'><div class='paper-box-image'><div><div class="badge">ICME 2022 Oral</div><img src='images/500x300.png' alt="fedic" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[2]** [FEDIC: Federated Learning on Non-IID and Long-Tailed Data via Calibrated Distillation](https://arxiv.org/pdf/2205.00172.pdf) \| [[code]](https://github.com/shangxinyi/FEDIC)

**Xinyi Shang**, Yang Lu<sup>†</sup>, Yiu-ming Cheung, Hanzi Wang.

- A new distillation method with logit adjustment and calibration gating network to solve the joint problem of heterogeneous and long-tailed data.
</div>
</div>

<div class='paper-box' id='pub-3'><div class='paper-box-image'><div><div class="badge">ICCV 2023</div><img src='images/500x300.png' alt="fedetf" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[3]** [No Fear of Classifier Biases: Neural Collapse Inspired Federated Learning with Synthetic and Fixed Classifier](https://arxiv.org/pdf/2303.10058.pdf) \| [[code]](https://github.com/ZexiLee/ICCV-2023-FedETF)

Zexi Li, **Xinyi Shang**, Rui He, Tao Lin<sup>†</sup>, Chao Wu<sup>†</sup>.

- A neural-collapse-inspired method that mitigates classifier biases in federated learning, achieving high global-model generalization together with strong local-model personalization.
</div>
</div>

<div class='paper-box' id='pub-4'><div class='paper-box-image'><div><div class="badge">ICML 2023</div><img src='images/500x300.png' alt="fedlaw" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[4]** [Understanding the Training Dynamics in Federated Deep Learning via Aggregation Weight Optimization](https://arxiv.org/pdf/2302.10911.pdf) \| [[code]](https://github.com/ZexiLee/ICML-2023-FedLAW)

Zexi Li, Tao Lin<sup>†</sup>, **Xinyi Shang**, Chao Wu<sup>†</sup>.

- We analyze FL training dynamics through client coherence and global weight shrinking, and design an aggregation algorithm that measurably improves generalization.
</div>
</div>

<div class='paper-box' id='pub-5'><div class='paper-box-image'><div><div class="badge">CVPR 2025</div><img src='images/500x300.png' alt="mindthegap" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[5]** [Mind the Gap: Confidence Discrepancy Can Guide Federated Semi-Supervised Learning Across Pseudo-Mismatch](https://arxiv.org/pdf/2503.13227.pdf)

Yijie Liu, **Xinyi Shang**, Yiqun Zhang, Yang Lu<sup>†</sup>, Chen Gong, Jing-Hao Xue, Hanzi Wang.

- We show that (1) data heterogeneity intensifies pseudo-label mismatches, and (2) local- and global-model predictive tendencies diverge with heterogeneity. We propose a simple yet effective method to correct pseudo-labels by exploiting confidence discrepancies.
</div>
</div>

<div class='paper-box' id='pub-6'><div class='paper-box-image'><div><div class="badge">TAI 2025</div><img src='images/500x300.png' alt="fedssl-ah" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[6]** [Federated Semi-Supervised Learning with Annotation Heterogeneity](https://arxiv.org/pdf/2303.02445.pdf)

**Xinyi Shang**, Gang Huang, Yang Lu<sup>†</sup>, Jian Lou, Bo Han, Yiu-ming Cheung, Hanzi Wang.

- We formalize Federated Semi-Supervised Learning with annotation heterogeneity and propose a new framework with a mutual-learning strategy.
</div>
</div>

<div class='paper-box' id='pub-7'><div class='paper-box-image'><div><div class="badge">ICLR 2025</div><img src='images/500x300.png' alt="gift" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[7]** [GIFT: Unlocking Full Potential of Labels in Distilled Dataset at Near-zero Cost](https://arxiv.org/pdf/2405.14736) \| [[code]](https://github.com/LINs-lab/GIFT)

**Xinyi Shang<sup>*</sup>**, Peng Sun<sup>*</sup>, Tao Lin<sup>†</sup>.

- Models trained on distilled datasets are highly sensitive to the soft-label loss. Building on this insight, we introduce a plug-and-play approach that efficiently leverages full label information at near-zero cost.
</div>
</div>

<div class='paper-box' id='pub-8'><div class='paper-box-image'><div><div class="badge">ICLRW 2024 DMLR</div><img src='images/500x300.png' alt="infocomp" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[8]** [Information Compensation: A Fix for Any-scale Dataset Distillation](https://openreview.net/forum?id=2SnmKd1JK4)

Peng Sun, Bei Shi, **Xinyi Shang**, Tao Lin<sup>†</sup>.

- A near-lossless information-compression approach that distills the key information of original datasets with minimal loss, surpassing existing methods in both efficiency and effectiveness across dataset scales.
</div>
</div>

<div class='paper-box' id='pub-9'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='images/500x300.png' alt="earlystage" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[9]** Early-Stage Training with Distilled Data Helps Prevalently

**Xinyi Shang<sup>†</sup>**, Jing-Hao Xue.
- We uncover a key advantage of distilled datasets: in early training phases, models trained on distilled data show substantially higher efficiency than those trained on original data. We provide explanations and validate the practical implications.
</div>
</div>

<div class='paper-box' id='pub-10'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='images/500x300.png' alt="rethinking" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[10]** Rethinking the Use of Distilled Data: Embrace, Don't Abandon, the Original Data

**Xinyi Shang<sup>†</sup>**, Jing-Hao Xue.
- We revisit the use of distilled data and propose a dynamic framework that integrates distilled and original data by analyzing their distinct properties. Efficacy is demonstrated both theoretically and empirically.
</div>
</div>

<div class='paper-box' id='pub-11'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='images/500x300.png' alt="privacy" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[11]** Privacy as a Free Lunch: Crafting Initial Distilled Datasets through the Kaleidoscope

Shuo Shi<sup>*</sup>, Peng Sun<sup>*</sup>, **Xinyi Shang<sup>*</sup>**, Tianyu Du<sup>†</sup>, Xuhong Zhang, Jianwei Yin, Tao Lin.
- We identify explicit privacy leakage in distilled datasets and show theoretically that it stems from initializing distilled images with real data. A plug-and-play module applies strong perturbations to real data during initialization to address this.
</div>
</div>

<div class='paper-box' id='pub-12'><div class='paper-box-image'><div><div class="badge">Preprint T-PAMI</div><img src='images/500x300.png' alt="dd-survey" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[12]** [Dataset Distillation in the Era of Large-Scale Data: Methods, Analysis, and Future Directions](https://www.techrxiv.org/users/923195/articles/1295079-dataset-distillation-in-the-era-of-large-scale-data-methods-analysis-and-future-directions)

**Xinyi Shang**, Peng Sun, Zhiqiang Shen, Tao Lin, Jing-Hao Xue.

- We identify four significant shifts in the field of dataset distillation and provide the first comprehensive, stage-wise review through the dataset-distillation pipeline.
</div>
</div>

<div class='paper-box' id='pub-13'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='images/500x300.png' alt="equallycritical" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[13]** Equally Critical: Samples, Targets, and Their Mappings in Datasets

Runkang Yang<sup>*</sup>, Peng Sun<sup>*</sup>, **Xinyi Shang<sup>*</sup>**, Yi Tang, Tao Lin<sup>†</sup>.
- Recent work mostly optimizes samples X while overlooking targets Y. We review the sample-target relationship and comprehensively analyze how variations in target and sample types, quantities, and qualities influence training efficiency and efficacy.
</div>
</div>

<div class='paper-box' id='pub-14'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='images/500x300.png' alt="cudo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**[14]** [Collaborative Unlabeled Data Optimization](https://arxiv.org/pdf/2505.14117)

**Xinyi Shang<sup>*</sup>**, Peng Sun<sup>*</sup>, Fengyuan Liu<sup>*</sup>, Tao Lin<sup>†</sup>.
- We pioneer a data-centric paradigm for collaborative unlabeled data optimization, demonstrating effectiveness and efficiency across diverse datasets and architectures.
</div>
</div>

# 🎖 Honors and Awards
- *2023* Xiamen University Outstanding Master Thesis.
- *2023* Xiamen University Outstanding Graduates.
- *2022* China National Scholarship (Top 0.2%, the highest-level scholarship established by the central government).
- *2022* Excellent Merit Student of Xiamen University (Top 2%).
- *2021* Merit Student of Xiamen University (Top 8%).
- *2020* China College Students Innovation and Entrepreneurship Competition — two provincial projects.
- *2019* Provincial Excellent Volunteer honor (500+ hours of volunteering).
- *2018* Star of Excellent Volunteers honor (only one student in the college per year).

# 💻 Research Experience
- *2022.11 - 2023.09*, Research Intern, [LINs Lab](https://lins-lab.github.io/), Westlake University, supervised by [Prof. Tao Lin](https://tlin-taolin.github.io/). *Decentralized deep learning.*
- *2022.06 - 2022.09*, Research Intern, MARS Lab, Wuhan University, supervised by [Prof. Mang Ye](https://marswhu.github.io/). *Federated learning.*

# 🤝 Academic Service
- **Conference Reviewer:** NeurIPS 2025, ICCV 2025, ICLR 2025, CVPR 2025, WACV 2025, IJCAI 2024.
- **Journal Reviewer:** IEEE TNNLS, IEEE TCSVT, ACM CSUR, IEEE TC, IEEE TETCI.

# 🙌 Voluntary Activities
- *2019.03 - 2019.09*, Director of [Teach For China](https://baike.baidu.com/item/%E7%BE%8E%E4%B8%BD%E4%B8%AD%E5%9B%BD/499616) at Zhongnan University of Economics and Law.
- *2017.09 - 2019.06*, Director of [We-Bright](https://baike.baidu.com/item/%E5%BE%AE%E5%85%89%E6%94%AF%E6%95%99/16975919), supporting 53 rural primary schools across Sichuan and Guangxi provinces.

# 🎨 Hobbies
- [Cooking and Bakery](/files/bakery.pdf) — I hope I will own my bakery one day.
- [Drawing](/files/drawing.pdf).
- Photography and keeping journals.
