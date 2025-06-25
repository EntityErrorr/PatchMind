# PatchMind: Masked Patch Prediction Using Vision Transformers

PatchMind is a lightweight self-supervised learning project that reconstructs masked image patches using a Vision Transformer (ViT). Inspired by MAE (Masked Autoencoders), it teaches ViT to learn visual features without labels using CIFAR-10.

## Highlights
- Masked patch prediction with ViT encoder and MLP decoder
- Trained on CIFAR-10 with 75% patch masking
- Built for low-resource GPUs 

## Results & Analysis

The model successfully learns to reconstruct missing image regions from heavily masked (75%) input images. While fine details are often lost, the overall color distribution, object layout, and semantic structure are preserved to a reasonable extent. 

This demonstrates the effectiveness of self-supervised learning using Vision Transformers, even on small datasets like CIFAR-10. The learned embeddings capture useful visual features without any label supervision.

### Observations:
- Reconstructed patches match general object position and color tones.
- Performance improves steadily with more epochs (and lower masking ratio).
- Slight blurriness in reconstructions is expected due to simple MLP decoder.

This project shows that Vision Transformers can be effectively used for self-supervised masked image modeling, even in low-resource environments. By reconstructing masked patches, the model learns rich representations that can potentially transfer well to other tasks.

### Future Work:
- Replace MLP decoder with a CNN or Transformer-based decoder
- Train on higher-res images or medical datasets
- Fine-tune the encoder on classification downstream tasks
