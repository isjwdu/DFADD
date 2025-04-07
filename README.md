# DFADD: The Diffusion and Flow-matching based Audio Deepfake Dataset

<p align="center">  
    <a href="https://arxiv.org/abs/2409.08731">Paper</a>, 
    <a href="https://huggingface.co/datasets/isjwdu/DFADD">Dataset</a>, 
    <a href="https://github.com/DFADD-Dataset/DFADD_demo_pages/">Demo</a>, 
    <a href="https://github.com/isjwdu/DFADD">Homepage</a> 
</p>
<p align="center">  
    <i>SLT 2024</i>
</p>

#### Updates
[04/2025] We fixed the mismatch between Matcha TTS audio and labels, and unified all audio formats. Please download the ZIP file for the updated data.

[11/2024] We provide checkpoint training on Unofficial PFlow-TTS.

[09/2024] We release all DFADD datasets on Huggingface.

## Key Features: 
1. DFADD is the first dataset that includes spoofed speech generated specifically using diffusion and Flow-matching based TTS models.

2. Compared to anti-spoofing models trained on the ASVspoof, models trained on DFADD exhibit better Equal Error Rates (EERs) when confronted with spoofed speech generated using the same methods.

## Dataset Download
1. [HuggingFace dataset](https://huggingface.co/datasets/isjwdu/DFADD)

```
from datasets import load_dataset
DFADD = load_dataset('isjwdu/DFADD')
```

2. [**ZIP files**](https://huggingface.co/datasets/isjwdu/DFADD/tree/main)

The zip file was updated in Apr. 2025.
Please merge the VCTK_BONAFIDE into each DFADD subset.

## Checkpoint Download
For those interested in PFlow, we provide checkpoints trained for 1100 epochs on V100-32G.

[Download PFlow Checkpoint](https://huggingface.co/datasets/isjwdu/DFADD/resolve/main/pflowtts_checkpoint_epoch%3D1099.ckpt)

or
```
wget https://huggingface.co/datasets/isjwdu/DFADD/resolve/main/pflowtts_checkpoint_epoch%3D1099.ckpt
```

To generate speech for a VCTK speaker, follow [PFlow-TTS](https://github.com/p0p4k/pflowtts_pytorch) with the vocoder replaced by [HiFi-GAN VCTK_V1](https://drive.google.com/drive/folders/1vJlfkwR7Uyheq2U5HrPnfTm-tzwuNuey?usp=sharing) pre-trained on VCTK

## Acknowledgement
DFADD is created based on several official and unofficial open-source implementations and datasets:

[VCTK](https://datashare.ed.ac.uk/handle/10283/3443) dataset, licensed under CC-BY-4.0.

[LJ Speech](https://keithito.com/LJ-Speech-Dataset) dataset, licensed under Public Domain.

Hifi-GAN Vocoder (Official), https://github.com/jik876/hifi-gan.

PFlow-TTS (Unofficial), https://github.com/p0p4k/pflowtts_pytorch.

NaturalSpeech2 (Unofficial), https://github.com/CODEJIN/NaturalSpeech2.

Grad-TTS (Official), https://github.com/huawei-noah/Speech-Backbones/tree/main/Grad-TTS.

Style-TTS2 (Official), https://github.com/yl4579/StyleTTS2.

Matcha-TTS (Official), https://github.com/shivammehta25/Matcha-TTS.

## Citation
Please consider citing our paper if this work helps your research. Thank you!
```
@inproceedings{du2024dfadd,
  title={DFADD: The Diffusion and Flow-Matching Based Audio Deepfake Dataset},
  author={Du, Jiawei and Lin, I-Ming and Chiu, I-Hsiang and Chen, Xuanjun and Wu, Haibin and Ren, Wenze and Tsao, Yu and Lee, Hung-yi and Jang, Jyh-Shing Roger},
  booktitle={2024 IEEE Spoken Language Technology Workshop (SLT)},
  pages={921--928},
  year={2024},
  organization={IEEE}
}
```
