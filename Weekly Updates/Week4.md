**FLASH (Week 4/Week 1):** 

- Pretrained models that were provided by authors were run and verified last week.

- This week, I retrained the models from scratch.

- I was able to complete the reproducibility process for 6 datasets, namely:

**Cadets**: Model from scratch provided the same results as the pre-trained model: 

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-3ywgHpja8M7kJz2XDW6L6o5NhkGc3hzAQFW7reoNC9KnNc1nMaHkVWRmmxQikejU1PKTg95546ri7f4zmRgkpI8h5BS0aVg2qdWFnMvXdmCpwLahfFJ0hlFgV3Ve_ADepg7XVRNA-BcjiXSiltlTTGQB?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\


**Fivedirections**: Model from scratch did not provide same results as the pre-trained model. In fact on multiple runs, the performance kept getting worse. 

This is the dataset that the authors had very poor precision on, but the results after training the model from scratch have even lower precision values. I made sure to make multiple runs, all with fresh files, this was the result of the last run I made:

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfSlOi3eNq6v9jUjcIyb4qPNbMtq7Xcp1zAnxX5TakxpYsiJqk4Zhfq4A_9DdRrvqaHgEKjsiIGh0NZAOPvkhD5dnEsHzxeAMfg_VKzB1y9qUkgH5tU4tUM8A5QxRGmAX-7aob_BKJ1jVHEKF-B2Qg--gI?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\


While these are the results on the pre-trained model:

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRU9OY2WQJG5vI3Onmj-9D86bpGTT6NBgCN4MoiPsUks8_4-zvlpkP6tPO8vXWbW2pf0cU4iD_dJSxsRnJdIGn-MPgCKuGV7QuvNVPbxwSdfOwEfitoasD0R3Aq9N3iSkC1cZbvdYX1N2ewLTxWniniB29?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\


**Theia**: Model from scratch provided the same results as the pre-trained model: 

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYwFVfe3GdfVENwZaxCqlLD44AhXh7ILgJy04vPmN9l_scEfgEqySmkKE6Thh-LSI6iKCDTvvyNuSYP_NEDO1rVjUitFC8OzNxn6g8ZQev5pUDWuiECPgOWRBBCXUFLWmJIT7ZGAskMibVYzgJO_lgqems?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\


**Trace**: Model from scratch provided the same results as the pre-trained model: 

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdXCBt_iZse8umYfBBzgpbMKPUDizoDmKBZ1yZaLdR_SeBAznkLmY-h5Y-wmcEIZO7-3zJZst7Aqhf9Ryg83zktVqHb8HYc4bHFIchGIToYQM3KMpK4Iyip3xPrLSF5VT-LQdtqI3h1gnAo2MZMegsMPcKJ?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\


**Streamspot**: The code provided to run this was erroneous;

1. The dataset had to be downloaded manually from a link, but then the parser provided for the files was functioning incorrectly. Particularly, it divided the files into separate directories, but then the code after would not be accessing the directories. I had to modify the parser so that the parsed files would have correct structure and access.

This code used a variable ‘scene’ that would create ‘streamspot/0/1.txt’ for example, which would be incorrect for use in later code. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdoGdu4nJGNhNDf3yTo-FyYGUpQOODV5_N4zC2PQxb-5Ha-lsJoxpH9r2woiez8ldK3TfblNitKIlMtOexa9vsG0ChhwtZ8krI-e3d-ZGsvpD2RLcmfAvlD5Kk7OFey6U19OrA5sCG-97GO0Y4fHPhyfAT4?key=-sDb-ENbuLLxKxQ1iK1g-B17)

Use in later code: 

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcQ6z4ksEPxnekJgNzEcm5R-5-lTGEAoC_BOGEu5IK9E0Vlo34NQaP_doKrSl_fq4M56IEgPXp7Wn0cnwqs162GVts790_6nvRJRk4fzeh3eifQHwWRzZ-nUUhDeVuO_jkn9pLfbEDjw3Z5DZRLKvg2olds?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\


Changes made: 

\
\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeIhco6qNZkN_XQbUyQdyBMzJBVlLO8EEKp4HKlun15PW3ZcewqYyawJTG9glXuBltcD64LEDyZ3Cqk5auKz452hIwoH7tNI6cITSNcuyktrXJc3pyJuF9IN2xoKXaXlD9tYaZjNdNHtzzKZf4xyEnBCJg?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\
\


2. The word2vector model was being trained from scratch (if Train\_Word2vec was True), but the model trained from this was not being used in the code anywhere. I had to include lines of code to ensure that my trained Word2vec model was the one that was to be used.

A ‘word2vec’ variable is created but not used in further code.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQ4UdqeiVtW2fEikcvd56kbdFzgKFU8MXqKVBLDw9fRh5kirsDnuPTKhcNFqzcY17xGQFhp2WqFF819IUaFmlm1DJ7jxujRkzboKpMdr7AA3mU6mrEIN4M31zwrLHQdbkBWoDFFxGWV7SSXORKV_H9oNE?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\


A new ‘w2vmodel’ is initialised and used regardless of the Train\_Word2vec variable value.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdCHD0WktyHJ017yoM-lwtlUzbJHxKCjq3wtjDX76OWJMO3ueoOPSH_k7YUvLxH91zBs7FdXE9f3bOUypZ4jeyJgDIg-ZrOdqHzNH5INGmv9qZI7G8Pi8SfXE4FYFCBeuk0AMTPEKKpdvnqc721Uem-jhzT?key=-sDb-ENbuLLxKxQ1iK1g-B17)

