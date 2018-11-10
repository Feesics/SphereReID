# SphereReID

This is my implementation of [SphereReID](https://arxiv.org/abs/1807.00537).

My working environment is python3.5.2, and my pytorch version is 0.4.0. If things are not going well on your system, please check you environment.

I only implement the *network-D* in the paper which is claimed to have highest performance of the four networks that the author proposed. 

### Train and Evaluate
* To train the model, just run the training script:  
```
    $ python train.py
```
This will train the model and save the parameters to the directory of ```res/```.

* To embed the gallery and query set with the trained model and compute the accuracy, directly run:
```
    $ python evaluate.py
```
This will embed the gallery and query set, and then compute cmc and mAP.


### Notes: 
Sadly, I am not able to reproduce the result merely with the method mentioned in the paper.  So I add a few other tricks beyond the paper which help to boost the performance, these tricks includes:   

* During embedding phase, aggregate the embeddings of the original pictures and those of their horizontal counterparts by computing the average embeddings, as done in [MGN](https://arxiv.org/pdf/1804.01438.pdf).   

* 

