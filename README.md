### PVGRU

The repository contains the code for PVHD，the baseline for comparison, and SepaCVAE, where the code for SepaCVAE is provided by the original author of the paper [1].

### PLATO

We employ PLATO (uncased model: 12-layers, 768-hidden, 12-heads, 132M parameters) fine-tuning on two datasets.



### Attention

We employ an improved version of BLEU and ROUGE  in paper [2]. When using the BLEU function provided by NLTK with SmoothingFunction().method7, the results are improved by about 20 points. We provide a set of comparative results for reference.

Results of HRED

BLEU in paper: bleu-1: 0.2890 bleu-2: 0.2352 bleu-3:0.2103 bleu-4: 0.2019

NLTK BLEU: bleu-1: 0.4865 bleu-2: 0.3789 bleu-3: 0.3101 bleu-4: 0.2619

### DailyDialog

#### NLTK-BLEU  

| Model      | BLEU-1 |BLEU-2 |
| ----------- | ----------- |----------- |
| PLATO      | 42.00       |32.90       |
| SepaCVAE   | 45.37       |34.38      |
|PVHD       | 49.54       |37.35       |


#### BLEU In Paper [2]  

| Model      | BLEU-1 |BLEU-2 |dist-1 | dist-2|
| ----------- | ----------- |----------- |----------- |----------- |
| PLATO      | 24.77       |13.22       |14.75 |47.16 |
| SepaCVAE   | 25.31       |22.41       |12.08 |36.56 |
|PVHD       | 32.19       |25.42       |15.33 |49.93 |


### DSTC7-AVSD (without knowledge)

#### NLTK-BLEU  

| Model      | BLEU-1 |BLEU-2 |
| ----------- | ----------- |----------- |
| PLATO      | 52.44       |40.02       |
| SepaCVAE   | 44.85       |30.08       |
|PVHD       | 49.60       |39.78       |

#### BLEU In Paper [2]  

| Model      | BLEU-1 |BLEU-2 |dist-1 | dist-2|
| ----------- | ----------- |----------- |----------- |----------- |
| PLATO      | 30.16       |18.61       |6.37 |29.74 |
| SepaCVAE   | 26.59       |18.94       |5.53 |28.50 |
|PVHD       | 29.87       |20.03       |6.54 |31.77 |


### T-Test

#### DailyDialog  

| Model | p-value |
| ----------- | ----------- |
| PVHD-PLATO|0.11|
|PVHD-SepaCVAE|0.05|

#### DSTC7-AVSD  

| Model | p-value |
| ----------- | ----------- |
| PVHD-PLATO|0.22|
|PVHD-SepaCVAE|0.04|

[1] Bin Sun, Shaoxiong Feng, Yiwei Li, Jiamou Liu, and Kan Li. 2021. Generating relevant and coherent dialogue responses using self-separated conditional variational autoencoders. In ACL.

[2] Yang A, Liu K, Liu J, et al. Adaptations of ROUGE and BLEU to Better Evaluate Machine Reading Comprehension Task.ACL 2018: 98-104.
