# How to train model

1. Install [the 🐸 Coqui-TTS](https://github.com/coqui-ai/TTS) and clone [the 🐸 Coqui-TTS](https://github.com/coqui-ai/TTS) to local computer.
2. Download ```lb-de-fr-en-pt-12800-TTS-CORPUS.zip``` file from https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS and unzip.
3. Download ```th-th.zip``` file from https://huggingface.co/datasets/wannaphong/tsync1-2-yourtts and unzip.
4. Move th-th folder to mailabs/ that unzip from ```lb-de-fr-en-pt-12800-TTS-CORPUS.zip```. (It will be mailabs/th-th)
5. Download the speaker encoder model (```config_se.json``` and ```model_se.pth.tar```) from [🐸 Coqui-TTS](https://github.com/coqui-ai/TTS/releases/tag/speaker_encoder_model) to ```recipes/multilingual/vits_tts```
6. Go to ```recipes/multilingual/vits_tts``` that cloned from the 🐸 Coqui-TTS and config path in ```train_vits_tts.py``` file and run ```python train_vits_tts.py```