# KhanomTan TTS v1.0
KhanomTan TTS (ขนมตาล) is an open-source Thai text-to-speech model that supports multilingual speakers such as Thai, English, and others.

KhanomTan TTS is a YourTTS model trained on multilingual languages that supports Thai. We use Thai speech corpora, TSync 1* and TSync 2* [mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS](https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS) to train the YourTTS model by using code from [the 🐸 Coqui-TTS](https://github.com/coqui-ai/TTS).

*Note: Those are not complete corpora. We can access the public corpus only which is smaller.

**Demo** [https://wannaphong.github.io/KhanomTan-TTS-v1.0/](https://wannaphong.github.io/KhanomTan-TTS-v1.0/)

**Model** [https://huggingface.co/wannaphong/khanomtan-tts-v1.0](https://huggingface.co/wannaphong/khanomtan-tts-v1.0)

### Config
We use Thai characters to the graphemes config to training the model and use the Speaker Encoder model from [🐸 Coqui-TTS](https://github.com/coqui-ai/TTS/releases/tag/speaker_encoder_model).

### Dataset
We use Tsync 1 and Tsync 2 corpora, which are not complete datasets, and then add these to [mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS](https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS) dataset.

### Trained the model
We use the 🐸 Coqui-TTS multilingual VITS-model recipe (version 0.7.1 or the commit id is d46fbc240ccf21797d42ac26cb27eb0b9f8d31c4) for training the model, and we use the speaker encoder model from [🐸 Coqui-TTS](https://github.com/coqui-ai/TTS/releases/tag/speaker_encoder_model) then we release the best model to public access.

### Language
- th-th: Thai
- en: English
- fr-fr: French language
- pt-br: Portuguese
- x-de: Danish
- x-lb: Luxembourgish

### Speaker and Language

- en
    - female
	    - Linda
    - male
	    - p259
	    - p274
	    - p286
- fr-fr
    - female
	    - Bunny
	    - Judith
    - male
	    - Bernard
- pt-br
    - male
	    - Ed
- th-th
    - female
	    - Tsyncone
	    - Tsynctwo
- x-de
    - female
	    - Judith
	    - Kerstin
    - male
	    - Thorsten
- x-lb
    - female
	    - Caroline
	    - Judith
	    - Nathalie
	    - Sara
    - male
	    - Charel
	    - Guy
	    - Jemp
	    - Luc
	    - Marco

## Model Cards
- Developer: Wannaphong Phatthiyaphaibun
- Model date: 2022-08-24
- Model version: 1.0
- Dataset: [mbarnig/lb-de-fr-en-pt-th-12200-TTS-CORPUS](https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS), [TSync 1, and TSync 2](https://huggingface.co/datasets/wannaphong/tsync1-2-yourtts).
- Code License: Apache License, Version 2
- Model License: CC-BY-NC-SA 3.0

### Intended Use
- Intended to be used for applications that need to use text-to-speech.
- Intended to be made for an open-source project, startup, independent developer, student, and other. It is the basic tool for use in applications.
- Not suitable for emotion text-to-speech, code-switch text-to-speech.


### Factors
- Based on quality audio, numbers of hours and other for text-to-speech task.
- Evaluation factors is use the testset.


### Metrics
- avg_loader_time
- avg_loss_disc
- avg_loss_0
- avg_loss_gen
- avg_loss_kl
- avg_loss_feat
- avg_loss_mel
- avg_loss_duration
- avg_loss_1

### Training Data
We use [mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS](https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS) corpus and merge with Tsync 1 corpus  and Tsync 2 corpus (Not complete data because We can use the public dataset only, and they don't release complete corpus)

### Evaluation Data
Fiew files sound from Tsync 1 and Tsync 2 corpora and [mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS](https://huggingface.co/datasets/mbarnig/lb-de-fr-en-pt-12800-TTS-CORPUS).

### Quantitative Analyses

See more at [https://huggingface.co/wannaphong/khanomtan-tts-v1.0/tensorboard](https://huggingface.co/wannaphong/khanomtan-tts-v1.0/tensorboard).

**Best Model**

```
[1m   --> STEP: 430/449 -- GLOBAL_STEP: 58800[0m
     | > loss_disc: 2.54072  (2.58441)
     | > loss_disc_real_0: 0.19995  (0.18017)
     | > loss_disc_real_1: 0.16633  (0.20526)
     | > loss_disc_real_2: 0.23312  (0.22947)
     | > loss_disc_real_3: 0.22889  (0.24121)
     | > loss_disc_real_4: 0.24266  (0.23288)
     | > loss_disc_real_5: 0.27341  (0.23818)
     | > loss_0: 2.54072  (2.58441)
     | > grad_norm_0: 104.64307  (99.20876)
     | > loss_gen: 2.15378  (2.19429)
     | > loss_kl: 2.26462  (2.09749)
     | > loss_feat: 5.16728  (5.06811)
     | > loss_mel: 20.70769  (20.19465)
     | > loss_duration: 0.30896  (0.39851)
     | > loss_1: 30.60234  (29.95306)
     | > grad_norm_1: 1141.71912  (867.80768)
     | > current_lr_0: 0.00020 
     | > current_lr_1: 0.00020 
     | > step_time: 1.42650  (1.40457)
     | > loader_time: 0.01250  (0.01142)


[1m > EVALUATION [0m


  [1m--> EVAL PERFORMANCE[0m
     | > avg_loader_time:[91m 0.00631 [0m(+0.00023)
     | > avg_loss_disc:[91m 2.58187 [0m(+0.08440)
     | > avg_loss_disc_real_0:[92m 0.07255 [0m(-0.01495)
     | > avg_loss_disc_real_1:[92m 0.17810 [0m(-0.01394)
     | > avg_loss_disc_real_2:[91m 0.21503 [0m(+0.02537)
     | > avg_loss_disc_real_3:[92m 0.21009 [0m(-0.03936)
     | > avg_loss_disc_real_4:[91m 0.21894 [0m(+0.01136)
     | > avg_loss_disc_real_5:[92m 0.21494 [0m(-0.02851)
     | > avg_loss_0:[91m 2.58187 [0m(+0.08440)
     | > avg_loss_gen:[92m 1.78352 [0m(-0.16346)
     | > avg_loss_kl:[92m 2.18065 [0m(-0.13942)
     | > avg_loss_feat:[91m 4.92250 [0m(+0.03692)
     | > avg_loss_mel:[92m 19.75920 [0m(-1.00270)
     | > avg_loss_duration:[91m 0.30307 [0m(+0.00521)
     | > avg_loss_1:[92m 28.94896 [0m(-1.26345)
```

**Last checkpoint**

```
[1m   --> STEP: 404/449 -- GLOBAL_STEP: 439975[0m
     | > loss_disc: 2.31149  (2.37792)
     | > loss_disc_real_0: 0.16091  (0.13133)
     | > loss_disc_real_1: 0.16328  (0.19283)
     | > loss_disc_real_2: 0.20310  (0.21166)
     | > loss_disc_real_3: 0.23234  (0.22953)
     | > loss_disc_real_4: 0.20503  (0.21695)
     | > loss_disc_real_5: 0.23729  (0.22788)
     | > loss_0: 2.31149  (2.37792)
     | > grad_norm_0: 32.66961  (29.36955)
     | > loss_gen: 2.38829  (2.46154)
     | > loss_kl: 2.13480  (2.14247)
     | > loss_feat: 6.61947  (7.41335)
     | > loss_mel: 18.98203  (18.62947)
     | > loss_duration: 0.26565  (0.32838)
     | > loss_1: 30.39024  (30.97523)
     | > grad_norm_1: 380.15573  (318.00244)
     | > current_lr_0: 0.00018 
     | > current_lr_1: 0.00018 
     | > step_time: 1.36950  (1.60544)
     | > loader_time: 0.01070  (0.01238)


[1m   --> STEP: 429/449 -- GLOBAL_STEP: 440000[0m
     | > loss_disc: 2.36906  (2.37788)
     | > loss_disc_real_0: 0.17430  (0.13148)
     | > loss_disc_real_1: 0.21238  (0.19297)
     | > loss_disc_real_2: 0.23353  (0.21159)
     | > loss_disc_real_3: 0.22233  (0.22948)
     | > loss_disc_real_4: 0.22807  (0.21668)
     | > loss_disc_real_5: 0.23396  (0.22782)
     | > loss_0: 2.36906  (2.37788)
     | > grad_norm_0: 17.20346  (29.36594)
     | > loss_gen: 2.48922  (2.46176)
     | > loss_kl: 1.93436  (2.14287)
     | > loss_feat: 7.27229  (7.42032)
     | > loss_mel: 17.29741  (18.62724)
     | > loss_duration: 0.25341  (0.32484)
     | > loss_1: 29.24669  (30.97705)
     | > grad_norm_1: 148.36732  (319.84647)
     | > current_lr_0: 0.00018 
     | > current_lr_1: 0.00018 
     | > step_time: 1.36860  (1.59275)
     | > loader_time: 0.01080  (0.01229)
```

### Ethical Considerations
This model can be used in multilingual language to speak with another language speaker or use voice clones, but the YourTTS model cannot synthesize voice like natural speakers. It can't synthesize voice at 44100 Hz. It depends on your ethics, so we don't recommend using this model in the wrong way. The lousy synthesis may be from the corpus or others because we can use the public dataset and graphemes for training the model. If you need the best synthesis, we suggest you collect your dataset with a large dataset (very much and very high quality) and train a new model with text-to-speech models, i.e., Tacotron or VITS.

Read about YourTTS:
[https://github.com/coqui-ai/TTS/discussions/1759](https://github.com/coqui-ai/TTS/discussions/1759).

### Caveats and Recommendations
- Text without special characters, code-switching, digital numbers, and more. (monolingual text only)
- You need to choose language when you use this model.
- YourTTS: Towards Zero-Shot Multi-Speaker TTS and Zero-Shot Voice Conversion for everyone https://github.com/Edresson/YourTTS
- Try to use phonemes instead of using graphemes.
Read more about 🐸TTS at https://github.com/coqui-ai/TTS
- How to collect your dataset for text-to-speech: https://tts.readthedocs.io/en/latest/what_makes_a_good_dataset.html
- How to create a speech dataset for ASR, TTS, and other speech tasks https://ogunlao.github.io/blog/2021/01/26/how-to-create-speech-dataset.html
- New to the TTS field, and I have some questions (about the necessary data) https://discourse.mozilla.org/t/new-to-the-tts-field-and-i-have-some-questions-about-the-necessary-data/75198.

