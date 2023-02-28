
 
<div align="center">

<!-- TITLE -->
# 🌎 &nbsp; **Internet Explorer** &nbsp; 🌏
Targeted Representation Learning on the Open Web

[![arXiv](https://img.shields.io/badge/cs.LG-arXiv:2302.14051-b31b1b.svg)](https://arxiv.org/abs/2302.14051)
[![Website](https://img.shields.io/badge/🌎-Website-blue.svg)](http://internet-explorer-ssl.github.io)
[![Video](https://img.shields.io/badge/Video-YouTube-red.svg)](https://internet-explorer-ssl.github.io/static/videos/internet_explorer.mp4)
</div>


<!-- DESCRIPTION -->
## Abstract

Vision models heavily rely on fine-tuning general-purpose
models pre-trained on large, static datasets. These
general-purpose models only understand knowledge within
their pre-training datasets, which are tiny, out-of-date
snapshots of the Internet—where billions of images are
uploaded each day.


We suggest an alternate approach: rather than hoping our
static datasets transfer to our desired tasks after
large-scale pre-training, we propose dynamically utilizing
the Internet to quickly train a small-scale model that
does extremely well on the task at hand. Our approach,
called Internet Explorer, explores the web in a
self-supervised manner to progressively find relevant
examples that improve performance on a desired target
dataset. It cycles between searching for images on the
Internet with text queries, self-supervised training on
downloaded images, determining which images were useful,
and prioritizing what to search for next.


We evaluate Internet Explorer across several datasets and
show that it outperforms or matches CLIP oracle
performance by using just a single GPU desktop to actively
query the Internet for 30–40 hours.

## Overview
### Learn a task-specific model by exploring the web
Given unlabeled data for a target task, our approach, Internet Explorer, searches the Internet to progressively find more and more relevant training data via self-supervised training.

<div align="center">
<img src="./static/explorer_setting.svg" width="500" style="display: block; margin: 0 auto;">
</div>

### Method
Internet Explorer iteratively repeats 4 steps to find and learn from relevant Internet data. It cycles between searching for images on the Internet with text queries, self-supervised training on downloaded images, determining which images are relevant to the target dataset, and prioritizing what to search for next.

<div align="center">
<img src="./static/explorer_method.svg" width="500" style="display: block; margin: 0 auto;">
</div>

## Code
Coming soon!


<!-- CITATION -->
## Citation

If you find this work useful in your research, please cite:

```bibtex
@misc{li2023internet,
    title={Internet Explorer: Targeted Representation Learning on the Open Web}, 
    author={Alexander C. Li and Ellis Brown and Alexei A. Efros and Deepak Pathak},
    year={2023},
    eprint={2302.14051},
    archivePrefix={arXiv},
    primaryClass={cs.LG}
}
```
