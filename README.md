# News Category Classification

Identify the type of news based on headlines and short descriptions by fine tuning on pre-trained BERT uncased model.


## About BERT

BERT, which stands for Bidirectional Encoder Representations from Transformers, is a neural network-based technique for natural language processing pre-training. In plain English, it can be used to help Google better discern the context of words in search queries.

<p align="center">
<img width="600" src="https://github.com/milsun/News-Category-Classification-BERT/blob/master/images/bert.png">
</p>


For example, in the phrases “nine to five” and “a quarter to five,” the word “to” has two different meanings, which may be obvious to humans but less so to search engines. BERT is designed to distinguish between such nuances to facilitate more relevant results.

## Dataset

The dataset contains 200k records. Each json record contains following attributes:

- category: Category article belongs to
- headline: Headline of the article
- authors: Person authored the article
- link: Link to the post
- short_description: Short description of the article
- date: Date the article was published

<p align="center">
<img width="600" src="https://github.com/milsun/News-Category-Classification-BERT/blob/master/images/input.png">
</p>


## Results
Fine tuned model was able to achieve 82% accuracy.
Below are some out of sample predictions:
```
[('PM Modi Hardens Stance On Protesters, Who Pose His First Real Challenge',
  array([-6.5154715 , -7.7886257 , -0.75399137, -5.9940453 , -4.2135687 ,
         -7.72484   , -7.7832584 , -6.262067  , -8.085926  , -7.925973  ,
         -6.9494925 , -6.309304  , -8.293657  , -5.5070305 , -7.0753546 ,
         -6.904769  , -7.2521315 , -6.3372955 , -6.857065  , -8.015599  ,
         -7.881233  , -7.0995054 , -8.0088415 , -6.5394707 , -7.0655813 ,
         -6.981015  , -1.0736921 , -8.447243  , -1.9318712 , -8.590682  ,
         -8.383945  , -8.809869  , -9.235688  , -9.884265  , -8.44239   ,
         -8.099691  , -8.930006  , -7.976119  , -8.833439  , -7.8294954 ,
         -8.28489   ], dtype=float32),
  'WORLD NEWS'),
 ('Billions of years ago Mars had big, wide, intense rivers',
  array([-10.164058  ,  -8.552259  ,  -6.9318857 ,  -8.41971   ,
          -9.535336  ,  -6.6712923 , -10.04326   ,  -9.883109  ,
          -7.462676  ,  -9.108592  ,  -8.674977  ,  -7.725085  ,
          -8.46935   ,  -8.644373  ,  -6.536705  ,  -8.940154  ,
          -0.02220168,  -8.339192  ,  -8.040723  ,  -9.072937  ,
          -8.803793  ,  -7.7881737 ,  -7.6218023 ,  -6.2437706 ,
          -7.845797  ,  -6.8099074 ,  -5.914486  ,  -8.849068  ,
          -7.6748075 ,  -8.439492  ,  -7.091228  ,  -7.8040953 ,
          -8.904095  ,  -7.8750706 ,  -8.938344  ,  -8.56688   ,
          -7.14773   ,  -7.507223  ,  -8.753856  ,  -5.8121176 ,
          -7.455835  ], dtype=float32),
  'SCIENCE'),
 ('The film was creative and surprising',
  array([-7.7040215, -1.0293102, -6.8923616, -4.952792 , -5.111165 ,
         -6.954315 , -2.4609525, -4.6206093, -4.1399984, -2.1357315,
         -4.971432 , -5.164293 , -5.0581775, -4.664072 , -6.2247214,
         -4.9402494, -6.140673 , -5.1794496, -6.463245 , -6.010908 ,
         -5.2263217, -3.4671912, -4.679649 , -7.321819 , -6.8393226,
         -5.4467444, -6.5966196, -7.08523  , -4.847103 , -5.9624367,
         -1.5037777, -5.1998515, -5.0846314, -6.4759407, -4.7600803,
         -5.520092 , -5.912579 , -6.323898 , -7.4525394, -7.5091567,
         -3.495819 ], dtype=float32),
  'ENTERTAINMENT'),
 ('Gaming machines are powered by efficient micro processores and GPUs',
  array([-6.923841  , -7.5176897 , -5.666759  , -5.9771748 , -8.385565  ,
         -6.5320063 , -7.4589543 , -8.129181  , -8.69984   , -7.9544897 ,
         -7.070156  , -3.2465584 , -6.793621  , -6.246279  , -0.12876646,
         -7.5667496 , -4.2696624 , -7.4210143 , -5.9329557 , -6.444842  ,
         -8.290107  , -6.3658404 , -7.003379  , -6.9174986 , -6.0500865 ,
         -6.131018  , -4.3399906 , -6.5386376 , -5.283232  , -7.8250046 ,
         -5.8118753 , -7.2823906 , -7.92196   , -5.6401763 , -8.163938  ,
         -7.7866626 , -7.2878127 , -6.9017143 , -5.4717903 , -6.2594504 ,
         -5.624967  ], dtype=float32),
  'TECH')]

```