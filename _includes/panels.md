{% comment %}
三个面板的正文。/、/experience/、/awards-and-service/ 三个页面都会 include 这个
文件，所以每个页面的 DOM 里都有全部三个面板 —— tabs.html 才能用 pushState 原地
切换而不刷新。

哪个面板初始可见由 include 方传入的 page.panel 决定（在服务端就渲染好 hidden，
避免加载瞬间闪现错误的面板）。

每个面板必须带 markdown="1"，否则 kramdown 会把 div 里的内容当成纯 HTML，
标题、列表、链接全部失效。
{% endcomment %}
{% assign active = page.panel | default: "panel-home" %}

<div id="panel-home" class="tab-panel"{% if active != "panel-home" %} hidden{% endif %} markdown="1">

<span class='anchor' id='about-me'></span>

I am **Yiran Qiao**, a PhD student in Computer Science at Case Western Reserve University, where I am fortunate to be advised by [Prof. Jing Ma](https://jma712.github.io/). Prior to that, I received my M.S. in Electrical and Computer Engineering from The Ohio State University and my B.Eng. in Electrical Engineering from Xi'an Jiaotong University.

My research centers on **diffusion models** and **flow matching**, along with their applications to world models and 3D generation. I am also interested in causal inference and adversarial attacks and defenses.


# 🔥 News
- *2026.08*: &nbsp;🎉 Our paper _NS-Copilot_ is accepted to **EMNLP 2026 Findings**!
- *2026.06*: &nbsp;🎉 Our paper _DefenseSplat_ is accepted to **ECCV 2026**!
- *2026.05*: &nbsp;🎉 Our paper _SAIF_ is accepted to **ECML PKDD 2026**!
- *2026.04*: &nbsp;🎉 Our paper _YesBut-v2_ is accepted to **TPAMI**!
- *2025.09*: &nbsp;🎉 Our paper _Segment then Splat_ is accepted to **Neurips 2025**!
- *2024.12*: &nbsp;🎉 Our paper _GLEAN_ is accepted to **AAAI 2025**!
- *2024.09*: &nbsp;🎉 Our paper _YesBut_ is accepted to **Neurips 2024 (Oral)**!


# 📝 Selected Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='/images/valerant.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

<span style="font-variant: small-caps;">Valerant</span>: An Automatic Na<u>V</u>ig<u>A</u>b<u>L</u><u>E</u> Game Map Generato<u>R</u> via <u>A</u>ction-Co<u>N</u>ditioned World Model Explora<u>T</u>ion

**Yiran Qiao**, Feng Wang, Jing Ma

[**\[Paper\]**](https://arxiv.org/pdf/2609.09418) [**\[Project Page\]**](https://yrqiao.github.io/VALERANT/)
- VALERANT builds a navigable 3D game map from a single image by rolling out candidate actions through an action-conditioned world model, reconstructing each rollout with SLAM, and committing the step that scores best.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='/images/dilast.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Structured 3D Latents Are Surprisingly Powerful: Unleashing Generalizable Style with 2D Diffusion

**Yiran Qiao**, Yiren Lu, Yunlai Zhou, Disheng Liu, Linlin Hou, Rui Yang, Yu Yin, Jing Ma

[**\[Paper\]**](https://arxiv.org/pdf/2605.04412) [**\[Project Page\]**](https://yrqiao.github.io/DiLAST/)
- We introduce **DiLAST**: 2D <u>Di</u>ffusion-based <u>L</u>atent <u>A</u>wakening for 3D <u>S</u>tyle <u>T</u>ransfer. It guides a 3D generator's structured latents with a pretrained 2D diffusion teacher, transferring styles well outside the generator's training distribution and plugging into existing backbones unchanged.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='/images/advsplat.jpg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

AdvSplat: Adversarial Attacks on Feed-Forward Gaussian Splatting Models

**Yiran Qiao**, Yiren Lu, Yunlai Zhou, Rui Yang, Linlin Hou, Yu Yin, Jing Ma

[**\[Paper\]**](https://arxiv.org/pdf/2603.23686) [**\[Project Page\]**](https://yrqiao.github.io/AdvSplat/)
- AdvSplat gives the first systematic account of adversarial attacks on feed-forward 3DGS, with two query-efficient black-box algorithms that parameterize imperceptible pixel perturbations in the frequency domain and disrupt reconstruction without access to model internals.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ECCV 2026</div><img src='/images/eccv2026-poster.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

DefenseSplat: Enhancing the Robustness of 3D Gaussian Splatting via Frequency-Aware Filtering

**Yiran Qiao**, Yiren Lu, Yunlai Zhou, Rui Yang, Linlin Hou, Yu Yin, Jing Ma

[**\[Paper\]**](https://arxiv.org/pdf/2602.19323) [**\[Code\]**](https://github.com/yrqiao/DefenseSplat)
- DefenseSplat filters poisoned input views in the wavelet domain and regularizes Gaussian scale during training, restoring 3DGS fidelity under attack without adversarial training or clean ground truth.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">AAAI 2025</div><img src='/images/aaai2025-poster.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Certified Causal Defense with Generalizable Robustness

**Yiran Qiao**, Yu Yin, Chen Chen, Jing Ma

[**\[Paper\]**](https://arxiv.org/pdf/2408.15451) [**\[Code\]**](https://github.com/yrqiao/Glean/tree/main)
- GLEAN learns causally invariant features behind an L-Lipschitz encoder, certifying a robustness radius that holds across shifted domains.
</div>
</div>



<!-- - [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020** -->

</div>


<div id="panel-experience" class="tab-panel"{% if active != "panel-experience" %} hidden{% endif %} markdown="1">

# 💼 Internship Experience

<!--
每条一个 cv-item。cv-line 是左右两栏（左边机构/职位，右边地点/日期），
对应 LaTeX 里的 \hfill；窄屏上会换行而不是挤在一起。
-->

<div class="cv-item">
  <div class="cv-line"><strong>Xi’an Jiaotong University</strong><span>Xi’an, China</span></div>
  <div class="cv-line"><em>Research Assistant Intern</em><span>Aug 2020 – Jun 2021</span></div>
</div>

Supervisor: Prof. Xiong Wu<br>
*Topic: Distributed Energy Storage in Smart Grids*

<div class="cv-item">
  <div class="cv-line"><strong>Emerson Technology Resources (Xi’an) Co., Ltd.</strong><span>Xi’an, China</span></div>
  <div class="cv-line"><em>Electrical Engineering Intern</em><span>Jun 2020 – Aug 2020</span></div>
</div>

# 📖 Education

<div class="cv-item">
  <div class="cv-line"><strong>Case Western Reserve University</strong><span>Cleveland, OH, USA</span></div>
  <div class="cv-line"><em>Ph.D. in Computer Science</em><span>Aug 2023 – Present</span></div>
</div>

<div class="cv-item">
  <div class="cv-line"><strong>The Ohio State University</strong><span>Columbus, OH, USA</span></div>
  <div class="cv-line"><em>M.S. in Electrical and Computer Engineering</em><span>Aug 2021 – May 2023</span></div>
</div>

<div class="cv-item">
  <div class="cv-line"><strong>Xi’an Jiaotong University</strong><span>Xi’an, China</span></div>
  <div class="cv-line"><em>B.Eng. in Electrical Engineering</em><span>Sep 2015 – Jun 2019</span></div>
</div>

</div>


<div id="panel-awards" class="tab-panel"{% if active != "panel-awards" %} hidden{% endif %} markdown="1">

# 🎖 Awards

<div class="cv-item">
  <div class="cv-line"><strong>Outstanding Graduate Teaching Award</strong><span>2025</span></div>
</div>

# 🤝 Service

**Conference Reviewer**: NeurIPS 2025, ICLR 2026, ICML 2026, CVPR 2026, NeurIPS 2026, ICLR 2027

**Teaching Assistant**: CSDS 452, CSDS 435, CSDS 433

</div>
