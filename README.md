# Japanese BERT trained on Aozora Bunko and Wikipedia

This is a repository of Japanese BERT trained on [Aozora Bunko](https://www.aozora.gr.jp/) and [Wikipedia](https://ja.wikipedia.org/).

# Features

* We provide models trained on Aozora Bunko. We used works written both in contemporary Japanese and in classical Japanese.
* Models trained on Aozora Bunko and Wikipedia are also available.
* We trained models with different pre-tokenization methods.
* All models are trained with the same configuration as the [bert-japanese](https://github.com/yoheikikuta/bert-japanese). We also provide models with 2M training steps.

# Pretrained models

After pre-tokenization, texts are tokenized with [subword-nmt](https://github.com/rsennrich/subword-nmt). Final vocab size is 32k.

## BERT-base
### Trained on Aozora Bunko (6M sentences)

#### Pre-tokenized by [MeCab](https://taku910.github.io/mecab/) with [unidic-cwj-2.3.0](https://unidic.ninjal.ac.jp/download#unidic_bccwj) and [UniDic-qkana_1603](https://unidic.ninjal.ac.jp/download_all#unidic_qkana)
* BERT-base_aozora_unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora_unidic_bpe-32k_2m.tar.xz

### Pre-tokenized by [SudachiPy](https://github.com/WorksApplications/SudachiPy) with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* BERT-base_aozora_sudachipy-unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora_sudachipy-unidic_bpe-32k_2m.tar.xz

### Trained on Aozora Bunko (6M) and Japanese Wikipedia (1.5M)

#### Pre-tokenized by MeCab with unidic-cwj-2.3.0 and UniDic-qkana_1603

* BERT-base_aozora-jawiki1.5m_unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora-jawiki1.5m_unidic_bpe-32k_2m.tar.xz

#### Pre-tokenized by SudachiPy with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* BERT-base_aozora-jawiki1.5m_sudachipy-unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora-jawiki1.5m_sudachipy-unidic_bpe-32k_2m.tar.xz

### Trained on Aozora Bunko (6M) and Japanese Wikipedia (3M)

#### Pre-tokenized by MeCab with unidic-cwj-2.3.0 and UniDic-qkana_1603

* BERT-base_aozora-jawiki3m_unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora-jawiki3m_unidic_bpe-32k_2m.tar.xz

#### Pre-tokenized by SudachiPy with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* BERT-base_aozora-jawiki3m_sudachipy-unidic_bpe-32k_1.4m.tar.xz
* BERT-base_aozora-jawiki3m_sudachipy-unidic_bpe-32k_2m.tar.xz

# Details of corpora

* Aozora Bunko: Git repository as of 2019-04-21
    * `git clone https://github.com/aozorabunko/aozorabunko` and `git checkout 1e3295f447ff9b82f60f4133636a73cf8998aeee`.
    * We removed text files with a copyright flag. You can identify them with `index_pages/list_person_all_extended_utf8.zip`.
* Wikipedia (Japanese): XML dump as of 2018-12-20
    * You can get the archive from the [download page of bert-japanese](https://drive.google.com/drive/folders/1Zsm9DD40lrUVu6iAnIuTH2ODIkh-WM-O?usp=sharing).

# Details of pretraining

coming soon
