# cms-gan-super-resolution
Using Generative Adversarial Networks (GANs) for super-resolution tasks on the CMS detector dataset. 

Dataset : https://cernbox.cern.ch/s/EYgmOkI9BjwxNqy

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
