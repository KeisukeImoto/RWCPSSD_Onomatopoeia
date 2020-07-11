# RWCP-SSD-Onomatopoeia

RWCP-SSD-Onomatopoeia is the onomatopoeic word dataset including 155,568 onomatopoeic words for 105 kinds of environmental sounds (e.g., shaver sound, whistle sound) included in RWCP-SSD (Real World Computing Partnership-Sound Scene Database) [1].
The RWCP-SSD-Onomatopoeia also contains self-reported confidence scores and others-reported acceptance scores to the onomatopoeic word, which can be used to evaluate the appropriateness of onomatopoeic words.
This dataset is designed and collected for researches on environmental sound synthesis using onomatopoetic words and environmental sound conversion into onomatopoeic words. For more information, refer to the paper [2]. If you use the RWCP-SSD-Onomatopoeia, please cite the paper [2]:  


## Contents

The RWCP-SSD-Onomatopoeia dataset consists of the following contents:

- Onomatopoeic words for environmental sounds

	We collected a total of 155,568 onomatopoeic words for for 105 kinds of environmental sounds (e.g., shaver sound, whistle sound). Each onomatopoeic word was collected from Japanese speakers in katakana, which is a Japanese syllabary, and was converted to the English phoneme representation.

- Self-reported confidence scores

	We collected confidence levels for onomatopoeic words workers themselves transcribed. The self-reported confidence score enables us to evaluate the appropriateness of onomatopoeic words on the basis of the judgement of the person giving the onomatopoeic words.

- Others-reported acceptance scores

	We collected acceptance levels for onomatopoeic words transcribed by others. The others-reported acceptance score enables us to evaluate the appropriateness of onomatopoeic words on the judgement of others. 

- WorkerID

	The dataset includes anonymized IDs of workers who gave onomatopoeic words, confidence scores, and acceptance scores.

Onomatopoeic words of Japanese syllabary and English phoneme representation are included in RWCP_SSD_Ononatopoeia_en and RWCP_SSD_Ononatopoeia_jp, respectively.

**Note that RWCP-SSD-Onomatopoeia does not contain sound files, which can be obtained from [NII Speech Resources Consortium (NII-SRC)](http://research.nii.ac.jp/src/en/index.html).** If you need any assistance, please do not hesitate to contact us.


## File format

The RWCP-SSD-Onomatopoeia consists of following two types of csv files:

- XXX.ono (csv format file)  
	``[Worker ID who gaves onomatopoeic words, ID for onomatopoeic word, Onomatopoeia, self-reported confidence score]``

- XXX.acc (csv format file)  
	``[ID for onomatopoeic word, Onomatopoeia, Worker ID who gaves acceptance score, Othres-reported acceptance score]``


## Directory structure

The RWCP-SSD-Onomatopoeia and RWCP-SSD have the same directory structure, and we can easily merge these resources.
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



## Citation
```
@article{Okamoto_arXiv2000_01,
  author={Yuki Okamoto and Keisuke Imoto and Shinnosuke Takamichi and Ryosuke Yamanishi and Takahiro Fukumori and Yoichi Yamashita},
  title={RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis},
  journal={arXiv preprint}
  year=2020,
  pages={1--5},
  url={https://arxiv.org/abs/2007.04719}
}
```


## References
[1] S. Nakamura, K. Hiyane, F. Asano, and T. Endo, "Acousticalsound database in real environments for sound scene under-standing and hands-free speech recognition," Proc. LanguageResources and Evaluation Conference (LREC), pp. 965–968,2000.  
[2] Y. Okamoto, K. Imoto, S. Takamichi, R. Yamanishi, T. Fukumori, and Y. Yamashita, "RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis," arXiv preprint, arXiv:2007.04719, 2020.  
[3] "Speech Segmentation Toolkit Using Julius," https://github.com/julius-speech/segmentation-kit.
