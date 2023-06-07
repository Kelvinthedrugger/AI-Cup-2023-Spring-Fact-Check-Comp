
## brief on the codes

Cross_plus_baseline_64_0316_0522_with_private.ipynb: produce files to train our Cross-Encoder, which will produce our final prediction.

Truth_Detection_For_Report.ipynb: Cross-Encoder implementation.

others in TWCC: our attempt to produce better data to train the Cross-Encoder. they're attempts and not our final submission.

### google colab

- [x] basically, just the train_doc64_sent64 one: it's [Cross_plus_baseline_64_0316_0522_with_private.ipynb](https://raw.githubusercontent.com/Kelvinthedrugger/AI-Cup-2023-Spring-Fact-Check-Comp/master/notebooks/google_colab/Cross_plus_baseline_64_0316_0522_with_private.ipynb)

the resulting files of the above notebook:
* model weight: with_0522__model.248.pt (which is in [cross_plus_baseline_stuff/checkpoints/sent_retrieval/](https://drive.google.com/drive/folders/1-CcS70WlE96ArDEHCxrqNHXiNEXG7TT7?usp=sharing) )
* .jsonls files to train the Cross-Encoder ( you can find these in [cross_plus_baseline_stuff/prediction_results/](https://drive.google.com/drive/u/1/folders/1-HQC9UzEYcyM5VbSxBJqONawmVW6D20l) )
    * train_doc64sent64_with_0522.jsonl

    * dev_doc64sent64_with_0522.jsonl

    * test_doc64sent64_with_private.jsonl


### TWCC

#### Cross Encoder

- [x] [Truth_Detection_For_Report.ipynb](https://raw.githubusercontent.com/Kelvinthedrugger/AI-Cup-2023-Spring-Fact-Check-Comp/master/notebooks/TWCC/Truth_Detection_For_Report.ipynb)

#### Other attempts to do the clustering instead of classification

- [ ] Bi_encoder_train_with_train_test_split.ipynb

- [ ] Bi_encoder_try_multilingual_cased.ipynb

- [ ] Cross_plus_baseline_64_0316_0522_with_private.ipynb 

- [ ] bi_encoder_with_test_embed_not_train_test_split.ipynb

- [ ] do_the_embedding.ipynb

