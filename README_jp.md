# RWCP-SSD-Onomatopoeia

RWCP-SSD-OnomatopoeiaはRWCP実環境音声音響データベース (RWCP-SSD)[1]に含まれる105種類の環境音に対して，計155,568個のオノマトペを付与したデータセットです．
RWCP-SSD-Onomatopoeiaには，オノマトペに対する自信度，許容度も含まれており，オノマトペの適切性を評価するために利用できます．
本データセットは，オノマトペを用いた環境音の合成・変換に関する研究のために設計・収集されたものです．
データセットの詳しい概要は論文[2]を参照してください．
また，RWCP-SSD-Onomatopoeiaを使用する場合は論文[2]を引用してください．  

更新：論文[3]で使用されたオノマトペのアライメント結果を追加しました．


## 内容

このデータセットは以下の内容を含みます．

- 環境音に対するオノマトペ

	105種類の環境音に対し，合計155,568個のオノマトペを収集しました．
	各オノマトペは日本語話者からカタカナで収集し，英語の音素表記に変換しました．

- オノマトペに対する自信度

	オノマトペを付与した本人自身のオノマトペに対し，155,568個の自信度を収集しました．
	自信度を利用することで，擬音語を与えた人の判断に基づいて擬音語の適切性を評価することができます．

- オノマトペに対する許容度

	他者が付与したオノマトペに対し，548,367個の許容度を収集しました．
	許容度は自信度が4以上のオノマトペに対し，5人以上のワーカーから収集しました．
	許容度を利用することで，他者の判断に基づいてオノマトペの適切性を評価することができます．

- ワーカーID

	データセットにはオノマトペ，自信度を与えたワーカー，許容度を与えたワーカーの匿名化されたIDが含まれています．

- アライメント結果

	[*Hidden markov model toolkit (HTK)*](https://htk.eng.cam.ac.uk/)を用いてオノマトペと環境音のアライメント結果を取得しました．アライメントに基づく無音区間の切り出しなどを行うことができます．現状では，カタカナ表記のオノマトペに対してのみ提供されています．

RWCP-SSD-Onomatopoeia_jp, RWCP-SSD-Onomatopoeia_enのそれぞれには，カタカナ表記のオノマトペと英語の音素表記のオノマトペが含まれています．

**RWCP-SSD-Onomatopoeiaには環境音ファイルは含まれていません．環境音ファイルは [国立情報学研究所 音声資源コンソーシアム (NII-SRC)](http://research.nii.ac.jp/src/en/index.html)から入手頂きますようお願いします．**
環境音ファイルの入手についてご不明点がございましたら，お気軽にお問い合わせください．


## ファイル形式

RWCP-SSD-Onomatopoeiaは以下の２種類のcsvファイルと１種類のlabファイルで構成されています．

- XXX.ono
	``[オノマトペを付与した人のID, オノマトペの識別ID, オノマトペ, 自信度]``

- XXX.acc
	``[オノマトペの識別ID, オノマトペ, 許容度を付与した人のID, 許容度]``

- {オノマトペの識別ID}.lab

オノマトペの識別IDは各環境音のオノマトペごとに付与された固有のIDです．

## ディレクトリ構造

RWCP-SSD-OnomatopoeiaとRWCP-SSDは同じディレクトリ構造を持っており，これらのリソースは簡単に併合することができます．
本データセットのディレクトリ構造は以下の通りです．

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
	        │   │   ├── 0006_7.lab
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



## 利用規約

RWCP-SSD-Onomatopoeiaは以下の場合に限り利用可能です．
- アカデミック機関での研究
- 非商用目的の研究（営利団体での研究も含む）
- 個人での利用（ブログなどを含む）

営利目的での利用を希望される場合は，井本 桂右もしくは岡本 悠希までご連絡ください．
再配布はできませんが，本データセットの一部（例えば，10個のオノマトペ）をあなたのウェブページやブログなどで公開することは可能です．
論文やブログポスト等の成果を公開する際には，本論文を引用してください．  

### 引用
```
@article{Okamoto_DCASE2000_01,
  author={Yuki Okamoto and Keisuke Imoto and Shinnosuke Takamichi and Ryosuke Yamanishi and Takahiro Fukumori and Yoichi Yamashita},
  title={RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis},
  journal={Proc. Detection and Classification of Acoustic Scenes and Events (DCASE)}
  year=2020,
  pages={125--129},
}
```


## 作成者
岡本 悠希（立命館大学）  
井本 桂右（同志社大学）  
高道 慎之介（東京大学）  
山西 良典（関西大学）  
福森 隆寛（立命館大学）  
山下 洋一（立命館大学）  

井本 桂右 (keisuke.imoto@ieee.org)，岡本 悠希（yuki.11.research@gmail.com）が主な責任者です．


## 謝辞

この研究は２０２０年度国立情報学研究所公募型共同研究（20S0401）の助成を受けています。



## 参考文献
[1] S. Nakamura, K. Hiyane, F. Asano, and T. Endo, "Acousticalsound database in real environments for sound scene under-standing and hands-free speech recognition," Proc. Language Resources and Evaluation Conference (LREC), pp. 965–968,2000.  
[2] Y. Okamoto, K. Imoto, S. Takamichi, R. Yamanishi, T. Fukumori, and Y. Yamashita, "RWCP-SSD-Onomatopoeia: Onomatopoeic Word Dataset for Environmental Sound Synthesis," Proc. Detection and Classification of Acoustic Scenes and Events (DCASE), pp. 125-129, 2020. Paper URL: http://dcase.community/documents/workshop2020/proceedings/DCASE2020Workshop_Okamoto_21.pdf  
[3] H. Ohnaka, S. Takamichi, K. Imoto, Y. Okamoto, K. Fujii, and H. Saruwatari, "Visual Onoma-to-Wave: Environmental Sound Synthesis from Visual Onomatopoeias and Sound-Source Images," Proc. IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2023. Paper URL: https://ieeexplore.ieee.org/document/10096517