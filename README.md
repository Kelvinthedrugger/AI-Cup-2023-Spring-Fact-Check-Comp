# 競賽報告與程式碼TEAM_3176事實文字檢索與查核競賽_名次15

## File structure

<img src="https://raw.githubusercontent.com/Kelvinthedrugger/AI-Cup-2023-Spring-Fact-Check-Comp/master/assets/file_structure.png" width="560" height="370">

## On browsing the codes

see the **notebooks** folder for details.

## Install the libraries

Most of the used libraries are pre-installed in google colab and TWCC (台智雲)

, below are basically the ones you have to do manually.

Either paste this in terminal or in the jupyter notebook with **'!'** before

each line of **pip install** is fine.

e.g., 
```python
!pip install -U sentence-transformers -q
```

```bash

### sentence transformer
pip install -U sentence-transformers -q

### others
### to run 'parallel_apply()' in pandas
pip -q install pandarallel==1.6.4

### help parse the chinese text
pip -q install opencc

pip -q install hanlp

### transformers by huggingface that every one is using
pip -q install transformers==4.27.1

### search thru wikipedia
pip -q install wikipedia==1.4.0
```

## 使用簡介

任務目標：以wikipedia文件做為事實資料庫，判斷使用者輸入的Claims為真(supports)，偽(refutes)或資訊不足(Not Enough Info)

模型架構：
1. 事實提取：使用官方提供的baseline code part 2 (BERT-based model)，Top-K設為64，並取出前五高分的證據句
2. 判斷真偽：使用SBERT的Cross-Encoder (nli-deberta-base)做training
3. 重現結果流程與重要模塊輸出：詳見 **notebooks** 資料夾

## Citation

[Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084):

```bibtex 
@inproceedings{reimers-2019-sentence-bert,
    title = "Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks",
    author = "Reimers, Nils and Gurevych, Iryna",
    booktitle = "Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing",
    month = "11",
    year = "2019",
    publisher = "Association for Computational Linguistics",
    url = "https://arxiv.org/abs/1908.10084",
}
```

[Making Monolingual Sentence Embeddings Multilingual using Knowledge Distillation](https://arxiv.org/abs/2004.09813):

```bibtex
@inproceedings{reimers-2020-multilingual-sentence-bert,
    title = "Making Monolingual Sentence Embeddings Multilingual using Knowledge Distillation",
    author = "Reimers, Nils and Gurevych, Iryna",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing",
    month = "11",
    year = "2020",
    publisher = "Association for Computational Linguistics",
    url = "https://arxiv.org/abs/2004.09813",
}
```

