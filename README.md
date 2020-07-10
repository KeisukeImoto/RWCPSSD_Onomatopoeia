# RWCP-SSD-Onomatopoeia
RWCP-SSD-Onomatopoeia is a dataset hogehoge



## Contents


## File format

The RWCP-SSD-Onomatopoeia consists of following two types of csv files:

- XXX.ono (csv format file)  
[Worker ID who gaves onomatopoeic words, ID for onomatopoeic word, Onomatopoeia, self-reported confidence score]  

- XXX.acc (csv format file)  
[ID for onomatopoeic word, Onomatopoeia, Worker ID who gaves acceptance score, Othres-reported acceptance score]


## Directory structure


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



## Citations
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
