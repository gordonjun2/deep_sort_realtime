# Deep Sort Tracking with CenterNet (or CenterNet (by Xing Yi Zhou))

## Introduction

- Deep Sort is added on top of CenterNet-1
- Detections by CenterNet-1 will be send to Deep Sort to do the tracking

## How to use

Enter main directory and use:

```
python demo_deep_sort.py ctdet_drone --dataset visdrone --arch <choose your arch> --load_model <path to .pth> --demo <path to video>

```

# Deep SORT

## Introduction
A more realtime adaptation of Deep SORT.
Adapted from the official repo of *Simple Online and Realtime Tracking with a Deep Association Metric* (Deep SORT): [Git Repo](https://github.com/nwojke/deep_sort)
See the Deep Sort's paper [arXiv preprint](https://arxiv.org/abs/1703.07402) for more information.

## Dependencies
- Python 3.5
- NumPy
- sklean
- cv2
- Embedder requires Pytorch & Torchvision

## Sorry i have no time to document further please just call me haha

## [From original repo] Highlevel overview of source files

In the top-level directory are executable scripts to execute, evaluate, and
visualize the tracker. The main entry point is in `deep_sort_app.py`.
This file runs the tracker on a MOTChallenge sequence.

In package `deep_sort` is the main tracking code:

* `detection.py`: Detection base class.
* `kalman_filter.py`: A Kalman filter implementation and concrete
   parametrization for image space filtering.
* `linear_assignment.py`: This module contains code for min cost matching and
   the matching cascade.
* `iou_matching.py`: This module contains the IOU matching metric.
* `nn_matching.py`: A module for a nearest neighbor matching metric.
* `track.py`: The track class contains single-target track data such as Kalman
  state, number of hits, misses, hit streak, associated feature vectors, etc.
* `tracker.py`: This is the multi-target tracker class.