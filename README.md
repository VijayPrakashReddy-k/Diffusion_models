## ✨ Diffusion Models:

*Denoising diffusion models are a new and promising area of research in computer vision, with great success in generative modeling. They consist of two stages:* 

**1. A forward stage in which input data is gradually altered by adding noise, and** <br>  **2. A reverse stage in which the model attempts to recover the original data by gradually reversing the diffusion process.** <br> <br>*These models are well-regarded for the high quality and variety of the generated samples they produce, but they have the drawback of being computationally slow due to the large number of steps involved during sampling.*

## 🔎 Evaluation Metrics:

Following are widely used methods for measuring the similarity between images.

**1.IS (Inception Score)**:

Inception Score (IS) is a widely used metric for evaluating the quality of generated images. It is based on a combination of two factors: **Image quality and Image diversity.**

To calculate the IS, a pre-trained deep neural network, usually Inception-v3, is used to classify the generated images into different categories. The scores of the softmax outputs of the network for each image are averaged to obtain a measure of image quality. A higher score indicates better quality.

To measure image diversity, the entropy of the conditional distribution of the class labels given the generated images is calculated. A higher entropy indicates greater diversity.

The final IS score is the exponential of the average of these two factors. The higher the IS score, the better the generated images are considered to be in terms of both quality and diversity.

However, IS has been criticized for not capturing certain aspects of image quality and diversity, such as the presence of specific objects or the perceptual similarity between images. Additionally, IS is sensitive to the choice of the feature extractor and the number of categories used for classification, which can impact its usefulness as a general-purpose metric.

**2. FID (Fréchet Inception Distance):**

FID (Fréchet Inception Distance) is a commonly used metric for evaluating the quality of generated images. It is based on the Fréchet distance between two multivariate Gaussians that model the feature representations of real and generated images, respectively.

Specifically, FID calculates the distance between the mean and covariance of the feature representations of real and generated images, which are extracted from a pre-trained deep neural network, usually Inception-v3. The lower the FID score, the closer the distribution of generated images is to that of real images, indicating better quality.

FID is considered to be a more reliable metric than others, such as Inception Score (IS), because it takes into account both the quality and diversity of generated images. However, FID requires access to the real images for comparison, which may not always be feasible in some applications. Additionally, FID is sensitive to the size of the dataset and the choice of the feature extractor, which can impact its usefulness as a general-purpose metric.

**3. SSIM (Structure Similarity Index Measure):**

The Structure Similarity Index Measure (SSIM) is a widely used metric for evaluating the similarity between two images. It measures the structural similarity between the two images by comparing their **luminance, contrast, and structure.**

The SSIM index ranges from -1 to 1, where 1 indicates perfect similarity. A value of 0 means there is no similarity between the two images, while a negative value indicates that the two images are dissimilar and may have opposite contrast or structure.

The SSIM index is calculated by comparing the local windows of the two images and calculating the mean, variance, and covariance of the luminance, contrast, and structure in each window. The SSIM index is then obtained as a weighted sum of the luminance, contrast, and structure similarity measures, with the weights determined by a set of empirically derived constants.

SSIM is commonly used in image and video compression applications, as well as in image restoration and enhancement tasks. However, it has some limitations, such as its sensitivity to changes in the local window size and the fact that it may not always align with human perception of image similarity.

**4. LPIPS (Learned Perceptual Image Patch Similarity):**

Learned Perceptual Image Patch Similarity (LPIPS) is a metric for evaluating the similarity between two images that is designed to align with human perception. LPIPS measures the perceptual distance between two images by comparing their feature representations extracted from a pre-trained deep neural network.

The feature representations are obtained by passing the images through a deep neural network, such as VGG or AlexNet, and extracting features at multiple layers of the network. The feature maps are then compared patch-wise using a distance metric, such as the L2 distance, to obtain a measure of the perceptual similarity between the images.

LPIPS has been shown to be more reliable than traditional image similarity metrics, such as SSIM, in capturing the perceptual differences between images, especially in scenarios where the images have been distorted or manipulated. It has also been used in various applications, such as image and video compression, image super-resolution, and style transfer.

However, LPIPS may not always align with human perception in all scenarios, and its performance may vary depending on the choice of the pre-trained network and the distance metric used. Additionally, LPIPS may be computationally expensive due to the need to extract features from deep neural networks.
