# 競賽報告與程式碼TEAM_3176事實文字檢索與查核競賽_名次15

## File structure

// TODO: put file tree here using commands like 'tree'

// 粗體的是folder

**excalidraw_pics**

    if one uses pics drawn with excalidraw, put the pics there

    to make sure that .md files can render normally


**notebooks**

|---**google colab**
        ...
        will just be a README.md with link to files in it?

|---**TWCC**
        ...

<img src="https://raw.githubusercontent.com/Kelvinthedrugger/AI-Cup-2023-Spring-Fact-Check-Comp/master/assets/file_structure.png" width="560" height="256">

## Installation

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
