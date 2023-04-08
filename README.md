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

<hr>

Our results for the Offensive Language Identification Task
 

| Table: Results on Offensive Language Development Dataset | Table: Results on Offensive Language Test Dataset |
| :--: | :--: |
| <table><tr><th>Model Name</th><th>Accuracy</th></tr><tr><td>mBERT Cased</td><td>0.76</td></tr><tr><td>XLMR</td><td>0.76</td></tr><tr><td>IndicBERT</td><td>0.74</td></tr><tr><td>XLMR with NLL Loss and Class Weights</td><td>0.64</td></tr><tr><td>XLMR with Sadice Loss</td><td>0.61</td></tr><tr><td>mBERT with Sadice Loss</td><td>0.61</td></tr><tr><td>mBERT with NLL Loss and Class Weights</td><td>0.58</td></tr></table> | <table><tr><th>Model Name</th><th>Accuracy</th></tr><tr><td>mBERT Cased</td><td>0.75</td></tr><tr><td>XLMR</td><td>0.75</td></tr><tr><td>IndicBERT</td><td>0.73</td></tr><tr><td>XLMR with NLL Loss and Class Weights</td><td>0.64</td></tr><tr><td>XLMR with Sadice Loss</td><td>0.61</td></tr><tr><td>mBERT with Sadice Loss</td><td>0.61</td></tr><tr><td>mBERT with NLL Loss and Class Weights</td><td>0.59</td></tr></table> |


