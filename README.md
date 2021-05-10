# Brain-Tumor-Segmentation

Brain tumor is one of a deadly disease that needs high accuracy in identification and medical surgery. Brain tumor can be identified in MRI. We used deep learning and computer vision techniques to detect tumor in MRI images. 


## Dataset
The dataset we will be using the data from the [Decathlon 10 Challenge](https://decathlon-10.grand-challenge.org)

- Dataset is stored in the ***NifTI-1*** format and we will be using the ***NiBabel*** library to interact with the files.
- Each training sample is composed of two separate files:
  - The first file is an image file containing a 4D array of MR image in the shape of (240, 240, 155, 4).
  - The second file in each training example is a label file containing a 3D array with the shape of (240, 240, 155).


The colors correspond to each class.
- *Red* is *edema*
- *Green* is a *non-enhancing tumor*
- *Blue* is an *enhancing tumor*. 

An example of a single MRI with labels visualization

![gif](https://user-images.githubusercontent.com/55098118/117672689-b2b8dd00-b1c7-11eb-827e-d10c7cc4bcb6.gif)

An example of patch from whole mri image

![patch](https://user-images.githubusercontent.com/55098118/117673074-12af8380-b1c8-11eb-830c-36a4f3a6780b.png)

## Model
For segmenting tumor in MRI we used [3D U-net](https://arxiv.org/abs/1606.06650) as our traning model.

- Below image shows the architecture of **UNet** model
![unet](https://user-images.githubusercontent.com/55098118/117673870-d03a7680-b1c8-11eb-8d5a-055cbb356da5.png)

These are the scores achived after traning 15 epochs:
- validation soft dice loss : ***0.7117***
- validation dice coefficient : ***0.2960***

### References

[1] https://arxiv.org/abs/1606.06650

[2] https://decathlon-10.grand-challenge.org


---------------------------------------------

<h3 align="center">Connect with me:</h3>
<p align="center">
<a href="https://linkedin.com/in/manideepgujjari" target="blank"><img align="center" src="https://raw.githubusercontent.com/manideep03/manideep03/ac2f1c13beae920dd2dbcdcff9e8c04f1b9d323a/linkedin.svg" alt="manideepgujjari" height="30" width="40" /></a>
<a href="https://github.com/manideep03/" target="blank"><img align="center" src="https://raw.githubusercontent.com/manideep03/manideep03/ac2f1c13beae920dd2dbcdcff9e8c04f1b9d323a/github.svg" alt="manideep03" height="30" width="40" /></a>
</p>
