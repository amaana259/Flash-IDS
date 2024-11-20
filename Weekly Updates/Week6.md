**FLASH (Week 6/Week 3):** 

- Pretrained models that were provided by authors were run and verified last week.

- Last week, I focused on solving the issue with the OpTC dataset and the issue with the Word2Vec trained-from-scratch model not being used.

- This week, I focused on re-running the Cadets, Trace, Theia and OpTC datasets from scratch.

**OpTC**: 

Same issue as last week. The authors haven't responded to either our emails or the GitHub issues.

Had raised a Github issue regarding this earlier. Last week, we emailed the authors of FLASH about this, and we have not received a response to this query yet.

As the issue is (slightly) similar to the Word2vec train file path issue, I believe the authors have given clarity on how to get the train files; download the benign training files from the ‘ecar’ dataset link they provided.

However, again the main issue at hand is what files are to be used for the training process. We have sent a follow-up to the email received earlier, inquiring about the exact files we need to use to train the GNN and XGBoost models, but have not received a response yet. 

A GitHub issue was also created by another reviewer on the same topic but was never answered. This is keeping the OpTC reproduction on hold.


**Cadets**: 

Last two weeks, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script.

Results using pre-trained model:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcSIalkaqpM7FJ1UF6fqf6K3U9IqWhGblXdOFDDxJ9KTKqwyj4B9ZDfWvA_Ld9xfD8ewo-Ym28QHYnIEAUSR8xkrUaW36JdSWcOi80ng253WMN_ZQKZafzqd3-uppbTdZuwfsfhJg?key=tc3eE6OCaujTVD4DI05zEqkv)

Results using model trained from scratch:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfFPbwh7HytMMWs5pUbkCB41oSH3Mm4jn9p2hSDD4ZzTdnZCrWiIMC61p9YBILcUEMwiIg3ZkKuMaCjA6htwPPHCDenNlausJQfqYvJzRPq25WJ9Or12cmLSbPzP2lLZrBXwxJBSQ?key=tc3eE6OCaujTVD4DI05zEqkv)

**Theia**: 

Last two weeks, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script.

Results using pre-trained model:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemxhZJv3zO7WWSRPdbxVKSYhpICvsUpHGw0a_GeZz3ueb0JVkasdZGYQYq1tWymGZMMqCCLvK0L2VNl5ukkOGUu80EbNAN_FswuYneHYN6cjlGgXKpw_nvJNAAeSErjlq0EVGmOw?key=tc3eE6OCaujTVD4DI05zEqkv)

Results using model trained from scratch:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-J5igzaawb80IsJ5UQT27faG4b3UX1aE4DeYaEA4LWN1gIOUQ30FZbUxKWDaHdGx1A0NHTuQ8crkgRSvEDyuoN7rBihUGrrjS36Jk5pTfb8_tgVw7uKvJ3XCstN18PZZ59_K4aA?key=tc3eE6OCaujTVD4DI05zEqkv)

**Trace**: 

Last two weeks, I trained the model from scratch and believed that the results were reproduced correctly. I noticed after working on streamspot that the code scripts did not use the scratch-trained model and the code lines for this had to be added.

This week, I added the same lines and re-ran the script. 

Results using pre-trained model:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1QqKlHHryaR2NBRIpijLvy1HpNJAUtFUwicR6AZzLKdtC3f-a4P1Bt_noeqzCP9mbE2nHforFyQHxZM7kF27it9xAA487JfZv8l1ASnNhvHqn47wgXdWS5SNj1bAkjeKUOkmymQ?key=tc3eE6OCaujTVD4DI05zEqkv)

Results using model trained from scratch:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcp27xzK9sqgm9CxRF7_PPA6Llif1YUDVt1vjG7LsyJbb_pPncV1xWXlgh6RVeYXUoZZhf5f9YNEZmk1DRQobO0qX3juFy6r9ampMXr76a9bywtb6FNG8JyfRbSN16YeLsm-12r?key=tc3eE6OCaujTVD4DI05zEqkv)
