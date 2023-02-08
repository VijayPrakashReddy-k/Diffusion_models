## 📌 Hierarchical Text-Conditional Image Generation with CLIP Latents (Dall-e-2)

*There are the four key high-level concepts:*

    • CLIP: Model that takes image-caption pairs and creates “mental” representations in the form of vectors, called text/image embeddings.

    • Prior model: Takes a caption/CLIP text embedding and generates CLIP image embeddings.

    • Decoder Diffusion model (unCLIP): Takes a CLIP image embedding and generates images.

    • DALL·E 2: Combination of prior + diffusion decoder (unCLIP) models.
