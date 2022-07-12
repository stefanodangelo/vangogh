# Revisiting Artistic Style Transfer For Data Augmentation In A Real-case Scenario

## Authors
### D'Angelo Stefano <br>stefano.dangelo.ct@gmail.com
### Precioso Frédéric <br>frederic.precioso@univ-cotedazur.fr 
### Fabien Gandon <br>fabien.gandon@inria.fr

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

All the packages that were present in the VM used to run the code are listed in `requirements.txt` file. Note that not all of them have been used, so it is not necessary to install them all.


Main credits: https://github.com/huihuangzhao/Neural-Style-Transfer-Papers-Code
## Instructions
1. For the pre-processing phase or to reproduce [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) results, have a look at `src/CycleGAN.ipynb` notebook. A pretrained model is available for the pre-processing step, and once you download it, just copy the folder `vangogh2photo`, containing both the 2 generators and the 2 discriminators, under `pytorch-CycleGAN-and-pix2pix/checkpoints/`. The latter should be the right path if you cloned the CycleGAN repository without changing any names. \
2. To generate segmentation masks, after having downloaded the source code of Automated Deep Photo Style Transfer, open file `automated-deep-photo-style-transfer/style_transfer.py` and comment lines 347-349. Then, run `src/AutomatedDeepPhotoStyleTransfer.ipynb`. \
3. To reproduce results of:
- **Patch-based** model, run `src/Patch-based.ipynb`
- **Neural Doodle** model, run `src/Neural-Doodle.ipynb`
- **Photo-Realistic into Painting-Like Artistic Style Transfer** model, uncomment lines 347-349 and comment lines 330-333; then run `src/AutomatedDeepPhotoStyleTransfer.ipynb`
- **Neural Style Transfer** run `src/NeuralStyleTransfer.ipynb` ([credits](https://github.com/titu1994/Neural-Style-Transfer.git))
- **CNNMRF** run `src/CNNMRF.ipynb` ([credits](https://github.com/jonzhaocn/cnnmrf-pytorch))

## Testing
To assess validity of the methodology, follow these steps:
1. Unzip `src/classifier_dataset.zip`
2. Run `src/Classifier.ipynb` notebook
