# RWCP-SSD-Onomatopoeia

RWCP-SSD-Onomatopoeia is the onomatopoeic word dataset including 155,568 onomatopoeic words for 105 kinds of environmental sounds (e.g., shaver sound, whistle sound) included in RWCP-SSD (Real World Computing Partnership-Sound Scene Database) [1].
The RWCP-SSD-Onomatopoeia also contains self-reported confidence scores and others-reported acceptance scores to the onomatopoeic words, which can be used to evaluate the appropriateness of onomatopoeic words.
This dataset is designed and collected for researches on environmental sound synthesis using onomatopoetic words and environmental sound conversion into onomatopoeic words. For more information, refer to the paper [2]. If you use the RWCP-SSD-Onomatopoeia, please cite the paper [2].  

update: Alignment results of onomatopoeia used in the paper[4] are added (Japanese only).


## Contents

The RWCP-SSD-Onomatopoeia dataset consists of the following contents:

- Onomatopoeic words for environmental sounds

	We collected a total of 155,568 onomatopoeic words for for 105 kinds of environmental sounds (e.g., shaver sound, whistle sound). Each onomatopoeic word was collected from Japanese speakers in katakana, which is a Japanese syllabary. We converted each onomatopoeic word written by katakana into the English phoneme representation, which follows the conversion rule of [katakana2accphrase.csv](https://github.com/KeisukeImoto/RWCPSSD_Onomatopoeia/blob/master/katakana2accphrase.csv).

- Self-reported confidence scores

	We collected 155,568 confidence scores for onomatopoeic words workers themselves transcribed. The self-reported confidence score enables us to evaluate the appropriateness of onomatopoeic words on the basis of the judgement of the person giving the onomatopoeic words.

- Others-reported acceptance scores

	We collected 548,367 acceptance scores for onomatopoeic words transcribed by other workers. The others-reported acceptance score was collected from more than five workers for onomatopoeic words with 4 or high confidence scores. The others-reported acceptance score enables us to evaluate the appropriateness of onomatopoeic words on the judgement of others.

- WorkerID

	The dataset includes anonymized IDs of workers who gave onomatopoeic words, confidence scores, and acceptance scores.

- Alignment results

	Alignment results of onomatopoeia and environmental sounds were obtained using [*Hidden markov model toolkit (HTK)*](https://htk.eng.cam.ac.uk/). It is possible to cut out silent intervals based on the alignment, etc. Currently, this service is only available for onomatopoeia written in katakana (japanese).

Onomatopoeic words of English phoneme representation and Japanese syllabary are included in RWCP_SSD_Ononatopoeia_en and RWCP_SSD_Ononatopoeia_jp, respectively.

**Note that RWCP-SSD-Onomatopoeia does not contain sound files, which can be obtained from [NII Speech Resources Consortium (NII-SRC)](http://research.nii.ac.jp/src/en/index.html).** If you need any assistance, please do not hesitate to contact us.


## File format

The RWCP-SSD-Onomatopoeia consists of following two types of csv files:

- XXX.ono  
	``[Worker ID who gaves onomatopoeic word, ID for onomatopoeic word, Onomatopoeia, Self-reported confidence score]``

- XXX.acc  
	``[ID for onomatopoeic word, Onomatopoeia, Worker ID who gaves acceptance score, Othres-reported acceptance score]``

- {ID for onomatopic word}.lab

The ID for onomatopoeic word is unique for each environmental sound and worker gaves the onomatopoeic word.

## Directory structure

The RWCP-SSD-Onomatopoeia and RWCP-SSD have the same directory structure, and you can easily merge these resources.
The directory structure of this dataset is as follows:

	RWCP_SSD_Onomatopoeia
	└── nospeech
	    └── drysrc
	        ├── a1
	        │   ├── cherry1
	        │   │   ├── 000.acc
	        │   │   ├── 000.ono
	        │   │   ├── 001.acc
	        │   │   ├── 001.ono
	        │   │   ├── 002.acc
	        │   │   ├── 002.ono
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   ├── 099.acc
	        │   │   └── 099.ono
	        │   ├── cherry2
	        │   ├── cherry3
	        │   ├     ・
	        │   ├     ・
	        │   ├     ・
	        │   └── wood3
	        ├── a2
	        ├── a3
	        ├── a4
	        ├   ・
	        ├   ・
	        ├   ・
	        └── c5

	RWCP_SSD_Onomatopoeia_lab
	└── nospeech
	    └── drysrc
	        ├── a1
	        │   ├── cherry1
	        │   │   ├── 0006_7.lab # correspond to [ID for onomatopoeic word]
	        │   │   ├── 0006_8.lab
	        │   │   ├── 0006_9.lab
	        │   │   ├── 0007_10.lab
	        │   │   ├── 0007_11.lab
	        │   │   ├── 0007_12.lab
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   ├── 1099_95.lab
	        │   │   └── 1099_96.lab
	        │   ├── cherry2
	        │   │   ├── 0001_52.lab
	        │   │   ├── 0001_53.lab
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   ├     ・
	        │   │   └── 1108_45.lab
	        │   ├── cherry3
	        │   ├     ・
	        │   ├     ・
	        │   ├     ・
	        │   └── wood3
	        ├── a2
	        ├── a3
	        ├── a4
	        ├   ・
	        ├   ・
	        ├   ・
	        └── c5

## Terms of use

The RWCP-SSD-Onomatopoeia may be used for 
- Research by academic institutions
- Non-commercial research, including research conducted within commercial organisations
- Personal use.

If you want to use for commercial purposes, please contact us (Keisuke Imoto or Yuki Okamoto).
Re-distribution is not permitted, but you can use a part of this dataset (e.g., 〜10 onomatopoeic words) in your website or blog post.
Please cite this paper when you use this dataset in your research paper, blog post, and preprint.

### Citation
```
@article{Okamoto_DCASE2000_01,
  author={Yuki Okamoto and Keisuke Imoto and Shinnosuke Takamichi and Ryosuke Yamanishi and Takahiro Fukumori and Yoichi Yamashita},
  title={RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis},
  journal={Proc. Detection and Classification of Acoustic Scenes and Events (DCASE)}
  year=2020,
  pages={125--129},
}
```

## Acknowledgment

The research was supported by ROIS NII Open Collaborative Research 2020 Grant Number 20S0401. 


## References
[1] S. Nakamura, K. Hiyane, F. Asano, and T. Endo, "Acoustical Sound Database in Real Environments for Sound Scene Understanding and Hands-free Speech Recognition," Proc. LanguageResources and Evaluation Conference (LREC), pp. 965–968,2000.  
[2] Y. Okamoto, K. Imoto, S. Takamichi, R. Yamanishi, T. Fukumori, and Y. Yamashita, "RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis," Proc. Detection and Classification of Acoustic Scenes and Events (DCASE), pp. 125-129, 2020. Paper URL: http://dcase.community/documents/workshop2020/proceedings/DCASE2020Workshop_Okamoto_21.pdf  
[3] "Speech Segmentation Toolkit Using Julius," https://github.com/julius-speech/segmentation-kit.  
[4] H. Ohnaka, S. Takamichi, K. Imoto, Y. Okamoto, K. Fujii, and H. Saruwatari, "Visual Onoma-to-Wave: Environmental Sound Synthesis from Visual Onomatopoeias and Sound-Source Images," Proc. IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2023. Paper URL: https://ieeexplore.ieee.org/document/10096517