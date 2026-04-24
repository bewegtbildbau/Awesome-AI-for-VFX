# Awesome AI for VFX
A curated collection of research papers, tools, workflows, and repositories for machine learning in visual effects, with a focus on compositing. (Links are mostly to github. Only to paper if no github available.)

:star: I know of use cases in VFX studios. I put these pretty conservative. Contact me if you know more.
 
:radioactive: Nuke plugin exits.
 
:gear: ComfyUI node exists.

## Roto/Prep

### Mask generation

* :star: :radioactive: :gear:  [SAM 2: Segement Anything](https://github.com/facebookresearch/sam2/) - 2024 - Great to generate segmented masks for all kinds of things. For temping shots these can be great. Somtimes can replace manual rotoscoping.
* :radioactive: :gear: [SAM 3: Segement Anything](https://github.com/facebookresearch/sam3) - 2025 - Not a strict update to SAM2. Concentrates on segmentation via prompts. Masks not as good as SAM2 (?).
* :gear: (older models)  [YOLO](https://github.com/ultralytics/ultralytics) - ongoing development - "object detection, tracking, instance segmentation, image classification, and pose estimation"
* :star: :radioactive: :gear: [ViTMatte](https://github.com/hustvl/ViTMatte) - 2023 - Great for fine detail masks.
  * [ViTMatte Cattery from The Foundry](https://community.foundry.com/cattery/38821/vitmatte)
  * [ViTMatte-for-Nuke](https://github.com/rafaelperez/ViTMatte-for-Nuke)
* [Generative Video Matting](https://github.com/aim-uofa/GVM) - 2025 - Generates video mattes.
* :gear: [VideoMaMa](https://cvlab-kaist.github.io/VideoMaMa/) - 2026 - Improves existing Mattes.
* :radioactive: :gear: [Robust Video Matting](https://github.com/PeterL1n/RobustVideoMatting) - 2021 -Old but fast
  
### Painting

* [Deep Learning-based Image and Video Inpainting: A Survey](https://arxiv.org/abs/2401.03395) - Overview of image and video inpainting mehtods.
* [ProPainter: Improving Propagation and Transformer for Video Inpainting](https://shangchenzhou.com/projects/ProPainter/) - 2023
* [LaMa Image Inpainting, Resolution-robust Large Mask Inpainting with Fourier Convolutions](https://github.com/advimman/lama)
  * [LaMa Cattery](https://community.foundry.com/cattery/38593/lama)

## Compositing

### Keying

* [CorridorKey](https://github.com/nikopueringer/CorridorKey) - 2026 - Key improving and "advanced despilling" / color unmixing.

### Creating layers

* [OmnimatteZero](https://github.com/dvirsamuel/OmnimatteZero) - 2025 - OmnimatteZero creates layers from a video. E.g. an object with shadows/reflections and an inpainted background.

### Creating util layers

* :star: [Depth Anything 3](https://github.com/ByteDance-Seed/Depth-Anything-3/tree/main) - For volumes/particles this can sometimes be enough to integrate elements without the need for rotoscoping/rotomation.
* :star: :gear: [Depth Pro: Sharp Monocular Metric Depth in Less Than a Second](https://github.com/apple/ml-depth-pro)
  * [Depth Pro Cattery](https://community.foundry.com/cattery/38820/depthpro)

### Deblurring

* [FMA-Net: Flow-Guided Dynamic Filtering and Iterative Feature Refinement with Multi-Attention for Joint Video Super-Resolution and Deblurring
] (https://kaist-viclab.github.io/fmanet-site/)

### Dynamic range improvements

* [LEDiff: Latent Exposure Diffusion for HDR Generation](https://lediff.mpi-inf.mpg.de/) - Resotring dynamic range through diffusion.
* [8 bit to half float Copycat](https://movingimagearts.com/8-bit-to-half-float-copycat/) - Recovering highlights and fixing banding from 8 bit images / cattery file for Nuke / trained in Nuke with Arri footage

### Nuke ML Bridges

* :radioactive: [ML Runner](https://github.com/lprestini/ml-runner) - A gizmo in Nuke connectes to a Server which is able to run Models like SAM3 or Depth to Anything 3.
* :radioactive: [Machine Learning Frame Server](https://github.com/TheFoundryVisionmongers/nuke-ML-server) - Nuke node which connects to Python server for inference.

### Nuke MCP Server

* :radioactive: [Nuke-MCP](https://github.com/dughogan/nuke_mcp) - MCP server for Nuke
* :radioactive: [Nuke MCP bridge](https://github.com/flowagent-sh/nuke-mcp) - MCP server for Nuke

## Modeling

* [Trellis 2](https://microsoft.github.io/TRELLIS.2/) - :question: Creating 3d Models from pictures. Would love to know how much this is used.

## Shading/Texturing

* :gear: [CHORD: Generating PBR Materials](https://ubisoft-laforge.github.io/world/chord/)

## Rendering

* Wētā FX ML Denoiser
* Diseny ML Denoiser
* [Intel Open Image Denoiser](https://www.openimagedenoise.org/)

## Gen AI

* :star: [ComfyUI](https://github.com/Comfy-Org/ComfyUI) - Node based tool for ML - Used in production. Node based GUI for diffusion models.

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
