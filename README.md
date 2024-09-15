# DFADD: The Diffusion and Flow-matching based Audio Deepfake Dataset

<p align="center">  
    <a href="">Paper</a>, 
    <a href="https://huggingface.co/datasets/isjwdu/DFADD">Dataset</a>, 
    <a href="https://github.com/DFADD-Dataset/DFADD_demo_pages/">Demo</a>, 
    <a href="https://github.com/isjwdu/DFADD">Homepage</a> 
</p>
<p align="center">  
    <i>SLT 2024</i>
</p>

**Key Features**: 
1. DFADD is the first dataset that includes spoofed speech generated specifically using diffusion and Flow-matching based TTS models.

2. Compared to anti-spoofing models trained on the ASVspoof, models trained on DFADD exhibit better Equal Error Rates (EERs) when confronted with spoofed speech generated using the same methods.

## Dataset Download

1. [HuggingFace dataset](https://huggingface.co/datasets/isjwdu/DFADD)

```
from datasets import load_dataset
DFADD = load_dataset('isjwdu/DFADD')
```

2. [**ZIP files**](https://huggingface.co/datasets/isjwdu/DFADD/tree/main)

## Acknowledgement

DFADD is created based on several official and unofficial open-source implementations and datasets:

[VCTK](https://datashare.ed.ac.uk/handle/10283/3443) dataset, licensed under CC-BY-4.0.

[LJ Speech](https://keithito.com/LJ-Speech-Dataset) dataset, licensed under Public Domain.

PFlow-TTS (Unofficial), https://github.com/p0p4k/pflowtts_pytorch.

NaturalSpeech2 (Unofficial), https://github.com/CODEJIN/NaturalSpeech2.

Grad-TTS (Official), https://github.com/huawei-noah/Speech-Backbones/tree/main/Grad-TTS.

Style-TTS2 (Official), https://github.com/yl4579/StyleTTS2.

Matcha-TTS (Official), https://github.com/shivammehta25/Matcha-TTS.
