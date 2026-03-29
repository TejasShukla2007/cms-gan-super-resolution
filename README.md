# cms-gan-super-resolution
Using Generative Adversarial Networks (GANs) for super-resolution tasks on the CMS detector dataset. 

Dataset : https://cernbox.cern.ch/s/EYgmOkI9BjwxNqy

The weights for the model trained can be found in [./weights](./weights) . 

[generator.weights.h5](./weights/generator.weights.h5) contains the weights of the generator immediately after GAN training.

[phy_generator.weights.h5](./weights/phy_generator.weights.h5)  contains the final weights of the generator after incorporating the $l_{\text{energy}}$ loss.

## The Model
A Generative Adversarial Network (GAN) model was trained on the CMS dataset for mapping lower resolution particle collision data to a higher resolution representation.

The architectures of the Generator and Discriminator, along with the associated hyperparameters, have been adapted from the following research paper, with minor modifications based on experimentation:
https://www.sciencedirect.com/science/article/pii/S0925231225008744

### Generator
<img width="1839" height="753" alt="image" src="https://github.com/user-attachments/assets/1ecdf27d-a58c-436d-b072-bb11bcc0742f" />
The above image has been taken from the research paper mentioned. The generator architecture in this project is based on this but with slight modifications.

### Discriminator 
<img width="1771" height="696" alt="image" src="https://github.com/user-attachments/assets/f96853c2-3ac6-424d-bd83-acc1020573bb" />
The above image has been taken from the research paper mentioned. The discriminator architecture in this project is based on this but with slight modifications.

## Results
The SR predicted cell energies perform well on super-resolution metrics with average PSNR = 44.60 and SSIM = 0.987.

<img width="1790" height="489" alt="image" src="https://github.com/user-attachments/assets/1e6ea5f0-dbc1-4da2-b2a3-575092bd25b5" />

The predictions are shown below along with the corresponding LR data and target HR data: 

Results in this project also indicate that performance of this model can be further improved by incorporating the $l_{\text{energy}}$ loss, defined in this project, during the GAN training loop.

<img width="1479" height="511" alt="image" src="https://github.com/user-attachments/assets/56af9642-0f8b-4157-b373-4a96ca0b9957" />
<img width="1588" height="552" alt="image" src="https://github.com/user-attachments/assets/7ba539e3-f5c8-4e18-99a0-de17f4bfceb2" />




