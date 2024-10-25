# Literature review!

## Selection criteria
- Must translate from audio
- Must generate a symbolic transcription (music notation)



## Existing music transcription software

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
- Was unable to transcribe fast passages (semiquavers at 120bpm)
- 
#### [AnthemScore](https://www.lunaverus.com/)
### Research papers 


### Tools
#### [Basic Pitch](https://huggingface.co/spotify/basic-pitch)
#### [Moseca](https://github.com/fabiogra/moseca)
- Uses (basic pitch)[#basicpitch]
- had a website but was discontinued
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
