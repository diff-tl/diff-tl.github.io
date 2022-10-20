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
      url: "/assets/docs/dtl_neurips2022.pdf"
    - label: "<i class=\"fa-brands fa-github\"></i> &nbsp; Code"
      url: "https://github.com/ZiweiXU/DTL-action-segmentation"
    - label: "<i class=\"fa-solid fa-clapperboard\"></i> &nbsp; SlidesLive"
      url: "https://recorder-v3.slideslive.com/?share=72695&s=7a503918-cc32-4c0e-bfb3-a7eb2e461cfc"

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
  - [Problem Formulation](#problem-formulation)
  - [Collecting Constraints (WIP)](#collecting-constraints-wip)
  - [Write Temporal Logic Formula (WIP)](#write-temporal-logic-formula-wip)

# Abstract
{: .text-center}

We propose Differentiable Temporal Logic (DTL), a model-agnostic framework that introduces temporal constraints to deep networks.
DTL treats the outputs of a network as a truth assignment of a temporal logic formula, and computes a temporal logic loss reflecting the consistency between the output and the constraints.
We propose a comprehensive set of constraints, which are implicit in data annotations, and incorporate them with deep networks via DTL.
We evaluate the effectiveness of DTL on the temporal action segmentation task and observe improved performance and reduced logical errors in the output of different task models.
Furthermore, we provide an extensive analysis to visualize the desirable effects of DTL.

# How does it work?
{: .text-center}

## Problem Formulation

We consider the action segmentation task in a video clip with `$L$` frames and `$N$` candidate actions `$\Set{A}={a_1,\ldots,a_N}$`.
We assume that there is a deep task model $g$ parameterized by `$\Mat{\Theta}$`, which takes frames `$\Vec{x}_0, \ldots, \Vec{x}_{L-1}$` as input, and outputs `$\hVec{y}_{a_1}, \ldots, \hVec{y}_{a_N}$`, where `$\hVec{y}_{a_i} \in \mathbb{R}^L$` is the unnormalized score for the presence of action `$a_i$` throughout the `$L$` frames.
We assume `$\hVec{y}_{a_i,t} > 0$` indicates $a_i$ presents at time `$t$`, and `$\hVec{y}_{a_i,t} \leq 0$` indicates the opposite.

Apart from the ground truth label `$\Vec{y}_{a_1},\ldots,\Vec{y}_{a_N}$`, there is a set of constraints that describe the relation between actions.
The design goal of DTL is to incorporate these constraints into the task model `$g$`, so that `$\hVec{y}$` complies with both the ground truth `$\Vec{y}$` and the constraints.
In order to do so, we introduce a temporal logic representation `$\Psi$`, and an evaluator $f$ that enforces the constraints in formula `$\psi \in \Psi$` on `$g$`, through its outputs `$\hVec{y}$`.

We achieve this objective in the following steps:

1. Collect constraints as `$\mathcal{C}$`.
2. Write constraints as a temporal logic formula `$\psi$`.
3. Evaluate `$\psi$` against model output `$\hVec{y}$` using `$f$`, as `$f(\psi, \hVec{y})$`, which reflect if `$\psi$` is satisfied.
4. Optimize model `$g$` such that `$f(\psi, \hVec{y})$` shows `$\hVec{y}$` satisfies `$\psi$`.

[Back to Top](#toc){: .btn-primary .btn--small}
{: .text-center}

## Collecting Constraints (WIP)

[Back to Top](#toc){: .btn-primary .btn--small}
{: .text-center}

## Write Temporal Logic Formula (WIP)

[Back to Top](#toc){: .btn-primary .btn--small}
{: .text-center}