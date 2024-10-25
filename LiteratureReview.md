# Literature review!





## Existing music transcription software
### Selection criteria
- Must translate from audio
- Must generate a symbolic transcription (music notation)
### Open source solutions
#### [Omnizart](https://github.com/Music-and-Culture-Technology-Lab/omnizart)
- Python library
- "transcribes musical notes of instruments [WCS20](#WCS20), chord progression [CS19](#CS19), drum events [WWS20](#WWS20), frame-level vocal melody [LS18](#LS18), note-level vocal melody [HS20](#HS20), and beat [CS20](#CS20)."
#### [Magenta Transformers](https://magenta.tensorflow.org/transcription-with-transformers)
- Started with [piano transcription](https://magenta.tensorflow.org/onsets-frames).
- Expanded in 2020 to [drum transcription](https://magenta.tensorflow.org/oaf-drums).
- Main discoveries:
  - For piano transcription, off-the-shelft Transformers work at least as well as custome neural network architectures, just needs model training to take the spectrogram as input and output MIDI-like note events
  - For multi-instrument transcription, training a single model on basically all existing datasets is very helpful. 
### Paid solutions
#### [klangio/melody scanner](https://allthingsai.com/tool/klangio)
My experience: 
- Tried transcribing played saxophone
- Transcribed slow passages ok
- Didn't provide many tools to transcribe individual passages/retry transcriptions
- Was unable to transcribe fast passages (semiquavers at 100bpm)

#### [AnthemScore](https://www.lunaverus.com/)
My experience:
- Tried transcribing C major scale up and down on the recorder in crotchets, quavers, and semiquavers (4ths, 8ths, 16ths)
- Worked reasonably well, seems like it's using a spectrograph AI method, a one-shot method essentially
- only does up to 30 seconds for the free version


## Existing jazz analysis AI
### [Jazz Harmony Helper](https://www.yeschat.ai/gpts-9t557DU9q4u-Jazz-Harmony-Helper)
- GPT powered garbage
- 

## Tools
### [Basic Pitch](https://huggingface.co/spotify/basic-pitch)
### [Demucs](https://github.com/facebookresearch/demucs)
- "state0of-the-art" music source separation model by facebook research
- Capable of separating drums, bass, and vocals from the rest of the accompaniment
- based on U-net convolutional architecture insired by [Wave-U-Net](https://github.com/f90/Wave-U-Net)
### [Moseca](https://github.com/fabiogra/moseca)
- Discussed on [reddit by the author](https://old.reddit.com/r/opensource/comments/15x3e52/from_frustration_to_creation_how_i_built_my_own/)
- Uses [basic pitch](#basicpitch)
- had a website but was discontinued

### [MidiTok](https://github.com/Natooz/MidiTok)
- Symbolic music representation
- Multiple methods
-   REMI
-   MIDI-Like
-   TSD
- [Documentation](https://miditok.readthedocs.io/en/v3.0.1/tokenizations.html#tsd)



## Datasets
### [Jazznet](https://paperswithcode.com/dataset/jazznet#:~:text=jazznet%20is%20a%20dataset%20of,than%2026k%20hours%20of%20audio.)
- Dataset of chord progressions for jazz music generation
### [symbolic-jazz-standards](https://huggingface.co/datasets/jspr/symbolic-jazz-standards)
- 10,000 minutes of audio from ~200 public-domain well-known songs
- Separated into component stems using Demucs in 4-stem mode to vocals, bass, drums, and other
- Fed through "a proprietary polyphonic music transcription model" to obtain the stems' corresponding symbolic domain representations

### [JazzSet](https://old.reddit.com/r/datasets/comments/1b73vz3/jazzset_large_audio_dataset_with_instrumentation/)
- "A remarkably large dataset of digitized high quality full length jazz session recordings from 1905 to 1966 with instrumentation and performer details annotated."
- Files available on [google drive](https://drive.google.com/drive/folders/1MkAiT8Zgm2bF-BWKYOdhVOJS-eduIofb?usp=sharing)
## References

#### CS19
T.-P. Chen and L. Su. Harmony transformer: incorporating chord segmentation into harmony recognition. In ISMIR. 2019.

#### CS20
Y.-C. Chuang and L. Su. Beat and downbeat tracking of symbolic music data using deep recurrent neural networks. In APSIPA ASC. 2020.

#### HS20
J.-Y. Hsu and L. Su. Vocano: transcribing singing vocal notes in polyphonic music using source separation and semi-supervised learning. In (Under Review). 2020.

#### LS18
W.-T. Lu and L. Su. Vocal melody extraction with semantic segmentation and audio-symbolic domain transfer learning. In ISMIR. 2018.

#### WWS20
I.-C. Wei, C.-W. Wu, and L. Su. Improving automatic drum transcription using large-scale audio-to-midi aligned data. In ICASSP (Under Review). 2020.

#### WCS20
Y.-T Wu, B. Chen, and L. Su. Multi-instrument automatic music transcription with self-attention-based instance segmentation. In TASLP. 2020.
