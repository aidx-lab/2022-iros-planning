---
layout: page
title: 
---

This site complements the paper [**Speeding Up Optimization-based Motion Planning through Deep Learning**](https://ieeexplore.ieee.org/document/9981717) 
by 
[Johannes Tenhumberg](https://scholar.google.com/citations?user=2RZuYZMAAAAJ), 
[Darius Burschka](https://scholar.google.com/citations?user=y-MzVoUAAAA), and 
[Berthold Bäuml](https://scholar.google.com/citations?user=fjvpDsEAAAAJ) 
presented at the _2022 IEEE/RSJ International Conference on Intelligent Robots and Systems_ in Kyoto, Japan.

Here we introduce the different robots we used for our work and provide additional information on the datasets.
Furthermore, we describe our methods, the network architecture, and the training process in more detail.

![Justin](/assets/imgs/index/SphereJustin_in_PerlinNoise_33641.jpg)

# Abstract
---
Planning collision-free motions for robots with many degrees of freedom is challenging in complex environments. 
Recent work introduced the idea of speeding up the planning by encoding prior experience of successful motions in a neural network and then using the network’s predictions to help a motion planner, providing an initial guess for an optimization- based planner. 
However, this “neural motion planning” did not scale to complex robots in unseen 3D environments as needed for real-world applications. In this paper, we make use of the so-called “basis point set” [[Prokudin2019](https://arxiv.org/abs/1908.09186)] as a modern method to represent spatial data for neural motion planning to fill this gap. 
This new compact environment encoding, first introduced in computer vision, enables the efficient supervised training of motion planning networks that generalize well over diverse 3D worlds. To reach 100% planning success, we also introduce an elaborate training scheme.
We combine the network and the objective function as a metric to efficiently clean, extend and boost an initial dataset produced by a classical solver. 
The resulting network can predict an initial guess that quickly converges to a feasible solution, massively outperforming random multi-starts in unseen environments. Furthermore, the quick inference time of the network plus the guarantees of a classical solver lead to a fast (200 ms on a single CPU core) and safe way to generate optimal paths for the humanoid robot Agile Justin with 19DoF.
Finally, we show a successful real-world experiment based on a high-resolution world model from an integrated 3D sensor.

# Video
---
<p align="center">
<iframe width="560" height="315" 
src="https://www.youtube.com/embed/fKe1_vUNCew?si=7sDCKk_Sdc84OaTV"
frameborder="0"
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
referrerpolicy="strict-origin-when-cross-origin" 
allowfullscreen>
</iframe>
</p>

---
Cite this paper as:
```
@inproceedings{Tenhumberg2022,
  title={Speeding Up Optimization-based Motion Planning through Deep Learning},
  author={Tenhumberg, Johannes and Burschka, Darius and B{\"a}uml, Berthold},
  booktitle={IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)}, 
  year={2022},
}
```
[arxiv](https://arxiv.org/abs/2311.08345)
