> ## Env
    > Anaconda3 2022.10 - (Python 3.9.13 64bit)
    > Python - 3.8.16
    > Numpy - 1.23.5
    > OpenCV - 4.7.0.68

> ## Get started

#### Step1. Clone the Repository on your Desktop

    git clone https://github.com/ILXYENILXY/line_detection.git

#### Step2. Env setup

Anaconda env and Package settings are connected content with the env[Env], To start this repository, need installed various packages on anaconda env. To make this steps easier, In the git clone folder of the previous step, There will be ldetect_env yml, it is env file extracted from anaconda. run anaconda prompt in the folder cloned repository.

    (base) C:\>line_detection> conda env create -f ldetect_env.yml

and after creating the env, 
    
    (base) C:\>line_detection> conda activate ldetect

    (ldetect) C:\>line_detection>

base will be change to ldetect.

> ## Introduction

Usually, line detection uses Canny Edge Detection[CED] and Hough Transform. It is good algorithm to detect straight lines. but the road also consists of many curves. i think would be better to using contours than Hough Transform. 

> ## Pipeline

![Pipeline_img](https://user-images.githubusercontent.com/108206338/216509992-411ec6e6-4d5a-4336-ab19-614bd73b70cd.png)

* Gray scale - need convert to gray scale of input image, because, it is too much amount of computation.

* Gaussian Filter - line detection responds sensitively of the noise. therefore, need to filltering of the noise. Gaussian Fillter is commonly-used on line detection.

* Canny Edge Detection - in earnest, detection lane of though the Canny Edge Detection

* ROI Canny - Based ROI area, detection of lane from the Canny Edge Detection section.

* Find & Draw Contours - using `cv2.findContours`, `cv2.drawContours` functions, find contours of lane, and draw contours on the frame.

> ## Trouble Shooting

> ## References

