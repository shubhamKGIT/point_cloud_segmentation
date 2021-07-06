# Project submission to SLAM winter school 2021 
- Group Members
    Shubham Kesharwani <shubham.ksrwn@gmail.com>
    Younès RAOUI <y.raoui@um5r.ac.ma>


- Project Details 

Winter School Project 3
Learning Semantics of 3D Point Clouds.
Supervisor: Tejaswi Digumarti, a postdoctoral research associate at the Australian Centre for Field Robotics
(ACFR), University of Sydney. His research interests include semantic segmentation, mapping, 3D reconstruc-
tion and point cloud analysis. His expertise is in developing these techniques for natural environments. link
Email: tejaswi.digumarti@sydney.edu.au.
Problem description: Understanding what objects are present in a scene or what the constituent parts of an
object are is useful for several robotics applications such as navigation, mapping and interaction. In this project
we will work with 3D point clouds and look at two closely related tasks - object classi cation and semantic
segmentation. In object classi cation, we will try to infer the class of an object by learning geometric features
that are unique to a class and in semantic segmentation, we will assign to every point of the cloud a label that
represents the class it belongs to.
Purpose: This project aims to introduce deep learning based approaches to extracting features in 3D from
point clouds. Point clouds are common outputs of SLAM pipelines and making sense of these reconstructions
is the motivation behind this project. In the context of this workshop, this work  nds use in applications such
as analysis of medical scans, object classi cation for grasping and manipulation, etc.
Main reference: Paper: Qi, Charles R., et al. "Pointnet: Deep learning on point sets for 3d classi cation and
segmentation." Proceedings of the IEEE conference on computer vision and pattern recognition. 2017. link
Code: Skeleton code based on Tensor
ow 2.0 is provided and can be found at
https://github.com/tejaswid/winterschool project code 2021
Dataset: The dataset for this project is the ModelNet 10 dataset. This can be downloaded from here.
Project step: The participants will be asked to complete the following exploration steps based on the provided
code, including:
  Generating the datasets The ModelNet dataset is a collection of CAD models. The  rst step is to
generate point clouds by sampling the models. Using the skeleton code provided, write code to accomplish
this task.
  Building Network This is the most important part of the project. In the provided skeleton code,
key parts of the network are missing and need to be built. Build your network using Tensor
ow 2.0
functions such as \tf.keras.layers.Conv1D", \tf.keras.layers.Dense", \tf.keras.layers.BatchNormalization",
\tf.keras.layers.Dropout", etc. A key task is to implement the T-net which is the core of the proposed
architecture. Use the main reference as your guide. Help is provided in the code. Feel free to play
around with the parameters of the network. You need not follow the exact number of layers and neurons
mentioned in the reference.
  Object classi cation The  rst objective (easy) is to train the network for object classi cation, i.e given
the point cloud of an object the network has to predict a single label specifying what object the point
cloud represents. Evaluate the performance of your network with and without noise added to the sampled
point clouds. Report performance as a confusion matrix.
  Semantic segmentation The second objective (hard) is to train the network for semantic segmentation,
i.e. given a point cloud of a scene, the network has to label each point based on the object class that it
belongs to. For this task you will need to create a custom dataset using the same ModelNet10 dataset.
Create a dataset where each input cloud consists of 2-3 objects. Try to make one of suitable size, with a
range of orientations, placement and overlap of the objects. Report the performance on this task.
References
[1] Qi, Charles R., Hao Su, Kaichun Mo, and Leonidas J. Guibas. "Pointnet: Deep learning on point sets
for 3d classi cation and segmentation." In Proceedings of the IEEE Conference on Computer Vision and
Pattern Recognition (CVPR), 2017.
[2] Z.Wu, S. Song, A. Khosla, F. Yu, L. Zhang, X. Tang and J. Xiao "3D ShapeNets: A Deep Representation for
Volumetric Shapes." In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition,
2015.
