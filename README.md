# MISC
**The official repo for [MISC: Ultra-low Bitrate Image Semantic Compression Driven by Large Multimodal Model](https://arxiv.org/abs/2402.16749)**
<div align="center">

 <div style="width: 80%; text-align: center; margin:auto;">
      <img style="width: 80%" src="spotlight.png">
 </div> 
</div>

## Dependency

[GPT-4 Vision](https://openai.com/)

[CLIP_Surgery](https://github.com/xmed-lab/CLIP_Surgery/)

[Stable Diffusion 2.1](https://hf-mirror.com/stabilityai/stable-diffusion-2-1)

[DiffBIR](https://github.com/XPixelGroup/DiffBIR/)

[CompressAI](https://github.com/InterDigitalInc/CompressAI)

## Instruction

Download weights and put them into the weight folder:

DiffBIR (general_full_v1.ckpt): [link](https://hf-mirror.com/lxq007/DiffBIR-v2/resolve/main/v1_general.pth)
Cheng2020-Tuned (cheng_small.pth.tar): [link](https://www.dropbox.com/scl/fi/br0zu6a91wygs68afesyo/cheng_small.pth.tar?rlkey=2gdhpy3z5qank0giajacj2u9p&st=9q2y88aj&dl=0)

If you want to use 'mask', download the [CLIP_Surgery](https://github.com/xmed-lab/CLIP_Surgery/) model. Put the `clip' folder in the same directory as this project.

Run the ipynb code in different modes to decompress the image!

1. If you want pixel-instructed decoding, set the mode as 'pixel', a larger `block_num_min' means more pixels, with a larger bpps cost.

2. If you want net-instructed decoding, set the mode as 'net' to use our fine-tuned Cheng-2020 net. You can also use your own net weight trained by [CompressAI](https://github.com/InterDigitalInc/CompressAI).

3. If you want to use other models (like VVC, HiFiC, ...) as the starting point of diffusion, set the mode as 'ref', run your own model, and give the decompressed image and the bpps of your model.

## Demo
[Feb 29, 2024] A simple Jupyter demo is uploaded. The encoder and decoder model weights will be uploaded soon.

[Apr 24, 2024] The model weights are uploaded. Please follow the instruction when using the ipynb file. We are working on a pipeline for en/decoding a group of image.

## Visualzation Result
<div align="center">

 <div style="width: 80%; text-align: center; margin:auto;">
      <img style="width: 80%" src="example.png">
 </div> 
</div>

## Citation
If you find our work useful, please cite our paper as:
```
@misc{li2024misc,
      title={MISC: Ultra-low Bitrate Image Semantic Compression Driven by Large Multimodal Model}, 
      author={Chunyi Li and Guo Lu and Donghui Feng and Haoning Wu and Zicheng Zhang and Xiaohong Liu and Guangtao Zhai and Weisi Lin and Wenjun Zhang},
      year={2024},
      eprint={2402.16749},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
```
