
# CAMVID_Unet_Experiments

  

### Overview

[The Cambridge-driving Labeled Video Database (CamVid)](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/) provides ground truth labels that associate each pixel with one of 32 semantic classes. This dataset is often used in (real-time) semantic segmentation research.

  

### Note

This repo contains the source related to segmentation task on CamVid dataset hosed by [FastAI](https://s3.amazonaws.com/fast-ai-imagelocal/camvid.tgz)

  
  
  

### Implementation details

| Feature | Brief Explanation |
| ------ | ------ |
| Base Model Architecture | Resnet18 from [ResNet](https://arxiv.org/abs/1512.03385) family, implementation from [PyTorch](https://pytorch.org/)|
| Learning Rate Finder | [Learning rate finder](https://arxiv.org/abs/1506.01186) implementation from [FastAI](https://www.fast.ai/) |
| Learning rate and Momentum scheduler| [Flat + cosine anneal](https://lessw.medium.com/how-we-beat-the-fastai-leaderboard-score-by-19-77-a-cbb2338fab5c) implementation from [FastAI](https://www.fast.ai/) to achieve faster converge |
| Optimizer | [ranger](https://arxiv.org/abs/1908.00700v2) implementation from [FastAI](https://www.fast.ai/) |
| Self Attention Decoder | [Stand alone SA ](https://arxiv.org/abs/1906.05909) implementation from [FastAI](https://www.fast.ai/) |
| Mish Activation Decoder | [Mish Activation ](https://arxiv.org/abs/1908.08681) implementation from [FastAI](https://www.fast.ai/) |
| Dataset | Dataset [CamVid](https://s3.amazonaws.com/fast-ai-imagelocal/camvid.tgz) from [FastAI](https://www.fast.ai/) |

  
  

### Results

| Model | Metrics(Accuracy) | Epochs |
| ------ | ------ | ------ |
| Resnet18 | 90.17%(On 128X128 images) | 22 |

  
  

#### Inference

![Alt text](https://github.com/gurucharanmk/CAMVID_Unet_Experiments/blob/main/images/results_1.png )

![Alt text](https://github.com/gurucharanmk/CAMVID_Unet_Experiments/blob/main/images/results_1.png )

  

## License

This project is licensed under the [MIT License](https://github.com/gurucharanmk/CAMVID_Unet_Experiments/blob/main/LICENSE)
