**FLASH (Week 5/Week 2):** 

- Pretrained models that were provided by authors were run and verified last week.

- Last week, I retrained the models from scratch and was able to complete the reproducibility process for 6 datasets.

- This week, I focused on solving the issue with the OpTC dataset and the issue with the Word2Vec trained-from-scratch model not being used.

**OpTC**: Had an error earlier with XGBoost being used in my environment, but was able to fix this.

Again, a function for training word2vec is included in the script, but never runs. Moreover, it is not clear as to what file’s path has to be passed into this function as a parameter.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXepGym7aF-AbUs6a0V-XWausbHdkI0f1sBn2FEwxyBX3u7kwCk8CWstNJAHg1lGyepcSSkZuu28TaEB8Eg4RZ6fjQ1wmjyJOZ3iXwYlkAlKwv46JvIe61UAkAhQM_xk58sUOJYt?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

We contacted the authors of FLASH regarding this and they provided us a link to the OpTC dataset containing the benign files required to train a Word2Vec model from scratch. However, they did not address the missing code / lines that call this function in the script.

Moreover, it was not clear what files from the Drive Link provided were to be used to train the model, currently the assumption is that all files are used, which is unlikely. 

**The main issue at hand is to first inquire about the lines of code required to train the model, particularly how many and which files.**

I have modified the code scripts for other datasets but was hesitant modifying the code for training the Word2Vec model as I would like to first ensure that the code is working fine with a pre-trained Word2Vec model **and** scratch-trained GNN and XGBoost models, before proceeding with training a scratch Word2Vec too.

When running the code from scratch, retraining all of the models, there is this line of code that raises an error: ‘file\_path = ‘Enter path to train file here’.

Understandably, I would need to add the file path to the train file, but I have no idea what ‘train file’ refers to. There aren’t any instructions regarding what this might be.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeMtETDpzx6lzwrtacSz6AqaLzDPA1Redt-1R5rHIeyFparda69vkFb9zjn8kKH7vERyNNo2GFOnnjLaotxGCENJdCa8AIpAMlIW0mMja-QnxeVfLQzy8fTIhIzAUfbJk0SNftF?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

Similar issue later in the code:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEnXmfmUaDBuGUYyAFaK80DQ0ki6P8YDyIRGaNQLQ8E5dMBZ2t2s20qNDP-rwUdHv6sC2QAi7v3nsslCv2rjw3ctXpufYkFWLFnz0OwEndrJEU5cqdSIaAdZ8vLlb5LOBkAPvA-w?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

Had raised a Github issue regarding this last week. This week, we emailed the authors of FLASH about this, and we have not received a response to this query yet.

As the issue is (slightly) similar to the Word2vec train file path issue, I believe the authors have given clarity on how to get the train files; download the benign training files from the ‘ecar’ dataset link they provided.

However, again the main issue at hand is what files are to be used for the training process. We have sent a follow-up to the email received earlier, inquiring about the exact files we need to use to train the GNN and XGBoost models, but have not received a response yet. 

A GitHub issue was also created by another reviewer on the same topic but was never answered. This is keeping the OpTC reproduction on hold.

**Unicorn**: 

Last week, I was in the midst of training the model from scratch. I managed to fix a part of the code that helped speed up the process and produce results. However, these results were very far from what was expected.

Comparison of results: Above: Pretrained Model, Below: My run from scratch.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRK4-I0jdLpApuTCHA1l5WNEpk_vQTJPPqw8ujxORw3Tf155cMs2Fisd1tfrbJzvbAkbomOHxgKrMLRdQ8lnoNtLFY-MwyMTsmis92vcuh7gwhQMBeP6h_noDYTJ0LHW_KMcVUYg?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

**—------------------------------------------------------------------------------**

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXevLZu5PQKj5hzrqmBgP11bwrxsce5iPDd8GE9-SOm-2Zc0G4vOsE7VgyByHP3IO-j_V3-4Po08mkCvXLwocGluJKiaW1qeQFhLCXMjPBngHgBttih1nHLp_zYlAieckvTlaLt1?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

I initially thought this to be a one-off and re-run the script several times. Each run on that day resulted in a even worser performance, similar to what was happening for the FiveDirections dataset.

I re-run the scripts from scratch this week, and observed that each run produced random results, none of which matched (or bettered) the results produced by the pre-trained model.

Here are the results from the last two runs:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcX4NNnJ46ZEwes6LyW0jx5TfjfiZtsWDQafOtIHbz4n_qJ71jCxY0GLP7yU-i6VTZJc_oF1044kNTaACPag_B034pyhH8rt8nAZN16uRgf-3ip6c9jzAnE__tqLbiWT4fqWOE0vA?key=0HBOu1CR7C6EgfEQ-qNjuLS9)![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJAR9Vn4dFFDN9ljb1PTbhsZIWeDLlaSKba11QykZRjPE9gQJKMrT2lS894rVrTPv3qM9q41svRfLJCuSF_9xgNjlIoHT-3p3SjTeQNGNjAFFkqSuvDzzBJWgD35ShZgc-lseUjA?key=0HBOu1CR7C6EgfEQ-qNjuLS9)

I have not raised a GitHub issue regarding this or emailed about this yet, since I believe it is more likely to be an issue at my end instead of something wrong with the code, as the other datasets have performed fine.

**Cadets**: 

Last week, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script. Results to be added here: 

**Theia**: 

Last week, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script. Results to be added here:

**Trace**: 

Last week, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script. Results to be added here: