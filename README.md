# [A deep cut into Split Federated Self-supervised Learning](https://arxiv.org/abs/2406.08267)

This repository implements Momentum-Aligned contrastive Split Federated Learning (MonAcoSFL), presented at ECML PKDD 2024 - [check out the poster](https://drive.google.com/file/d/1-HqeQaHlxRKwCJrC1Ve8UiujH77D98L-/view).


It is an extension of [MocoSFL](https://openreview.net/forum?id=2QGJXyMNoPz), which keeps the online/momentum client models aligned during parameter synchronizations. 
This stabilizes the training and yields vastly improved results in deeper cut-layers that are more communication-efficient.

## Comparison of MocoSFL and MonAcoSFL

![image](plots/monacosfl.png)

## Overview

Collaborative self-supervised learning has recently become feasible in highly distributed environments by dividing the network layers between client devices and a central server. However, state-of-the-art methods, such as MocoSFL, are optimized for network division at the initial layers, which decreases the protection of the client data and increases communication overhead. In this paper, we demonstrate that splitting depth is crucial for maintaining privacy and communication efficiency in distributed training. We also show that MocoSFL suffers from a catastrophic quality deterioration for the minimal communication overhead. As a remedy, we introduce Momentum-Aligned contrastive Split Federated Learning (MonAcoSFL), which aligns online and momentum client models during training procedure. Consequently, we achieve state-of-the-art accuracy while significantly reducing the communication overhead, making MonAcoSFL more practical in real-world scenarios. 

## Getting Started

### Prerequisite:

Python > 3.7 with Pytorch, Torchvision

### Project Structure

`/run_monacosfl.py` -- Source files for MonAcoSFL

`/scripts` -- Evaluation scripts used on a single-GPU machine


## Acknowledgments

This repository is based on the [original MocoSFL codebase](https://github.com/SonyResearch/MocoSFL). 
We would like to thank the authors for open-sourcing it.

This research has been supported by the flagship project entitled "Artificial Intelligence Computing Center Core Facility" from the Priority Research Area DigiWorld under the Strategic Programme Excellence Initiative at Jagiellonian University, and by the Horizon Europe Programme (HORIZON-CL4-2022-HUMAN02) under the project "ELIAS: European Lighthouse of AI for Sustainability", GA no. 101120237. The research of Marcin Przewięźlikowski was supported by14 Marcin Przewięźlikowski, Marcin Osial, Bartosz Zieliński, and Marek Śmiejathe National Science Centre (Poland), grant no. 2023/49/N/ST6/03268. The research of Marcin Osial was supported by National Science Centre (Poland) grant number 2023/50/E/ST6/00469. The research of Marek Śmieja was supported by the National Science Centre (Poland), grant no. 2022/45/B/ST6/01117. The research of Bartosz Zieliński was supported by National Science Centre (Poland) grant number 2022/47/B/ST6/03397. Some experiments were performed on servers purchased with funds from a grant from the Priority Research Area (Artificial Intelligence Computing Center Core Facility) under the Strategic Programme Excellence Initiative at Jagiellonian University. We gratefully acknowledge Polish high-performance computing infrastructure PLGrid (HPC Center: ACK Cyfronet AGH) for providing computer facilities and support within computational grant no. PLG/2023/016303.

## Citation

If you find our work interesting, please cite it:

```
@inproceedings{przewiezlikowski2024deepcut,
author = {Przewięźlikowski, Marcin and Osial, Marcin and Zieliński, Bartosz and Śmieja, Marek},
title = {A Deep Cut Into Split Federated Self-Supervised Learning},
year = {2024},
isbn = {978-3-031-70343-0},
publisher = {Springer-Verlag},
address = {Berlin, Heidelberg},
url = {https://doi.org/10.1007/978-3-031-70344-7_26},
doi = {10.1007/978-3-031-70344-7_26},
booktitle = {Machine Learning and Knowledge Discovery in Databases. Research Track: European Conference, ECML PKDD 2024, Vilnius, Lithuania, September 9–13, 2024, Proceedings, Part II},
pages = {444–459},
numpages = {16},
keywords = {Federated learning, Self-supervised learning, Contrastive learning},
location = {Vilnius, Lithuania}
}
```



