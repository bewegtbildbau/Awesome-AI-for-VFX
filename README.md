# Awesome AI for VFX
A curated collection of research papers, tools, workflows, and repositories for machine learning in visual effects, with a focus on compositing. 

I am mostly interested where ML can help with the chore of our work.

:star: I heard of use cases in VFX studios. I put these pretty conservative. Contact me if you know more.
 
:radioactive: Nuke plugin exits.
 
:gear: ComfyUI node exists.

Links are mostly to github. Only to paper if no github available.

## Roto/Prep

### Mask generation

* :gear: [VideoMaMa](https://cvlab-kaist.github.io/VideoMaMa/) - 2026 - Improves existing Mattes.
* :gear: (older models)  [YOLO](https://github.com/ultralytics/ultralytics) - ongoing development - "object detection, tracking, instance segmentation, image classification, and pose estimation"
* [Generative Video Matting](https://github.com/aim-uofa/GVM) - 2025 - Generates video mattes.
* :radioactive: :gear: [SAM 3: Segement Anything](https://github.com/facebookresearch/sam3) - 2025 - Not a strict update to SAM2. Concentrates on segmentation via prompts. Masks not as good as SAM2 (?).
* :star: :radioactive: :gear:  [SAM 2: Segement Anything](https://github.com/facebookresearch/sam2/) - 2024 - Great to generate segmented masks for all kinds of things. For temping shots these can be great. Somtimes can replace manual rotoscoping.
* :star: :radioactive: :gear: [ViTMatte](https://github.com/hustvl/ViTMatte) - 2023 - Great for fine detail masks.
  * [ViTMatte Cattery from The Foundry](https://community.foundry.com/cattery/38821/vitmatte)
  * [ViTMatte-for-Nuke](https://github.com/rafaelperez/ViTMatte-for-Nuke)
* :radioactive: :gear: [Robust Video Matting](https://github.com/PeterL1n/RobustVideoMatting) - 2021 -Old but fast
  
### Painting

* [VOID: Video Object and Interaction Deletion](https://github.com/Netflix/void-model) - 2026
* [SVOR (Stable Video Object Removal)](https://github.com/xiaomi-research/svor/) - 2025
* [MiniMax-Remover](https://github.com/zibojia/MiniMax-Remover) - 2025
* [Deep Learning-based Image and Video Inpainting: A Survey](https://arxiv.org/abs/2401.03395) - 2024 - Overview of image and video inpainting mehtods.
* [ProPainter: Improving Propagation and Transformer for Video Inpainting](https://shangchenzhou.com/projects/ProPainter/) - 2023
* :star: [LaMa Image Inpainting, Resolution-robust Large Mask Inpainting with Fourier Convolutions](https://github.com/advimman/lama) - 2022
  * :radioactive: [LaMa Cattery](https://community.foundry.com/cattery/38593/lama)

## Compositing

### Keying

* [CorridorKey](https://github.com/nikopueringer/CorridorKey) - 2026 - Key improving and "advanced despilling" / color unmixing.

### Creating layers

* [OmnimatteZero](https://github.com/dvirsamuel/OmnimatteZero) - 2025 - OmnimatteZero creates layers from a video. E.g. an object with shadows/reflections and an inpainted background.

### Creating util layers

* :gear: [RollingDepth](https://github.com/prs-eth/rollingdepth) - 2025
* :star: [Depth Crafter](https://depthcrafter.github.io/) - 2025
  * :radioactive: [DepthCrafter for Nuke](https://github.com/Theo-SAMINADIN-td/NukeDepthCrafter)
* :star: [Depth Anything 3](https://github.com/ByteDance-Seed/Depth-Anything-3/tree/main) - 2025
  * :radioactive: [Depth Anything 3 for Nuke](https://github.com/petermercell/Depth-Anything-3-for-Nuke)
* :star: :gear: [Depth Pro: Sharp Monocular Metric Depth in Less Than a Second](https://github.com/apple/ml-depth-pro) - 2025
  * :radioactive: [Depth Pro Cattery](https://community.foundry.com/cattery/38820/depthpro)


### Deblurring

* [FMA-Net: Flow-Guided Dynamic Filtering and Iterative Feature Refinement with Multi-Attention for Joint Video Super-Resolution and Deblurring](https://kaist-viclab.github.io/fmanet-site/)

### Dynamic range improvements

* [LEDiff: Latent Exposure Diffusion for HDR Generation](https://lediff.mpi-inf.mpg.de/) - Resotring dynamic range through diffusion.
* [8 bit to half float Copycat](https://movingimagearts.com/8-bit-to-half-float-copycat/) - Recovering highlights and fixing banding from 8 bit images / cattery file for Nuke / trained in Nuke with Arri footage

### Nuke ML Bridges

* :radioactive: [ML Runner](https://github.com/lprestini/ml-runner) - A gizmo in Nuke connectes to a Server which is able to run Models like SAM3 or Depth to Anything 3.
* :radioactive: [Machine Learning Frame Server](https://github.com/TheFoundryVisionmongers/nuke-ML-server) - Nuke node which connects to Python server for inference.

### Nuke MCP Server

* :radioactive: [Nuke-MCP](https://github.com/dughogan/nuke_mcp) - MCP server for Nuke
* :radioactive: [Nuke MCP bridge](https://github.com/flowagent-sh/nuke-mcp) - MCP server for Nuke

## Gaussion Splats

* [3D Gaussian Splatting for Real-Time Radiance Field Rendering](https://arxiv.org/abs/2308.04079) - obviously a big topic and implemented in Nuke 17 already but as an honorable mention 

## Modeling

* [Trellis 2](https://microsoft.github.io/TRELLIS.2/) - :question: Creating 3d Models from pictures. Would love to know how much this is used.

## Shading/Texturing

* :gear: [CHORD: Generating PBR Materials](https://ubisoft-laforge.github.io/world/chord/)

## Rendering

* Wētā FX ML Denoiser
* Diseny ML Denoiser
* [Intel Open Image Denoiser](https://www.openimagedenoise.org/)

## Gen AI

I am  not going to cover the (very fast) moving field of Gen AI. I am going to list some interesting finds in this realm.

* :star: [ComfyUI](https://github.com/Comfy-Org/ComfyUI) - Node based tool for ML - Used in production. Node based GUI for diffusion models.

### transparency for diffusion

* [Transparent Image Layer Diffusion using Latent Transparency](https://github.com/lllyasviel/LayerDiffuse) - 2024 - repo basically empty - some other implementations seem to exist

### going beyond 1.0: HDR

* :gear: [ComfyUI HDR VAE Decode Node](https://github.com/netocg/vae-decode-hdr) - Looks quite intereisting. Original repo is down. Seems to be the same appraoch as LEDiff (see above).

## Data Sets

These sets come with different metadata like descriptions, segmentations and classifications.

 * [CelebA HQ](https://github.com/switchablenorms/CelebAMask-HQ) - 30.000 cropped images of heads / 1024*1024 / 2.8 GB
 * [Flickr-Faces-HQ Dataset ](https://github.com/NVlabs/ffhq-dataset) - 70.000 / 1024*1024 / 89 GB
 * [Places365-Standard](http://places2.csail.mit.edu/download.html) - Train(105GB)/Test(19GB)/Val(2.1GB)

          wget http://data.csail.mit.edu/places/places365/train_large_places365standard.tar
          wget http://data.csail.mit.edu/places/places365/val_large.tar
          wget http://data.csail.mit.edu/places/places365/test_large.tar
          https://hyper.ai/en/datasets/9427

  * Places365-Challenge - around 8 million images
  * [ADE20K](https://ade20k.csail.mit.edu/)
  * [Imagenet](https://www.kaggle.com/c/imagenet-object-localization-challenge/overview/description)
    * [Download from Kaggle](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data) - 1.2 Million images / 167 GB
  * [Open Images Dataset](https://storage.googleapis.com/openimages/web/index.html)
  * [Dynamic Replica](https://dynamic-stereo.github.io/) - synthetic data set containing several util layers / approx 140.000 frames in voer 500 videos / 1280*720
  * [BEDLAM](https://bedlam.is.tue.mpg.de/) - synthetic data set containing several util layers / 10.450 image sequences / 1280*720

## Conferences

* [Siggraph](https://www.siggraph.org/) - THE conference for computer graphics
* [CVPR](https://cvpr.thecvf.com/) - THE conferfence for computer vision

## Research Overview

* [Artificial Intelligence in Creative Industries: Advances Prior to 2025](https://arxiv.org/html/2501.02725v4)

## Some talks and more general info about the use of AI in VFX

* [Roto and Prep in the age of AI | a Visual Effects Society London Event](https://www.youtube.com/watch?v=NDEKzBeOcZ4) - 2026 - good overview of what studios and software companies are working on
* [Real Applications of Gen AI in Visual Effects](https://vimeo.com/1060631070) - 2025 - not touching VFX studio workflows a lot
* [Let's talk about AI and the VFX industry | Leading CGI experts panel](https://www.youtube.com/watch?v=1t778a3AfyI) - 2025 - pretty top level e.g. ethics of usage
* [How Generative AI Might Affect VFX Now and In the Future](https://vimeo.com/933093258) - 2024 - very good overview and not just about GenAI
