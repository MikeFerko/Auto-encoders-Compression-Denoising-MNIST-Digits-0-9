# Autoencoders for Compression & Denoising of MNIST Digits

Dense-layer autoencoders trained on MNIST to compress digit images and to reconstruct clean images from noisy input.

![Autoencoder network architecture](<https://raw.githubusercontent.com/MikeFerko/Auto-encoders-Compression-Denoising-MNIST-Digits-0-9/main/LAB3-Fig.1.Visualization of Auto-encoder Networks Architecture.jpg>)

- [Notebook](LAB3-Autoencoders_for_Compression_and_Denoising_final.ipynb)

## Approach

- Built a Dense-layer autoencoder (784 to 32 to 64 to 128 to 784, sigmoid output) trained with the Adam optimizer and binary cross-entropy loss for 10 epochs, batch size 128, on clean MNIST digits
- Visualized reconstructed test images alongside the learned encoding (W1) and decoding (W2) weight matrices as image grids
- Added an L1 activity regularizer on the encoding layer and an L2 kernel regularizer, retrained, and compared the resulting weight sparsity and reconstruction quality
- Switched the training/test inputs to a Gaussian-noised version of MNIST while keeping clean images as the target, retraining for 50 epochs to turn the model into a denoising autoencoder
- Deepened the network with two additional Dense layers (64 and 128 units, ReLU) and compared denoising quality and compression against the shallower version
