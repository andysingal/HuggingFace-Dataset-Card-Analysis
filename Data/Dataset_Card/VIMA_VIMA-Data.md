---
license: cc-by-4.0
---

# Dataset Card for VIMA-Data

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
- [Dataset Structure](#dataset-structure)
- [Dataset Creation](#dataset-creation)
- [Additional Information](#additional-information)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)

## Dataset Description

- **Homepage:** https://vimalabs.github.io/
- **Repository:** https://github.com/vimalabs/VimaBench
- **Paper:** https://arxiv.org/abs/2210.03094

### Dataset Summary

This is the official dataset used to train general robot manipulation agents with multimodal prompts, as presented in [paper](https://arxiv.org/abs/2210.03094). It contains 650K trajectories for 13 tasks in [VIMA-Bench](https://github.com/vimalabs/VimaBench). All demonstrations are generated by oracls.

## Dataset Structure

Data are grouped into different tasks. Within each trajectory's folder, there are two folders `rgb_front` and `rgb_top`, and three files `obs.pkl`, `action.pkl`, and `trajectory.pkl`. RGB frames from a certain perspective are separately stored in corresponding folder. `obs.pkl` includes segmentation and state of end effector. `action.pkl` contains oracle actions. `trajectory.pkl` contains meta information such as elapsed steps, task information, and object information. Users can build their custom data piepline starting from here. More details and examples can be found [here](https://github.com/vimalabs/VimaBench#training-data).

## Dataset Creation

All demonstrations are generated by scripted oracles.

## Additional Information

### Licensing Information

This dataset is released under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/legalcode) license.

### Citation Information

If you find our work useful, please consider citing us! 

```bibtex
@article{jiang2022vima,
  title   = {VIMA: General Robot Manipulation with Multimodal Prompts},
  author  = {Yunfan Jiang and Agrim Gupta and Zichen Zhang and Guanzhi Wang and Yongqiang Dou and Yanjun Chen and Li Fei-Fei and Anima Anandkumar and Yuke Zhu and Linxi Fan},
  year    = {2022},
  journal = {arXiv preprint arXiv: Arxiv-2210.03094}
}
```