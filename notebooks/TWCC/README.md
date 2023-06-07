## Setup

It is recommend to 'pip install gdown' for fetching the processed data

from google drive first.

download the files, then you don't have to worry about it anymore.

**note**: it's recommended to download manually since sometimes gdown fails due to frequently access to the file

#### the folders / files to download

[official baseline folder](https://drive.google.com/drive/folders/1T6jpOtdf_i6XNYA6F_lqU4mRRh1xYPcl)

[cross_plus_baseline_stuff](https://drive.google.com/drive/u/1/folders/1dvWs4TrBKsYmRca94fHYV9c-cF6uVEf9)

* [prediction_results](https://drive.google.com/drive/u/1/folders/1-HQC9UzEYcyM5VbSxBJqONawmVW6D20l?fbclid=IwAR38oIhEC5UzFet_d02YNYCHGdd26Ixl4yNDFV1vnymae1og7IppLBN_GA8)

[FACT_CHECK_COMP_DATA](https://drive.google.com/drive/u/1/folders/15ebq-z8vvtM9Rl9t0OXqPkewSv9UM7oj)

[our trained weight for Cross Encoder](https://drive.google.com/uc?id=1tx7UrNJn9G0eIGTX6BL6HUrIFO1LXt5i&export=download)

tips: 

0. after download, you don't really have to run the **!gdown** lines in the notebooks, unless you found the files not in the folders above. Even though sometimes **gdown** don't work, the output of the command shows where to download the files.

1. you can always use https://drive.google.com/drive/folders/ + file_id (the weird looking series of alpha-numeric symbols that appears in 'gdown' command) to browse the file on google drive

2. how do you know if the url is for folders or for files? easy, just look at the gdown command, if '--folder' is added, then it's a folder, otherwise, the ones, often with '--fuzzy', is a file.

3. for files, add https://drive.google.com/uc?id= upfront to view the file on google drive

#### scripts to download files using gdown

```python
# paste the whole thing in the jupyter notebook to run it
# , instead of directly running it in a .py file

# '!' at the begining of each command means running shell command inside jupyter notebook,
# remove it if you wanted to run the whole thing in a shell directly

# this one is the official provided baseline folder, in the last 5 days of the competition
# , this fails sometimes due to too much request to access it
# mount it to your google colab notebook
# or just directly download to your local machine is recommended

# baseline code from official repository
!gdown --folder 1T6jpOtdf_i6XNYA6F_lqU4mRRh1xYPcl

# FACT_CHECK_COMP_DATA, our processed data, recommended to download manually
!gdown --folder 15ebq-z8vvtM9Rl9t0OXqPkewSv9UM7oj

# prediction results, like train_doc64sent64.jsonl, included in our 'cross_plus_baseline_stuff' recommend to download manually
!gdown --folder 1-HQC9UzEYcyM5VbSxBJqONawmVW6D20l?fbclid=IwAR38oIhEC5UzFet_d02YNYCHGdd26Ixl4yNDFV1vnymae1og7IppLBN_GA8

# cross_plus_baseline_stuff, recommend to download manually
!gdown --folder https://drive.google.com/drive/u/1/folders/1dvWs4TrBKsYmRca94fHYV9c-cF6uVEf9

```

## note

#### if load pre-trained model in Sentence-Transformer failed: use the following script

```python
# if load bi_encoder not succeessful, use below code

# load some pretrained model with the same architecture
# , which is the original model that you fine-tuned on 

model = SentenceTransformer('sentence-transformers/all-mpnet-base-v2')

# then, use ._load_sbert_model(model_path)
# model_path: path to your fine-tuned model

if os.path.exists(os.path.join(model_path, 'modules.json')):   #Load as SentenceTransformer model
    model._load_sbert_model(model_path)

```


## Flow when checking the file

0. copy the file to edit

1. edit the copied file

2. once the file is editted, change its name to a more readable one

3. run on colab to see how it works? 
	(tho this will clear the previous output, 
	 , which is prevented from copying the file)

