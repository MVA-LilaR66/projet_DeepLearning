# Deep Learning Project for MVA

## Paper Reference
The project is based on the papers:  
**[An Image is Worth 16X16 Words: Transformers For Image Recognition at Scale](https://arxiv.org/pdf/2010.11929)** \
**[Training a Vision Transformer from scratch in less than 24 hours with 1 GPU](https://https://arxiv.org/pdf/2211.05187)** 

In this project, we reimplemented our own Vision Transformer (ViT) from scratch, improving upon the implementation found in:  
**[Implementing Vision Transformer (ViT) from Scratch](https://towardsdatascience.com/implementing-vision-transformer-vit-from-scratch-3e192c6155f0)**

## Authors
- **Lila Roig**
- **Romane Barra**

## Professor
- **V. Lepetit**

## Project Structure

- **biblio**: Papers on which the project is based.
- **code**:
    - **experiments**: Directory containing saved models.
    - **LilaRoig_RomaneBarraDeepLearningProject.ipynb**: Jupyter notebook containing the full code for the project.
- **RomaneBarra_LilaRoig_Poster_ViT.pdf**: Project poster.

## Modifications and Improvements

In this project, we implemented several improvements and new functionalities compared to the code provided by [Implementing Vision Transformer (ViT) from Scratch](https://towardsdatascience.com/implementing-vision-transformer-vit-from-scratch-3e192c6155f0). 

- **Extensive commenting**: All functions have been thoroughly documented.
  
- **Training interruption and resumption**: We added the ability to **pause** and **resume training** at any point, preserving the model's state for later continuation.

- **Network visualization**: We modified the code to visualize various components of the ViT during the forward pass, such as:
  - **Activations** of the learned **Patch Embeddings**.
  - **Learned weights** of the **Patch Embeddings**.
  - **Position Embeddings**.
  - **Attention Scores** between patches.

- **Performance optimizations**:
  - **Locality enhancement**: We incorporated a **depth-wise 3x3 convolution** into the Feed Forward module. This allows the model to better capture local spatial relationships between image patches. 
  
  - **Curriculum learning**: We introduced a strategy where training starts with **low-resolution images** and progressively increases the resolution over the epochs. This helps the model learn simpler patterns first and gradually tackle more complex features, improving overall generalization. 
