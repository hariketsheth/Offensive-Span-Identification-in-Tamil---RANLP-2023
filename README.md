# Offensive Span Identification in Tamil @RANLP-2023

## Offensive Language Detection in dravidian languages (Tamil)

| Faculty | Slot | Course | Course Code | 
| :--: | :--: | :--: | :--: |
| Dr. Ratnavel Rajalakshmi | L33+L34 (G1 Slot) | Essentials of Data Analytics | CSE3506 |

<br>

| Name | Register Number | Branch |
| :-- | :--: | --: |
| Hariket Sukesh Kumar Sheth (Team Leader) | 20BCE1975 | CSE Core |
| Manasvi Maheshwari | 20BAI1032 | CSE AI & ML |
| Suraj Shah | 20BRS1122 | CSE Robotics |

<br><hr>

All of the work completed for the tasks related to Offensive Language Identification that RANLP 2023 organised on Codalab is included in this repository.
`To execute these programs, you must have the following:`
1. pytorch
2. transformers
3. sadice
4. seaborn
5. sklearn
6. matplotlib

The pretrained transformers BERT, IndicBERT, and XLM-Roberta were employed for the job of ``Identifying Offensive Language``. We have utilised modified versions of these models in addition to the original versions of the pretrained transformers.
The customised versions were created by freezing the basic layers and then layering a fc layer on top of it with `nll_loss` and `sadice loss` custom loss routines.


In order to reproduce the results obtained you can clone this repository and place ur dataset path in the  train scripts to run the same.

Our results for the Offensive Language Identification Task

> 

| Table: Results on Offensive Language Development Dataset | Table: Results on Offensive Language Test Dataset |
| :--: | :--: |
| ![image](https://user-images.githubusercontent.com/72455881/230711003-bb4bb80f-0f47-4b6d-bedc-5005848a05e9.png) | ![image](https://user-images.githubusercontent.com/72455881/230711014-7e660873-8cae-4691-8e78-023a10882948.png) |

<!--
  | Model Name | Accuracy |
  | :-- | :--: |
  | mBERT Cased | 0.76 |
  | XLMR | 0.76 |
  | IndicBERT | 0.74 |
  | XLMR With NLL Loss and Class Weights | 0.64 |
  | XLMR With Sadice Loss | 0.61 |
  | mBERT With Sadice Loss | 0.61 |
  | mBERT With NLL Loss and Class Weights | 0.58 | 
  
  | Model Name | Accuracy |
  | :-- | :--: |
  | mBERT Cased | 0.75 |
  | XLMR | 0.75 |
  | IndicBERT | 0.73 |
  | XLMR With NLL Loss and Class Weights | 0.64 |
  | XLMR With Sadice Loss | 0.61 |
  | mBERT With Sadice Loss | 0.61 |
  | mBERT With NLL Loss and Class Weights | 0.59 | 
  
-->

