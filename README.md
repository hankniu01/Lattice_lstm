Chinese NER Using Lattice LSTM
====

Lattice LSTM (torch 1.12.0 version) for Chinese NER.[Chinese NER Using Lattice LSTM](https://arxiv.org/pdf/1805.02023.pdf).

Requirement:
======
	Python: 3.7   
	PyTorch: 1.12.0 

Input format:
======
CoNLL format (prefer BIOES tag scheme), with each character its label for one line. Sentences are splited with a null line.

	美	B-LOC
	国	E-LOC
	的	O
	华	B-PER
	莱	I-PER
	士	E-PER

	我	O
	跟	O
	他	O
	谈	O
	笑	O
	风	O
	生	O 

Pretrained Embeddings:
====
The pretrained character and word embeddings are the same with the embeddings in the baseline of [RichWordSegmentor](https://github.com/jiesutd/RichWordSegmentor)

Character embeddings (gigaword_chn.all.a2b.uni.ite50.vec): [Google Drive](https://drive.google.com/file/d/1_Zlf0OAZKVdydk7loUpkzD2KPEotUE8u/view?usp=sharing) or [Baidu Pan](https://pan.baidu.com/s/1pLO6T9D)

Word(Lattice) embeddings (ctb.50d.vec): [Google Drive](https://drive.google.com/file/d/1K_lG3FlXTgOOf8aQ4brR9g3R40qi1Chv/view?usp=sharing) or [Baidu Pan](https://pan.baidu.com/s/1pLO6T9D)

How to run the code?
====
1. Download the character embeddings and word embeddings and put them in the `data` folder.
2. Modify the `run_main.py` or `run_demo.py` by adding your train/dev/test file directory.
3. `sh run_main.py` or `sh run_demo.py`


Resume NER data 
====
Crawled from the Sina Finance, it includes the resumes of senior executives from listed companies in the Chinese stock market. Details can be found in our paper.


Cite: 
========
cite from https://github.com/jiesutd/LatticeLSTM 