# 3D-Content-creation-and-refinement

This repository focuses on generating diverse 3D point clouds from single-view 2D RGB images. The project utilizes a pretrained architecture known as 3DAttributeFlow to achieve this.

# Introduction

In this approach, we perform interpolation in the latent space between a source and a target, enabling the generation of a wide range of 3D point clouds. This method leverages the capabilities of the pretrained model to produce diverse and visually appealing 3D content from 2D inputs.

# System architecture

![_final_block_diagram _001](https://github.com/user-attachments/assets/c7025849-8b59-4a47-b1a4-00ac826167c7)


In this apporach we take two images, one as source and one as target, we perform feature extraction by leveraging pretrained resnet-18 architecture, then in the obtained feature vector we perform interpolation (cosine as well as linear) and pass this feature vector to the pretrained 3D Attribute Flow which reconstructs 3D point clouds, thereby generating diverse 3D point clouds from single view 2D RGB images.

# Results from Inter-class interpolation.

![Plane2car 002](https://github.com/user-attachments/assets/789eb998-8c49-4228-b480-3012868019b4)

Source is plane and target is car and intermediate point clouds represent output from that interpolation step, dataset used was shapenet rendered images.

# Results from Intra-class interpolation.

![car2car 001](https://github.com/user-attachments/assets/2aa6f603-fa9a-4f48-9896-8d021f4c8619)

Source is car type1 and target is car type2 and intermediate point clouds represent output from that interpolation step, dataset used was shapenet rendered images.

# Results from combining geometric style and semantic attributes.

![chair_combined2 001](https://github.com/user-attachments/assets/fb3589b6-49e1-4d08-8b14-1e5f937d9789)


Here we combine the geomtric style from chair 1 along with semantic attributes of chair 2 to generate a 3D point cloud with overall geometry as chair 1 and having semantics of chair 2.

# Results from varying parameters of latent vector

<img width="1124" alt="PlaneLen (1)" src="https://github.com/user-attachments/assets/e01b0c12-11f6-40ae-a90f-b1a0370403be">

Here we vary the 5th dimension of the latent vector to observe changes in the length of the wings. (Red one) represents no varied parameter, hence no change in the length of the wings, while (Blue one) is with the 5th parameter varied to observe the change in the length of its wings.
