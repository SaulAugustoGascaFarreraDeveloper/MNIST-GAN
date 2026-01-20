# MNIST-GAN
This project implements a Generative Adversarial Network (GAN) from scratch using PyTorch, trained on the MNIST handwritten digits dataset.

The goal is to learn the underlying data distribution of handwritten digits and generate new synthetic digit images that resemble real MNIST samples.

The project focuses on understanding the core mechanics of GANs, including:

    Generator and Discriminator architectures

    Adversarial training dynamics

    Loss functions and stability considerations

    Latent space sampling and image generation


<img width="2041" height="782" alt="Screenshot 2026-01-12 165711" src="https://github.com/user-attachments/assets/f6b70eac-0789-4648-bbf6-ba9befafc656" />



🧩 Model Architecture
Generator

  Fully connected (MLP-based) architecture
  
  Input: random noise vector 
    𝑧
    ∼
    𝑁
    (
    0
    ,
    1
    )
    z∼N(0,1)

Output: flattened 28×28 image (784 values)

  Uses:

    Linear layers
    
    Batch Normalization
    
    ReLU activations
    
    Sigmoid activation in the output layer

  Discriminator

    Fully connected (MLP-based) architecture
    
    Input: flattened image (real or generated)
    
    Output: probability of being a real image

Uses:

    Linear layers
    
    LeakyReLU activations
    
    Binary classification objective

⚙️ Training Setup

    Dataset: MNIST
    
    Image size: 28×28 (grayscale)
    
    Loss function: Binary Cross-Entropy (BCE)
    
    Optimizer: Adam
    
    Batch size: 128
    
    Latent dimension: 64
  
    Training epochs: 500
    
    Device: GPU (CUDA) NVDIA RTX 5070 Ti 

  📊 Results

  After 500 training epochs in 1.5 hours, the Generator is able to produce recognizable handwritten digits with reasonable diversity.
  
    ✔ Digits are clearly identifiable
    ✔ Multiple digit classes are generated
    ✔ No complete mode collapse observed
  
  However, the generated images are not perfectly sharp or realistic, which is expected given the model design.

  Some Images form my Results:

  <img width="610" height="873" alt="Screenshot 2026-01-11 215100" src="https://github.com/user-attachments/assets/e4a94227-0d2e-41f5-85b5-57308f3f6e9c" />
  
  <img width="456" height="825" alt="Screenshot 2026-01-12 171309" src="https://github.com/user-attachments/assets/f164efc7-2eee-44be-b7ed-06421f8a08e4" />


  

  

    

