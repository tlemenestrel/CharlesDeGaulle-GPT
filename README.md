# CharlesDeGaulle-GPT

## Introduction

This repository contains a version of GPT-2 finetuned on data extracted from Charles De Gaulle's speeches during and after WW2. The GPT-2 model used is a version further pretrained on a large heterogeneous French corpus (~60Gb).
    
## Table of Contents

- [Data Collection](#Data-Collection)
- [Training](#Training)

<table>
<tr>
<td>
  
<p align="center">
<img src="https://github.com/tlemenestrel/CharlesDeGaulle-GPT/blob/main/data/cdg.png" width="700">
</p>

</td>
</tr>
</table>

## Data Collection

Over 85 documents containing Charles De Gaulle's speeches were manually collected and converted to txt using spacypdfreader with the fr_core_news_sm_pipeline. The data was then pre-processed to be fed into the GPT-2 model.

## Training

The following parameters were used for training on an RTX 3090:

<ol>
  <li>learning_rate: 2e-05</li>
  <li>train_batch_size: 4</li>
  <li>optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08</li>
  <li>num_epochs: 8</li>
</ol> 
