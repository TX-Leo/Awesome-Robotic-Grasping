# Awesome-Robtoic-Grasping

## 目录

-   [Grasping Method](#Grasping-Method)
    -   [CNN(Convolutional Neural Network)](#CNNConvolutional-Neural-Network)
    -   [NeRF](#NeRF)
    -   [RL](#RL)
    -   [MLLM](#MLLM)
-   [Grasping Dataset](#Grasping-Dataset)
-   [Grasping Simulation](#Grasping-Simulation)
    -   [PyBullet](#PyBullet)
    -   [ROS+Gazebo](#ROSGazebo)
-   [Else Gripper | Else Arm](#Else-Gripper--Else-Arm)
    -   [Dexterous Grasping](#Dexterous-Grasping)
    -   [Dual-Arm Grasping](#Dual-Arm-Grasping)
    -   [Suction Grasping](#Suction-Grasping)
    -   [Multi-Fingered Grasping](#Multi-Fingered-Grasping)
-   [Research Group](#Research-Group)
    -   [USA](#USA)
    -   [Europe](#Europe)
    -   [China](#China)
    -   [Google Deepmind](#Google-Deepmind)
-   [Conference](#Conference)
-   [Talk](#Talk)
-   [Video](#Video)
-   [Book](#Book)
-   [Survey about Robotic Grasping](#Survey-about-Robotic-Grasping)
    -   [Github](#Github)
    -   [Paper](#Paper)
-   [My Ideas](#My-Ideas)

@ Date: 2023.11.25

@ Author: [Zhi Wang(Leo TX)](https://tx-leo.github.io/ "Zhi Wang(Leo TX)")

@ Email: <tx.leo.wz@gmail.com>

> 📌mostly for two-fingers gripper

## Grasping Method

### CNN(Convolutional Neural Network)

| Name                 | Features                                                                                                | 📄Paper                                                                                                                                                                | 🌐Project                                                        | 📁Github                                                                 |                              |
| -------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------------------- |
| GPD                  | Detect grasp poses in point clouds                                                                      | [Paper](https://arxiv.org/pdf/1706.09911.pdf?file=1706.09911.pdf "Paper")                                                                                              | Project                                                          | [Github](https://github.com/atenpas/gpd "Github")                        |                              |
| GQ-CNN               | Grasp Quality Convolutional Neural Networks                                                             | Paper                                                                                                                                                                  | [Project](https://berkeleyautomation.github.io/gqcnn/ "Project") | [Github](https://github.com/BerkeleyAutomation/gqcnn "Github")           |                              |
| GG-CNN               | Generative Grasping CNN                                                                                 | [Paper](https://arxiv.org/pdf/1804.05172.pdf "Paper")                                                                                                                  | Project                                                          | [Github](https://github.com/dougsm/ggcnn "Github")                       |                              |
| GraspNet-Baseline    | Baseline model for "GraspNet-1Billion: A Large-Scale Benchmark for General Object Grasping" (CVPR 2020) | [Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Fang_GraspNet-1Billion_A_Large-Scale_Benchmark_for_General_Object_Grasping_CVPR_2020_paper.pdf "Paper") | [Project](graspnet.net/ "Project")                               | [Github](https://github.com/graspnet/graspnet-baseline "Github")         |                              |
| GR-CNN               | Antipodal Robotic Grasping using Generative Residual Convolutional Neural Network                       | [Paper](https://arxiv.org/pdf/1909.04810.pdf "Paper")                                                                                                                  | Project                                                          | Github                                                                   |                              |
| Contact-GraspNet     |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
| GPNet                |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
| Graspness            |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
| Keypoint-GraspNet    | Keypoint-GraspNet: Keypoint-based 6-DoF Grasp Generation from the Monocular RGB-D input                 | [Paper](https://arxiv.org/pdf/2209.08752.pdf "Paper")                                                                                                                  | Project                                                          | [Github](https://github.com/ivalab/KGN "Github")                         |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
| PointNetGPD          |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
|                      | RGB-D Grasp Detection via Depth Guided Learning with Cross-modal Attention                              | [Paper](https://arxiv.org/pdf/2302.14264.pdf "Paper")                                                                                                                  |                                                                  |                                                                          | add depth in planar grasping |
| Scale-Balanced-Grasp | Towards Scale Balanced 6-DoF Grasp Detection in Cluttered Scenes                                        | [Paper](https://arxiv.org/pdf/2212.05275.pdf "Paper")                                                                                                                  | Project                                                          | [Github](https://github.com/mahaoxiang822/Scale-Balanced-Grasp "Github") |                              |
| VCPD                 | Volumetric-based Contact Point Detection for 7-DoF Grasping                                             | [Paper](https://openreview.net/pdf?id=SrSCqW4dq9 "Paper")                                                                                                              | Project                                                          | [Github](https://github.com/caijunhao/vcpd "Github")                     |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
| L2G                  | End-to-End Learning to Grasp via Sampling From Object Point Clouds                                      | [Paper](https://arxiv.org/pdf/2203.05585.pdf "Paper")                                                                                                                  | Project                                                          | [Github](https://github.com/antoalli/L2G "Github")                       | pc                           |
| SymmetryGrasp        | SymmetryGrasp: Symmetry-Aware Antipodal Grasp Detection From Single-View RGB-D Images                   | [Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=\&arnumber=9919329 "Paper")                                                                                     | Project                                                          | Github                                                                   | pc                           |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |
|                      |                                                                                                         | Paper                                                                                                                                                                  | Project                                                          | Github                                                                   |                              |

### NeRF

| Name      | Features                                                                                                                                                                                                                                                                                                                                                                                                                                             | 📄Paper                                           | 🌐Project                                                       | 📁Github                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------- |
| VGN       | VGN is a 3D convolutional neural network for real-time 6 DOF grasp pose detection. The network accepts a Truncated Signed Distance Function (TSDF) representation of the scene and outputs a volume of the same spatial resolution, where each cell contains the predicted quality, orientation, and width of a grasp executed at the center of the voxel. The network is trained on a synthetic grasping dataset generated with physics simulation. | [Paper](http://arxiv.org/abs/2101.01132 "Paper")  | Project                                                         | [Github](https://github.com/ethz-asl/vgn "Github")       |
| GIGA      | Synergies Between Affordance and Geometry: 6-DoF Grasp Detection via Implicit Representations                                                                                                                                                                                                                                                                                                                                                        | [Paper](http://arxiv.org/abs/2104.01542 "Paper")  | [Project](https://sites.google.com/view/rpl-giga2021 "Project") | [Github](https://github.com/UT-Austin-RPL/GIGA "Github") |
| GraspNeRF | GraspNeRF: Multiview-based 6-DoF Grasp Detection for Transparent and Specular Objects Using Generalizable NeRF                                                                                                                                                                                                                                                                                                                                       | [Paper](https://arxiv.org/abs/2210.06575 "Paper") | [Project](https://pku-epic.github.io/GraspNeRF/ "Project")      | [Github](https://github.com/PKU-EPIC/GraspNeRF "Github") |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |
|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Paper                                             | Project                                                         | Github                                                   |

### RL

| Name                    | Features                                                                                         | 📄Paper                                               | 🌐Project                                          | 📁Github                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------- |
| visual-pushing-grasping | Learning Synergies between Pushing and Grasping with Self-supervised Deep Reinforcement Learning | [Paper](https://arxiv.org/pdf/1803.09956.pdf "Paper") | [Project](https://vpg.cs.princeton.edu/ "Project") | [Github](https://github.com/andyzeng/visual-pushing-grasping "Github") |
| drl\_grasping           | Deep Reinforcement Learning for Robotic Grasping from Octrees                                    | [Paper](https://arxiv.org/pdf/2208.00818.pdf "Paper") | Project                                            | [Github](https://github.com/AndrejOrsula/drl_grasping "Github")        |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |
|                         |                                                                                                  | Paper                                                 | Project                                            | Github                                                                 |

### MLLM

| Name     | Features | 📄Paper | 🌐Project | 📁Github |
| -------- | -------- | ------- | --------- | -------- |
| KOSMOS-E |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |
|          |          | Paper   | Project   | Github   |

## Grasping Dataset

| Name               | Features                                                                                                                                                                                                           | 📄Paper                                                                                                   | 🌐Project                                                          | 📁Github                                                         |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- |
| Dex-Net            | Dexterity Network                                                                                                                                                                                                  | [Paper](https://github.com/BerkeleyAutomation/dex-net/raw/gh-pages/docs/dexnet_rss2017_final.pdf "Paper") | [Project](https://berkeleyautomation.github.io/dex-net/ "Project") | [Github](https://github.com/BerkeleyAutomation/dex-net "Github") |
| Cornell            |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| Jacquard           |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| VMRD               |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| grasp\_multiObject | Robotic grasp dataset for multi-object multi-grasp evaluation with RGB-D data. This dataset is annotated using the same protocal as Cornell Dataset, and can be used as multi-object extension of Cornell Dataset. | Paper                                                                                                     | Project                                                            | [Github](https://github.com/ivalab/grasp_multiObject "Github")   |
| OCID               |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| Grasp-Anything     |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| 6-DoF GraspNet     |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| EGAD               |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| ACRONYM            |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| MetaGraspNet       |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| YCB-Video          |                                                                                                                                                                                                                    | Paper                                                                                                     | Project                                                            | Github                                                           |
| GraspNet-1Billion  |                                                                                                                                                                                                                    |                                                                                                           |                                                                    |                                                                  |
| PID-GraspNet       |                                                                                                                                                                                                                    |                                                                                                           |                                                                    |                                                                  |

## Grasping Simulation

### PyBullet

| Name                 | Features                                                                                                                                                                                                 | 📄Paper                                                     | 🌐Project                                                         | 📁Github                                                                      |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| ur5-robotic-grasping | Learning to Grasp Objects in Highly Cluttered Environments using Deep Convolutional Neural Networks                                                                                                      | [Paper](https://fse.studenttheses.ub.rug.nl/25369/ "Paper") | Project                                                           | [Github](https://github.com/JeroenOudeVrielink/ur5-robotic-grasping "Github") |
| pybullet-robot-envs  | A Python package that collects robotic environments based on the PyBullet simulator, suitable to develop and test Reinforcement Learning algorithms on simulated grasping and manipulation applications. | Paper                                                       | Project                                                           | [Github](https://github.com/hsp-iit/pybullet-robot-envs "Github")             |
| GIGA                 |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
| Edge-Grasp-Network   | grasp generation and process                                                                                                                                                                             | [Paper](https://arxiv.org/abs/2211.00191 "Paper")           | [Project](https://haojhuang.github.io/edge_grasp_page/ "Project") | [Github](https://github.com/HaojHuang/Edge-Grasp-Network/tree/main "Github")  |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |
|                      |                                                                                                                                                                                                          | Paper                                                       | Project                                                           | Github                                                                        |

### ROS+Gazebo

| Name               | Features                                          | 📄Paper                                               | 🌐Project                                                               | 📁Github                                                              |
| ------------------ | ------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------- |
| grasping\_sim      | Leveraging Contact Forces for Learning to Grasp   | [Paper](https://arxiv.org/pdf/1809.07004.pdf "Paper") | Project                                                                 | [Github](https://github.com/machines-in-motion/grasping_sim "Github") |
| grasping in gazebo | Grasping in GAZEBO robotics simulator.            | Paper                                                 | [Project](https://web.tecnico.ulisboa.pt/joao.borrego/grasp/ "Project") | [Github](https://github.com/jsbruglie/grasp "Github")                 |
| airobot            | Robot simulation repository for robotic grasping. | Paper                                                 | Project                                                                 | [Github](https://github.com/rhett-chen/airobot/tree/master "Github")  |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |
|                    |                                                   | Paper                                                 | Project                                                                 | Github                                                                |

## Else Gripper | Else Arm

### Dexterous Grasping

| Name        | Features                                                                                           | 📄Paper                                                       | 🌐Project                                                                  | 📁Github                                                     |
| ----------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------ |
|             | Generalized Anthropomorphic Functional Grasping with Minimal Demonstrations                        | [Paper](http://export.arxiv.org/pdf/2303.17808v1 "Paper")     | Project                                                                    | Github                                                       |
| DexGraspNet | DexGraspNet: A Large-Scale Robotic Dexterous Grasp Dataset for General Objects Based on Simulation | [Paper](https://arxiv.org/pdf/2210.02697.pdf "Paper")         | [Project](https://pku-epic.github.io/DexGraspNet/ "Project")               | [Github](https://github.com/PKU-EPIC/DexGraspNet "Github")   |
| GenDexGrasp | GenDexGrasp: Generalizable Dexterous Grasping                                                      | [Paper](https://arxiv.org/pdf/2210.00722.pdf "Paper")         | [Project](https://tongclass.ac.cn/publication/2022/gendexgrasp/ "Project") | [Github](https://github.com/tengyu-liu/GenDexGrasp "Github") |
| HGC-Net     | HGC-Net: Deep Anthropomorphic Hand Grasping in Clutter                                             | [Paper](https://ieeexplore.ieee.org/document/9811756 "Paper") | Project                                                                    | [Github](https://github.com/yimingli1998/hgc_net "Github")   |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |
|             |                                                                                                    | Paper                                                         | Project                                                                    | Github                                                       |

### Dual-Arm Grasping

| Name | Features                                              | 📄Paper                                               | 🌐Project                                                     | 📁Github                                          |
| ---- | ----------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------- |
| DA2  | DA2 Dataset: Toward Dexterity-Aware Dual-Arm Grasping | [Paper](https://arxiv.org/pdf/2208.00408.pdf "Paper") | [Project](https://sites.google.com/view/da2dataset "Project") | [Github](https://github.com/ymxlzgy/DA2 "Github") |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |
|      |                                                       | Paper                                                 | Project                                                       | Github                                            |

### Suction Grasping

| Name                | Features | 📄Paper | 🌐Project | 📁Github |
| ------------------- | -------- | ------- | --------- | -------- |
| SuctionNet-1Billion |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |
|                     |          | Paper   | Project   | Github   |

### Multi-Fingered Grasping

| Name           | Features                                                                                         | 📄Paper                                               | 🌐Project | 📁Github |
| -------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------- | --------- | -------- |
| EfficientGrasp | EfficientGrasp: A Unified Data-Efficient Learning to Grasp Method for Multi-fingered Robot Hands | [Paper](https://arxiv.org/pdf/2206.15159.pdf "Paper") | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |
|                |                                                                                                  | Paper                                                 | Project   | Github   |

## Research Group

### USA

-   Shuran Song @ Stanford | REAL @ Stanford
-   Ken Goldberg @ Berkeley | [AutoLab @ Berkeley](https://autolab.berkeley.edu/ "AutoLab @ Berkeley")
-   Jeannette Bohg @ Stanford | IPRL Lab @ Stanford
-   Wenzhen Yuan @ UIUC | Touch Lab @ UIUC
-   Yuke Zhu @ UT Austin | RPL @ UT Austin
-   Hao Su @ UCSD | Su Lab @ UCSD
-   Xiaolong Wang @ UCSD
-   IVA Lab @ Georgia Tech(Personnel)
    -   Yunzhi Lin @ Georgia Tech&#x20;
    -   Fu-Jen Chu@ Georgia Tech
    -   grasp\_multiObject
    -   grasp\_multiObject\_multiGrasp
    -   Keypoint-GraspNet

### Europe

-   Danica Kragic @ KTH
-   Hamidreza Kasaei @ University of Groningen | IPL Lab @ University of Groningen

### China

-   Cewu Lu @ STJU | MVIG @ STJU
    -   Haoshu Fang @ STJU
    -   Chenxi Wang @ STJU
    -   Minghao Gou @ STJU
    -   Hongjie Fang @ STJU
-   He Wang @ PKU | EPIC @ PKU
-   Xuguang Lan @ XJTU
-   IRIP Lab @ Beihang University
    -   Haoxiang Ma @ Beihang University
    -   Di Huang @ Beihang University

### Google Deepmind

-   Andy Zeng @ Google Deepmind

## Conference

-   RSS: Robotics: Science and Systems
-   ICRA: IEEE International Conference on Robotics and Automation
-   IROS: IEEE/RSJ International Conference on Intelligent Robots and Systems
-   CoRL: Conference on Robot Learning
-   CVPR: IEEE Conference on Computer Vision and Pattern Recognition
-   ICCV: IEEE International Conference on Computer Vision
-   ECCV: European Conference on Computer Vision
-   NIPS: Conference on Neural Information Processing Systems
-   RA-L: IEEE Robotics and Automation Letters
-   Humanoids: IEEE-RAS International Conference on Humanoid Robots
-   IJRR: The International Journal of Robotics Research
-   ACM MM: ACM International Conference on Multimedia
-   T-RO: IEEE Transactions on Robotics

## Talk

-   [具身智能 —— 上海交大 卢策吾教授](https://www.bilibili.com/video/BV1P8411g7F2/?spm_id_from=333.999.0.0\&vd_source=550553ee94882c45bc7d3dfe65335db4 "具身智能 —— 上海交大 卢策吾教授")

## Video

-   [GraspNet Top-50抓取测试](https://www.bilibili.com/video/BV1ub4y1W7zP/?spm_id_from=333.788.recommend_more_video.15\&vd_source=550553ee94882c45bc7d3dfe65335db4 "GraspNet Top-50抓取测试")

## Book

-   [A Mathematical Introduction to Robotic Manipulation](https://www.cds.caltech.edu/~murray/books/MLS/pdf/mls94-complete.pdf "A Mathematical Introduction to Robotic Manipulation")
-   [Fundamentals Of Robotic Grasping And Fixturing](https://books.google.com.tw/books?id=mlDICgAAQBAJ\&printsec=frontcover\&hl=zh-TW#v=onepage\&q\&f=false "Fundamentals Of Robotic Grasping And Fixturing")
-   [Grasping in Robotics](https://www.springer.com/us/book/9781447146636 "Grasping in Robotics")
-   [Robotic Grasping and Manipulation](https://www.springer.com/us/book/9783319945675 "Robotic Grasping and Manipulation")

## Survey about Robotic Grasping

### Github

-   [Robotic-grasping-papers](https://github.com/rhett-chen/Robotic-grasping-papers "Robotic-grasping-papers")
-   [awesome-grasping](https://github.com/Po-Jen/awesome-grasping "awesome-grasping")
-   [Awesome-Implicit-NeRF-Robotics](https://github.com/zubair-irshad/Awesome-Implicit-NeRF-Robotics "Awesome-Implicit-NeRF-Robotics")
-   [awesome-robotics-libraries](https://github.com/jslee02/awesome-robotics-libraries "awesome-robotics-libraries")

### Paper

-   Deep Learning Approaches to Grasp Synthesis: A Review, \[[Project](https://rhys-newbury.github.io/projects/6dof/ "Project")], \[[Paper](https://arxiv.org/pdf/2207.02556.pdf "Paper")].
-   Robotic Grasping from Classical to Modern: A Survey, \[[Project](https://github.com/ZhangHanbo/Robotic-Grasping-from-Classical-to-Modern-A-Survey "Project")], \[[Paper](https://arxiv.org/pdf/2202.03631.pdf "Paper")].
-   Vision‑based robotic grasping from object localization, object pose estimation to grasp estimation for parallel grippers: a review, \[[Project](https://github.com/GeorgeDu/vision-based-robotic-grasping "Project")], \[[Paper](https://link.springer.com/content/pdf/10.1007/s10462-020-09888-5.pdf "Paper")].
-   [Data-Driven Grasp Synthesis - A Survey](https://arxiv.org/pdf/1309.2660.pdf "Data-Driven Grasp Synthesis - A Survey")

| Name | Features | 📄Paper | 🌐Project | 📁Github |
| ---- | -------- | ------- | --------- | -------- |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |
|      |          | Paper   | Project   | Github   |

## My Ideas

-   Multi-Views?
-   Add depth to the planar grasping
