# WearMask3D
![pipeline](/etc/pipeline.jpg)
This repository contains code for fitting masks to face images in the wild by utilizing the 3D morphable model. 
The code is provided without any warranty. If using this code, please cite our work as shown below.

## How to run WearMask3D
1. Download the dlib landmark pre-trained model.

2. Install the requirements listed in **requirements.txt**, e.g. by typing
```
pip install -r requirements.txt
```

3. Run the demo code by running
```
python main.py
```

### Parameters
Below is a list of tunable hyperparameters.

Source path:  Path of the input facial images
```
"srcPath": "./src"
```

Destination path:  Save path of the mask-augmented output images 
```
"dstPath": "./dst"
```

Version: Version of the WearMask3D's mask augmentation method. You can choose "1.1" or "1.0". ("1.1" is recommended.)
```
"version":  "1.1"
```

Brightness threshold: Pre-determined threshold value of the brightness of the input image. If an input image has a lower brightness than the threshold value, the rendered mask image becomes darker.
```
"brightnessThreshold": 0.4
```

Variance of the Laplacian threshold: Pre-determined threshold value of the variance of the Laplacian of the input image. If the Laplacian variance of the input image is lower than the threshold, the resolution of the mask image is lowered.
```
"laplacianVarianceThreshold":  400
```

## Masked Faces in the Wild (MFW-mini)
![mfw](/etc/mfw_mini.png)

## Bug report
Please raise an issue on Github for issues related to this code.
