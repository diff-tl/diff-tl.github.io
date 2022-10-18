---
hide_site_title: true
layout: splash
permalink: /
excerpt: "
<a href=\"https://ziweixu.github.io\" target=\"_blank\">Ziwei&nbsp;Xu</a><sup>1</sup> &emsp;
<a href=\"https://www.crcv.ucf.edu/person/rawat/\" target=\"_blank\">Yogesh&nbsp;S&nbsp;Rawat</a><sup>2</sup> &emsp;
<a href=\"https://sites.google.com/site/yongkangwong/\" target=\"_blank\">Yongkang&nbsp;Wong</a><sup>1</sup> &emsp;
<a href=\"https://www.comp.nus.edu.sg/~mohan/\" target=\"_blank\">Mohan&nbsp;S&nbsp;Kankanhalli</a><sup>1</sup> &emsp;
<a href=\"https://www.cs.ucf.edu/person/mubarak-shah/\" target=\"_blank\">Mubarak&nbsp;Shah</a><sup>2</sup> <br>

<sup>1</sup> National University of Singapore <br>
<sup>2</sup> Center for Research in Computer Vision, University of Central Florida
"
header:
  overlay_color: "#fff"
  overlay_filter: "0.0"
  actions:
    - label: "<i class=\"fas fa-file-pdf\"></i> &nbsp; Paper"
      url: ""
    - label: "<i class=\"fa-brands fa-github\"></i> &nbsp; Code"
      url: "https://github.com/ZiweiXU/DTL-action-segmentation"

title: "<div id=\"toc\">
Don't Pour Cereal into Coffee: <br>
Differentiable Temporal Logic for Temporal Action Segmentation
</div>"
---

<video autoplay preload controls object-fit="cover" width="100%" height="100%">
  <source src="assets/videos/animation.mp4" type="video/mp4">
</video>



- [Abstract](#abstract)
- [How does it work?](#how-does-it-work)

# Abstract
{: .text-center}

We propose Differentiable Temporal Logic (DTL), a model-agnostic framework that introduces temporal constraints to deep networks.
DTL treats the outputs of a network as a truth assignment of a temporal logic formula, and computes a temporal logic loss reflecting the consistency between the output and the constraints.
We propose a comprehensive set of constraints, which are implicit in data annotations, and incorporate them with deep networks via DTL.
We evaluate the effectiveness of DTL on the temporal action segmentation task and observe improved performance and reduced logical errors in the output of different task models.
Furthermore, we provide an extensive analysis to visualize the desirable effects of DTL.

# How does it work?
{: .text-center}

[Back to Top](#toc){: .btn-primary .btn--small}
{: .text-center}