# Engagement Recognition

TensorFlow implementation of [Engagement Recognition using Deep Learning and Facial Expression](https://arxiv.org/abs/1808.02324) proposing a deep learning model to recognize engagement from human faces.

<p align="center">
<img src="images/sample_eng.jpg" width=300 high=500>
</p>


### Transfer Model
This work presents a deep learning model to improve engagement recognition from face images captured `in the wild' that overcomes the data sparsity challenge by pre-training on readily available basic facial expression data, before training on specialised engagement data. In the first of two steps, a facial expression recognition model is trained to provide a rich face representation using deep learning. In the second step, we use the model's weights to initialize our deep learning based model to recognize engagement; we term this the Transfer model. 

<p align="center">
<img src="images/VGG_eng_model.jpg" width=500 high=700>
</p>

### Reference
if you use our code or model, please cite our paper:
```
@article{nezami2018deep,
  title={Engagement Recognition using Deep Learning and Facial Expression},
  author={Nezami, Omid Mohamad and Hamey, Len and Richards, Deborah and Dras, Mark and Wan, Stephen and Paris, Cecile},
  journal={arXiv preprint arXiv:1808.02324},
  year={2018}
}
```
### Data
We train the model on our new engagement recognition (ER) dataset with 4627 engaged and disengaged samples. We split the ER dataset into training (3224), validation (715), and testing (688) sets, which are subject-independent (the samples in these three sets are from different subjects). We will release our data to facilitate research on engagement recognition from visual data.

### Requiremens
Python 2.7.12
Numpy 1.15.2
Tensorflow 1.8.0

### Contents
1. [CNN Model Source Code](/code/CNN_model.py)
2. [VGG Model Source Code](/code/VGG_model.py)
3. [Transfer Model Source Code](/code/VGG_model.py)

### Train
1. Dowload pretrained model
   /model/TF_start*
2. Run the model's script:
    python VGG_model.py train

### Test
1. Download trained model: 
   /model/TF_final*
2. Run the model's script:
    python VGG_model.py test
    
### Results
|                   | Accuracy     | F1 | AUC    |
|-------------------|:-------------------:|:------------------------:|:---------------------:|
|Transfer | 72.38%  | 73.90% | 73.74%  |