I made the following change to ensure that my trained model from scratch would be used:

\
\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc4QgEukxfpOSTQWyDKSsOsz35YKf38_DSY1wOC4c5cPVOHVaLfJZ-wnQjjhgISNIG7HCXUr4aqk1grAKQmNW_optGVsiiu-soESDt1lAK2Yq9Fa_4UU-0WVGjJSfniK_koYXeQMILlN3dnq7Ay9qj0noQ?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\


Model from scratch provided the same results as the pre-trained model:![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfhgCGD4t3Bo4Uua0pJ9HMB9K8KHC2ftQ6u1Bh0CYJgJnoZy8W33QGwsc14-yi1QFfwArmLqgRSE3AsygBk0mZgextykkUUkCK2kGVkVE8ltv5J51mDJq7UOIkY1dVgk90Jcd4QOZbe33JyOMzYy7x5lC9I?key=-sDb-ENbuLLxKxQ1iK1g-B17)

\
\
\
\
\
\
\
\


**OpTC**: Had an error last week with xgboost being used in my environment, but was able to fix this.

Again, a function for training word2vec is included in the script, but never run.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcOdE2h11hrBjuG3nBlEIkzfA0lTvj6-CEJ0C1qqiMqivtgRWuG8LMSk3Jzu5KcetEKgxtBShZCPwkFpbeDCvflTkWyOQpYsdNJk4B4u5rvulfKs0_bIFmhMegjhbI-LPQkWs7IP4fCenbUpPxkvKx4bbL7?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\


I did not modify the code this time, as I wasn’t sure if modifying it would result in correct functioning (as it is supposed to) throughout the script file.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXesB1eWP8DKuBQ0Rg-e3HHc-OPJcpBxn4Jhhp9n7seckeQF1qobZyywqdhuhFoj-ZuUQpza-931HXYqR0fm20YtXii8xDmvcWMU1Yc1z7Q0TjKa6S7-WIMPjDOcsJo0Vt2WSopayqyKodSNL8RmzU9kdxbh?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\


I was then able to run the code for the provided pre-trained model.

\
\
\
\


When running the code from scratch, retraining all of the models, there is this line of code that raises an error: ‘file\_path = ‘Enter path to train file here’.

Understandably, I would need to add the file path to the train file, but I have no idea what ‘train file’ refers to. There aren’t any instructions regarding what this might be.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdtla7NeMuY5rz2i1LGVoQVt8P4XitqKXEn4lG-KK5p3xj5R0nVwcL1Of3gqw1tm37SRxrbc2hFJPXKxB2kqedWdCHufZSSkyCO6oSEVebo2Qyzr1vmzhhXg_C0qri15dbI8GdeL_5KYuMu6AGgR14Brc1o?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\


Similar issue later in the code:

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJ9-zV1kEK5VknY2iCjrxIU5XAvPV36iSWQBGlvdeuOTIfOGjW2uM066aN5TLiiDQWKJUhxVnKUkfTQBvTq2cQN3oENbKcljEF_n8W7fw1hb3KycZcdKXmMKwgT6BJ0J-CQXx33ailQgwAoTCHx08upRor?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\


Have raised a Github issue regarding this.

\
\
\
\
\
\
\
\
\


**Unicorn**: The (scratch) model is still being trained, I have only ran the pre-trained model as of yet. This dataset is taking unusually more time than the others, the reason for which I have pinpointed to this specific function:

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfHOGuBKb7L_uR-7B6OblLWXHn8HLG4NMtO2oOlzGnoqnWi9SxLyt8cd6SAcO3OSkox_YxT3Lr260xCTY0T38q-gxjVHzog1fIDZhKlJqyYUFEdWQ-nVPy8qa3SGzRcBgQ8LOV0bzy8iiXHmUAdnGbFs32K?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\
\


The function had been running for over 5 hours, until I interrupted it. I saw that a Github issue had been created regarding this and someone had suggested an edit that produced the same results but in much less time.

I have made the edits for now and am trying to see if I am able to reproduce the same result.

\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcHnL8gky8DAHk3VDfEd0HZlRnAuiEjhsrbUNC93gJphIOGxKZNyt_3oRa3nOskIrtkdzzcgej_sY_cFfSWT9Bl1vItTepPOKrfeV8djUb12Wk_yMtPP7M2oqlqciVR51boWF36pkLxB624FHXau1Nsuqsu?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\
\


Comparison of results: Left: Pretrained Model, Right: My run from scratch.

\
\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdE6wX6k7x8Lbk2RxHJHhGTYP1l7XAFwvW6nHsw-MlpRi3UUOWyTxk5jVkq0-aBbW8qdmrjyDHZeRYVrzwYLfSvrf2Y0uvcdprAQ9-icvzXk0jNAe9IzTgtqkih3HkKJ1QR4jqnL5StRbbVQ91JiLuE8y4?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfejzsi0OasrmOt8WOHqYAn_TRJwW2zouXWjwmVDbohj1WcCzCxNruYBzz_WLgRiu_8bN2eIBcvEHsEq-FWq9k4rZzsSxb0BJNL_iOAUBX5TDhEcBdzt0_vQBDyxlpsew78wZjiy0CwN3q_Q253G_0oC7Ev?key=-sDb-ENbuLLxKxQ1iK1g-B17)\
\
\
\
\
\
\
\
\
\
\
\


However, the results on the right are after I made the edits in the code. It might be possible that the results match if I run the original code but the run takes a lot of time. Moreover, I do not think the edits suggested _do anything different_ from what the original code intends to do.
