# Awesome AI for VFX
A curated collection of research papers, tools, workflows, and repositories for machine learning in visual effects, with a focus on compositing.

## Roto/Prep

* :star: [SAM 3: Segement Anything](https://github.com/facebookresearch/sam3) - Used in productions. Great to generate masks for all kinds of things. For temping shots these can be great. Somtimes can replace manual rotoscoping.

### Painting

* [Deep Learning-based Image and Video Inpainting: A Survey](https://arxiv.org/abs/2401.03395) - Overview of image and video inpainting mehtods.
* [ProPainter: Improving Propagation and Transformer for Video Inpainting](https://shangchenzhou.com/projects/ProPainter/)

###

## Compositing

###

### Creating util layers

* :star: [Depth Anything 3](https://github.com/ByteDance-Seed/Depth-Anything-3/tree/main) - This is already heavily used in productions. For volumes/particles this can sometimes be enough to integrate elements without the need for rotoscoping/rotomation. 

### Deblurring

[FMA-Net: Flow-Guided Dynamic Filtering and Iterative Feature Refinement with Multi-Attention for Joint Video Super-Resolution and Deblurring
] (https://kaist-viclab.github.io/fmanet-site/)

### Dynamic range improvements

* [LEDiff: Latent Exposure Diffusion for HDR Generation](https://lediff.mpi-inf.mpg.de/) - Resotring dynamic range through diffusion.
* [8 bit to half float Copycat](https://movingimagearts.com/8-bit-to-half-float-copycat/) - Recovering highlights and fixing banding from 8 bit images / cattery file for Nuke / trained in Nuke with Arri footage

### ML Runner

* [ML Server](https://github.com/lprestini/ml-runner) - A gizmo in Nuke connectes to a Server which is able to run Models like SAM3 or Depth to Anything 3.
* [Nuke ML Server](https://github.com/TheFoundryVisionmongers/nuke-ML-server) - Nuke node which connects to Python server for inference.

### Nuke MCP Server

* [MCP Server and Tool code for Nuke](https://github.com/dughogan/nuke_mcp)
* [Another Nuke MCP](https://github.com/flowagent-sh/nuke-mcp)

## Matte Painting

## Matchmove

## FX

## Modeling

* [Trellis 2](https://microsoft.github.io/TRELLIS.2/) - :question: Creating 3d Models from pictures. Would love to know how much this is used.

## Shading/Texturing

* [CHORD: Generating PBR Materials](https://ubisoft-laforge.github.io/world/chord/)

## Ligthing

## Rendering

* Wētā FX ML Denoiser
* Diseny ML Denoiser
* [Intel Open Image Denoiser](https://www.openimagedenoise.org/)

## Animation

## VFX Editing

## Pipeline

## Production

## Gen AI

* :star: [ComfyUI: Nuke for Models](https://github.com/Comfy-Org/ComfyUI) - Used in production. Node based GUI for diffusion models.

### going beyond 1: HDR

* [ComfyUI HDR VAE Decode Node](https://github.com/netocg/vae-decode-hdr) - Looks quite intereisting. Original repo is down. Seems to be the same appraoch as LEDiff (see above).

### Video

### Stills

## World Buidling AI

## More Infos and Sources

### Data Sets

These sets come with different metadata like descriptions, segmentations and classifications.

 * [CelebA HQ](https://github.com/switchablenorms/CelebAMask-HQ) - 30.000 cropped images of heads / 1024*1024 / 2.8 GB
 * [Flickr-Faces-HQ Dataset ](https://github.com/NVlabs/ffhq-dataset) - 70.000 / 1024*1024 / 89 GB
 * [Places365-Standard](http://places2.csail.mit.edu/download.html): Train(105GB)/Test(19GB)/Val(2.1GB)

          wget http://data.csail.mit.edu/places/places365/train_large_places365standard.tar
          wget http://data.csail.mit.edu/places/places365/val_large.tar
          wget http://data.csail.mit.edu/places/places365/test_large.tar
          https://hyper.ai/en/datasets/9427

  * Places365-Challenge - around 8 million images
  * [ADE20K](https://ade20k.csail.mit.edu/)
  * [Imagenet](https://www.kaggle.com/c/imagenet-object-localization-challenge/overview/description)
    * [Download from Kaggle](https://www.kaggle.com/competitions/imagenet-object-localization-challenge/data) - 1.2 Million images / 167 GB
  * [Open Images Dataset](https://storage.googleapis.com/openimages/web/index.html)

### Conferences

* [Siggraph: THE conference for computer graphics](https://www.siggraph.org/)
* [CVPR: THE conferfence for computer vision](https://cvpr.thecvf.com/)

### Research Overview

* [Artificial Intelligence in Creative Industries: Advances Prior to 2025](https://arxiv.org/html/2501.02725v4)
