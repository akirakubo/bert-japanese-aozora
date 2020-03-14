# Japanese BERT trained on Aozora Bunko and Wikipedia

This is a repository of Japanese BERT trained on [Aozora Bunko](https://www.aozora.gr.jp/) and [Wikipedia](https://ja.wikipedia.org/).

# Features

* We provide models trained on Aozora Bunko. We used works written both in contemporary Japanese kana spelling and in classical Japanese kana spelling.
* Models trained on Aozora Bunko and Wikipedia are also available.
* We trained models with different pre-tokenization methods (MeCab with UniDic, SudachiPy).
* All models are trained with the same configuration as the [bert-japanese](https://github.com/yoheikikuta/bert-japanese) (except for tokenization). We also provide models with 2M training steps.

# Pretrained models

If you want to use models with [🤗 Transformers](https://github.com/huggingface/transformers), see [Converting Tensorflow Checkpoints](https://huggingface.co/transformers/converting_tensorflow_models.html).

When you use models with pre-tokenization, you will have to pre-tokenize datasets with the same morphological analyzer and the dictionary.

When you do fine-tuning tasks, you may want to modify codes. [BERT日本語Pretrainedモデル - KUROHASHI-KAWAHARA LAB](http://nlp.ist.i.kyoto-u.ac.jp/index.php?BERT%E6%97%A5%E6%9C%AC%E8%AA%9EPretrained%E3%83%A2%E3%83%87%E3%83%AB) will help you out.

## BERT-base

After pre-tokenization, texts are tokenized by [subword-nmt](https://github.com/rsennrich/subword-nmt). Final vocab size is 32k.

### Trained on Aozora Bunko (6M sentences)

#### Pre-tokenized by [MeCab](https://taku910.github.io/mecab/) with [unidic-cwj-2.3.0](https://unidic.ninjal.ac.jp/download#unidic_bccwj) and [UniDic-qkana_1603](https://unidic.ninjal.ac.jp/download_all#unidic_qkana)
* 1.4M steps: [`BERT-base_aozora_unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1Ew_2WpA60CUmLvEMaRPyTvVlss699u5c)
* 2M steps: [`BERT-base_aozora_unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=1lvE4sSu6lbm9Ih8JjT_GR1F71LqwVrwj)

#### Pre-tokenized by [SudachiPy](https://github.com/WorksApplications/SudachiPy) with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* 1.4M steps: [`BERT-base_aozora_sudachipy-unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1MHbiF6k_5arRw_Bh9fPontmno4Pt7BCE)
* 2M steps: [`BERT-base_aozora_sudachipy-unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=1WOPW4r5KpNi_EdMbO8A1Siws_5WkeyT-)

### Trained on Aozora Bunko (6M) and Japanese Wikipedia (1.5M)

#### Pre-tokenized by MeCab with unidic-cwj-2.3.0 and UniDic-qkana_1603

* 1.4M steps: [`BERT-base_aozora-jawiki1.5m_unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1feLRNIRm2R9h5rS4ibnWyTAScIDhyVhE)
* 2M steps: [`BERT-base_aozora-jawiki1.5m_unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=1F1JSNZKMi1ofnbSCYQW06qI8cTlXVW1k)

#### Pre-tokenized by SudachiPy with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* 1.4M steps: [`BERT-base_aozora-jawiki1.5m_sudachipy-unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1wC1DAEV-kpFrxBUEcQq4sLiWFDwbn0LZ)
* 2M steps: [`BERT-base_aozora-jawiki1.5m_sudachipy-unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=1UZeKEHyTXugCw2eIUZV2JX7Ax6gdfmqc)

### Trained on Aozora Bunko (6M) and Japanese Wikipedia (3M)

#### Pre-tokenized by MeCab with unidic-cwj-2.3.0 and UniDic-qkana_1603

* 1.4M steps: [`BERT-base_aozora-jawiki3m_unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1P3wJ48SYfXK6JnXlxz3BOk-kEHXPQqj1)
* 2M steps: [`BERT-base_aozora-jawiki3m_unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=15QzuCIqlxn5ijNQM2toBzIp4njsKqaWT)

#### Pre-tokenized by SudachiPy with SudachiDict_core-20191224 and MeCab with UniDic-qkana_1603

* 1.4M steps: [`BERT-base_aozora-jawiki3m_sudachipy-unidic_bpe-32k_1.4m.tar.xz`](https://drive.google.com/open?id=1h19-o4fLmUFFDM5V8Tel1jcxCLX8yPgy)
* 2M steps: [`BERT-base_aozora-jawiki3m_sudachipy-unidic_bpe-32k_2m.tar.xz`](https://drive.google.com/open?id=1mv3UXOGWYztGlaYnAc0bm9RAlcv6g3i1)

# Details of corpora

* Aozora Bunko: Git repository as of 2019-04-21
    * `git clone https://github.com/aozorabunko/aozorabunko` and `git checkout 1e3295f447ff9b82f60f4133636a73cf8998aeee`.
    * We removed text files with a copyright flag. You can identify them with `index_pages/list_person_all_extended_utf8.zip`.
* Wikipedia (Japanese): XML dump as of 2018-12-20
    * You can get the archive from the [download page of bert-japanese](https://drive.google.com/drive/folders/1Zsm9DD40lrUVu6iAnIuTH2ODIkh-WM-O?usp=sharing).

# Details of pretraining

coming soon
