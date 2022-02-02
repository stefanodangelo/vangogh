# Final Degree Project 2021

## Author 
### D'Angelo Stefano <br>stefano.dangelo.ct@gmail.com
## Supervisor
### Precioso Frédéric <br>frederic.precioso@univ-cotedazur.fr 

## Description
This repository contains the final project of my studies entitled:

__*Deep Learning to paint like Van Gogh*__

Its main goal is to transfer style from Van Gogh's paintings to real images, in order to augment the set of Van Gogh's paintings available.

## Deliverables

###### Legend
| Progression | Color |
|:-----------------------|:------------------------------------:|
| Not done | [![RED](http://placehold.it/15/f03c15/f03c15)](#) |
| In progress | [![YELLOW](http://placehold.it/15/ffdd00/ffdd00)](#) |
| Completed | [![GREEN](http://placehold.it/15/44bb44/44bb44)](#) |

#### Progression table
| Task | Progression |
|:-----------------------|:------------------------------------:|
| Description of Work | [![GREEN](http://placehold.it/15/44bb44/44bb44)](#) |
| Detailed progress plan | [![GREEN](http://placehold.it/15/44bb44/44bb44)](#) |
| Scientific Article | [![GREEN](http://placehold.it/15/44bb44/44bb44)](#) |
| Software delivery form | [![YELLOW](http://placehold.it/15/ffdd00/ffdd00)](#) |
| Video | [![GREEN](http://placehold.it/15/44bb44/44bb44)](#) |
| Poster | [![YELLOW](http://placehold.it/15/ffdd00/ffdd00)](#) |

## Activities

- [x] Explore Neural Style Transfer implementation
- [x] Explore Convolutional Neural Network with Markov Random Field implementation
- [x] Explore CycleGAN implementation
- [x] Explore Automated Deep Photo Style Transfer implementation
- [x] Compare state-of-the-art models together
- [x] Find a model that improves the state-of-the-art
- [x] (Optional) Use semantic segmentation to see if this improves results

## Source code
In order for the notebooks to work, the following source code must be downloaded:
- Automated Deep Photo Style Transfer: 
  - [source code](https://drive.google.com/drive/folders/1ODEgBJmRBpBPJ9uDKwEyAnSkeLL4RcJV?usp=sharing) ([credits](https://github.com/Spenhouet/automated-deep-photo-style-transfer)) 
  - [weights](https://github.com/Spenhouet/automated-deep-photo-style-transfer/releases/latest) for the pretrained model
- Neural Doodle: 
  - [source code](https://drive.google.com/drive/folders/1-lkxkXrj025llmE4dDAOYCDJJUk3vYUw?usp=sharing) ([credits](https://github.com/gargimahale/Doodle))
  - [weights](http://www.vlfeat.org/matconvnet/models/imagenet-vgg-verydeep-19.mat) for the pretrained model
- [Dataset](https://drive.google.com/drive/folders/1r0PyD42lNfEIIKwtI_4J9NiELJOGw20D?usp=sharing)

Main credits: https://github.com/huihuangzhao/Neural-Style-Transfer-Papers-Code
## Instructions
For the pre-processing phase or to reproduce [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) results, have a look at `src/CycleGAN.ipynb` notebook. To generate segmentation masks, after having downloaded the source code of Automated Deep Photo Style Transfer, open file `automated-deep-photo-style-transfer/style_transfer.py` and comment lines 347-349. Then, run `src/AutomatedDeepPhotoStyleTransfer.ipynb`. \
To reproduce results of:
- **Patch-based** model, run `src/Patch-based.ipynb`
- **Neural Doodle** model, run `src/Neural-Doodle.ipynb`
- **Photo-Realistic into Painting-Like Artistic Style Transfer** model, uncomment lines 347-349 and comment lines 330-333; then run `src/AutomatedDeepPhotoStyleTransfer.ipynb`
- **Neural Style Transfer** run `src/NeuralStyleTransfer.ipynb` ([credits](https://github.com/titu1994/Neural-Style-Transfer.git))
- **CNNMRF** run `src/CNNMRF.ipynb` ([credits](https://github.com/jonzhaocn/cnnmrf-pytorch))
