# PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice 

## Notes
This repository is developed entirely on top of the original [Serenade](https://github.com/lesterphillip/) repository, developed by Lester Philip Violeta @Nagoya University. The following changes were made to it:
- Pitch curves are extracted with RMPVE instead of the Harvest algorithm.
- The transcription model operates directly on the pitch curves extracted with RMPVE, instead of on audio.
- Serenade is trained on LogF0 instead of notes, so that on inference it can be conditioned on the stylized pitch curve.
- Neither cyclic training nor SiFi-GAN post-processing is performed.

## Before you use this repo and pretrained models

### License
Commercial use is NOT allowed. Please read the [LICENSE](LICENSE) file. This repo and the models are licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

### Conditions
Using this repository and the models to impersonate any singer without their consent is strictly PROHIBITED. Please use this repo and the pretrained models responsibly.


## Usage

### Installation
```bash
conda create -n _pitchstar_ python=3.10
conda activate _pitchstar
pip install -e .
```

### Recipes
A recipe for training a model (with pretrained models) is provided. Please refer to the README file in the recipe directory for more details.
```
cd egs/gtsinger/pst1
./run.sh
```

## Acknowledgements
- [ParallelWaveGAN](https://github.com/kan-bayashi/ParallelWaveGAN/) (Repository skeleton)
- [seq2seq-vc](https://github.com/unilight/seq2seq-vc) (Repository skeleton and utils)
- [ESPNet](https://github.com/espnet/espnet) (GST encoder)
- [NNSVS](https://github.com/nnsvs/nnsvs) (Preprocessing, Linear MIDI shift)
- [Matcha-TTS](https://github.com/shivammehta25/Matcha-TTS) (1D UNet architecture)
- [Sprocket](https://github.com/k2kobayashi/sprocket) (F0 analysis)
- [Phoneme-MIDI](https://github.com/seyong92/phoneme-informed-note-level-singing-transcription) (Audio MIDI extraction, pretrained models)
- [SiFiGAN](https://github.com/chomeyama/SiFiGAN) (Analysis and synthesis code, pretrained models)

## Questions?
Please use the issues section to ask questions about the repo so that others can benefit from the answers.

## Citation
Currently under review.

## Author and Developer
Anonymous

## Advisers
Anonymous
