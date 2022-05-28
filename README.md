# Final Degree Project 2021

For the code used in the paper called __*Revisiting Artistic Style Transfer For Data Augmentation In A Real-case Scenario*__ scroll down to the **Source Code** section.

## Author 
### D'Angelo Stefano <br>stefano.dangelo.ct@gmail.com
## Supervisor
### Precioso Frédéric <br>frederic.precioso@univ-cotedazur.fr 

## Description
This repository contains the code for the final degree project 2021-2022 at Université Cote d'Azur entitled:

__*Deep Learning to paint like Van Gogh*__

Its main goal is to transfer style from Van Gogh's paintings to real images, in order to augment the set of Van Gogh's paintings available.

## Deliverables

###### Legend
| Progression | Color |
|:-----------------------|:------------------------------------:|
| Not done | [![RED](http://via.placeholder.com/15/f03c15/f03c15)](#) |
| In progress | [![YELLOW](http://via.placeholder.com/15/ffdd00/ffdd00)](#) |
| Completed | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |

#### Progression table
| Task | Progression |
|:-----------------------|:------------------------------------:|
| Description of Work | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |
| Detailed progress plan | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |
| Scientific Article | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |
| Software delivery form | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |
| Video | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |
| Poster | [![GREEN](http://via.placeholder.com/15/44bb44/44bb44)](#) |

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
- CycleGAN:
  - [pretrained Vangogh2Photo model](https://drive.google.com/file/d/1NGXoMgnkBwsO6WNuZfHpwbb3aN6NLs-7/view?usp=sharing) for the pre-processing phase
- Automated Deep Photo Style Transfer: 
  - [source code](https://drive.google.com/drive/folders/1ODEgBJmRBpBPJ9uDKwEyAnSkeLL4RcJV?usp=sharing) ([credits](https://github.com/Spenhouet/automated-deep-photo-style-transfer)) 
  - [weights](https://github.com/Spenhouet/automated-deep-photo-style-transfer/releases/latest) for the pretrained model
- Neural Doodle: 
  - source code is already in `src` folder ([credits](https://github.com/gargimahale/Doodle))
  - [weights](http://www.vlfeat.org/matconvnet/models/imagenet-vgg-verydeep-19.mat) for the pretrained model
- [Dataset](https://drive.google.com/drive/folders/1r0PyD42lNfEIIKwtI_4J9NiELJOGw20D?usp=sharing)

Main credits: https://github.com/huihuangzhao/Neural-Style-Transfer-Papers-Code
## Instructions
For the pre-processing phase or to reproduce [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) results, have a look at `src/CycleGAN.ipynb` notebook. A pretrained model is available for the pre-processing step, and once you download it, just copy the folder `vangogh2photo`, containing both the 2 generators and the 2 discriminators, under `pytorch-CycleGAN-and-pix2pix/checkpoints/`. The latter should be the right path if you cloned the CycleGAN repository without changing any names. \
To generate segmentation masks, after having downloaded the source code of Automated Deep Photo Style Transfer, open file `automated-deep-photo-style-transfer/style_transfer.py` and comment lines 347-349. Then, run `src/AutomatedDeepPhotoStyleTransfer.ipynb`. \
To reproduce results of:
- **Patch-based** model, run `src/Patch-based.ipynb`
- **Neural Doodle** model, run `src/Neural-Doodle.ipynb`
- **Photo-Realistic into Painting-Like Artistic Style Transfer** model, uncomment lines 347-349 and comment lines 330-333; then run `src/AutomatedDeepPhotoStyleTransfer.ipynb`
- **Neural Style Transfer** run `src/NeuralStyleTransfer.ipynb` ([credits](https://github.com/titu1994/Neural-Style-Transfer.git))
- **CNNMRF** run `src/CNNMRF.ipynb` ([credits](https://github.com/jonzhaocn/cnnmrf-pytorch))
