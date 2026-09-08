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

I am **Yiran Qiao**, a PhD candidate in Computer Science at Case Western Reserve University, where I am fortunate to be advised by [Prof. Jing Ma](https://jma712.github.io/). Prior to that, I received my M.S. from The Ohio State University and my B.S. in Electrical Engineering from Xi'an Jiaotong University.

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

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">AAAI 2025</div><img src='images/aaai2025-poster.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Certified Causal Defense with Generalizable Robustness

**Kaiming He**, Xiangyu Zhang, Shaoqing Ren, Jian Sun

[**\[Paper\]**](https://arxiv.org/pdf/2408.15451)
- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
</div>
</div>

- [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020**

</div>


<div id="panel-experience" class="tab-panel"{% if active != "panel-experience" %} hidden{% endif %} markdown="1">

# 💼 Experience

<!--
格式参考，删掉本注释后照着写：
- *2024.05 - 2024.08*, **Research Intern**, Company / Lab, City. Worked on ___.
-->

# 📖 Education

- **Case Western Reserve University** — Ph.D. in Computer Science, advised by [Prof. Jing Ma](https://jma712.github.io/)
- **The Ohio State University** — M.S.
- **Xi'an Jiaotong University** — B.S. in Electrical Engineering

</div>


<div id="panel-awards" class="tab-panel"{% if active != "panel-awards" %} hidden{% endif %} markdown="1">

# 🎖 Awards

<!--
格式参考，删掉本注释后照着写：
- *2025.03*, Award name, Granting body.
-->

# 🤝 Service

<!--
格式参考：
**Reviewer**: NeurIPS 2025, ICML 2025, CVPR 2025
-->

</div>
