# 3D-Content-creation-and-refinement

This repository focuses on generating diverse 3D point clouds from single-view 2D RGB images. The project utilizes a pretrained architecture known as 3DAttributeFlow to achieve this.

# Introduction

In this approach, we perform interpolation in the latent space between a source and a target, enabling the generation of a wide range of 3D point clouds. This method leverages the capabilities of the pretrained model to produce diverse and visually appealing 3D content from 2D inputs.

# System architecture

![_final_block_diagram _001](https://github.com/user-attachments/assets/c7025849-8b59-4a47-b1a4-00ac826167c7)


In this apporach we take two images, one as source and one as target, we perform feature extraction by leveraging pretrained resnet-18 architecture, then in the obtained feature vector we perform interpolation (cosine as well as linear) and pass this feature vector to the pretrained 3D Attribute Flow which reconstructs 3D point clouds, thereby generating diverse 3D point clouds from single view 2D RGB images.

# Results from Inter-class interpolation.
