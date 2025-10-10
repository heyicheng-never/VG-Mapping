# VG-Mapping: Variation-Aware 3D Gaussians for Online Semi-static Scene Mapping
Yicheng He, Jingwen Yu, Guangcheng Chen, Hong Zhang<br>

This repository contains the dataset and code for the paper VG-Mapping: Variation-Aware 3D Gaussians for Online Semi-static Scene Mapping, an online RGB-D 3D Gaussians mapping system tailored for semi-static scenes.

## Update
- [x] VG-Scene dataset
- [ ] Code for VG-Mapping

## VG-Scene Dataset
### Download
You can download the VG-Scene dataset from [Google Drive](https://drive.google.com/drive/my-drive).
### Dataset format
The **VG-Scene** dataset includes 6 synthetic sequences and 3 real-world sequences. Each sequence consists of a *pre-change* and a *post-change* sub-sequence. The dataset covers common types of scene changes, such as object addition, removal, and rearrangement. The format of the dataset is shown below.

```
VG-Scene
|
|---- ldyn_real  # Real-world semi-static sequences
|     |---- meeting_room_745
|     |       +--- cam_params.json
|     |       +--- depth
|     |       |     └── 1757854453.628079891.png
|     |       |     └── ......
|     |       +--- rgb
|     |       |     └── 1757854453.628079891.png
|     |       |     └── .......
|     |       --- depth.txt
|     |       --- rgb.txt
|     |       --- groundtruth.txt
|     |---- multi_tables_593
|     |---- table_276
|     |
|---- ldyn_syn  # Synthetic semi-static sequences
|     |
|     |---- barbershop1_280
|     |       +--- intrinsic.txt
|     |       +--- results
|     |       |     +--- depth000000.png
|     |       |     └── frame000000.jpg
|     |       |     └── ......     
|     |       --- traj.txt
|     |---- barbershop2_280
|     |---- classroom_500
|     |---- Cloister_500
|     |---- flat1_400
|     |---- flat2_400
```

The format of the synthetic sequences in the ldyn_real folder is consistent with that of the [Replica](https://github.com/cvg/nice-slam?tab=readme-ov-file), while the real-world sequences in the ldyn_syn folder follow the format of the [TUM-RBGD](https://cvg.cit.tum.de/data/datasets/rgbd-dataset/download). Each sequence follows the naming format: *sequence name_post-change start frame index*.
