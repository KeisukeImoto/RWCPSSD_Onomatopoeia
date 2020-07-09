# RWCP-SSD-Onomatopoeia

## 内容
このデータセットはRWCP 実環境音声音響データベース[1]に含まれる105種類の環境音に対するテキストで書かれたオノマトペからなります．環境音に対するオノマトペはクラウドソーシングサービスを用いて収集しました． 
このデータセットは以下の２種類のデータからなります．


- ***RWCP-SSD-Onomatopoeia_jp***
	- 環境音に対するカタカナ表記のオノマトペ（合計155,568個）
	- オノマトペに対する自信度
		- 付与したオノマトペに対する５段階での自信度合い  
	- オノマトペに対する許容度
		- 他者が付与したオノマトペに対する５段階での許容度合い  
	- オノマトペ，自信度，許容度を付与した人のID
		- ４桁の算用数字による匿名化されたID  


- ***RWCP-SSD-Onomatopoeia_en*** 
	- 環境音に対する音素表記のオノマトペ（合計155,568個）
		- Julius 音素セグメンテーションキット[2]によりカタカナで書かれたオノマトペを音素表記に変換したデータ  
	- オノマトペに対する自信度
		- 付与したオノマトペに対する５段階での自信度合い  
	- オノマトペに対する許容度
		- 他者が付与したオノマトペに対する５段階での許容度合い  
	- オノマトペ，自信度，許容度を付与した人のID
		- ４桁の算用数字による匿名化されたID  


このデータセットはRWCP 実環境音声音響データベースと同じディレクトリ構造をしています．
このデータセットのディレクトリ構造は以下の通りです．  


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

各ディレクトリには以下の２種類のファイルを含みます．
- XXX.ono：[オノマトペを付与した人のID, オノマトペの識別ID, オノマトペ, 自信度]の順に記載されたcsvファイル
- XXX.acc：[オノマトペの識別ID, オノマトペ, 許容度を付与した人のID, 許容度]の順に記載されたcsvファイル  


オノマトペの識別IDはオノマトペごとに付与された固有のIDです．

## 使い方
このデータセットは以下の場合に限り使用可能です．
- アカデミック機関での研究
- 非商用目的の研究（営利団体での研究も含む）
- 個人での利用（ブログなどを含む）

営利目的の利用を希望される場合，keisuke.imoto@ieee.org までご連絡ください．また，論文やブログポスト等の成果を公開する際には，下記論文を引用してください．  

Yuki Okamoto, Keisuke Imoto, Shinnosuke Takamichi, Ryosuke Yamanishi and Yoichi Yamashita,   
"RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis,"  
arXiv preprint, XXXX.XXXXX, 2020


## 作成者
岡本 悠希（立命館大学）  
井本 桂右（同志社大学）  
高道 慎之介（東京大学）  
山西 良典（関西大学）  
福森 隆寛（立命館大学）  
山下 洋一（立命館大学）  

井本 桂右 (keisuke.imoto@ieee.org)，岡本 悠希（yuki.11.research@gmail.com）が主な責任者です．


## 商用利用
我々は，皆様の商用利用を歓迎します．下記メールアドレスにご連絡ください．  
井本 桂右：keisuke.imoto@ieee.org


## 参考文献
[1] S. Nakamura, K. Hiyane, F. Asano, and T. Endo,   
	“Acousticalsound database in real environments for sound scene under-standing and hands-free speech recognition,”      
	Proc. LanguageResources and Evaluation Conference (LREC), pp. 965–968,2000.  
[2] “Speech Segmentation Toolkit using Julius,” https://github.com/julius-speech/segmentation-kit.
