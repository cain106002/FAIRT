# FAIRT
FAIRT is a Fast Automated Image Reorient Tool for human brain 3DT1 MRI image.
It could be also found at https://gitee.com/heng1988/FAIRT

manual
1) download the F_deep_reorient.m and F_Reorient.py. One function (y_Reslice.m) from DPABI was used in the code, so SPM and DPABI were required.
2) download the keras models:

   the six .h5 files at https://github.com/cain106002/FAIRT/releases/latest
   
   For Chinese User, the .h5 files could also be downloaded at https://pan.baidu.com/s/18bvwnmvWpMHukmq_MNOmbQ 
Password：4s5m
3) put the six .h5 files with the same folder of F_deep_reorient.m and F_Reorient.py
4) create tensorflow/keras running envirement. Here we recommend to use virtual enviroment by Anaconda3.x (https://www.anaconda.com/distribution/). Here we would show an example for Windows user. It is similar for Linux user.
5) open Anaconda Prompt in the start menu

step 6-9 were only done at first run

6) create a virtual enviroment: conda -n DRT python=3.6
7) activate virutal enviroment: conda activate DRT
8) install tensorflow cpu version: pip install tensorflow

   if the user have CUDA compatible GPU card (nVidia GTX 2060 or above was recommended), you could try the gpu version:
   pip install tensorflow-gpu
9) install keras: pip install keras

10) run MATLAB in Anaconda Prompt: conda activate DRT 

    then run matlab at the same prompt 
11) save the dir storing F_deep_reorient.m in the PATH of matlab
12) structure the 3DT1 images as below
    
    DATA_PATH-----sub01-----anat.nii
    
                -----sub02-----anat.nii
             
                -----sub03-----anat.nii
13) run F_deep_reorient(PATH_STORING_MRI_DATA,PATH_OUTPUT,PATH_OF_EMPTY_TEMPORAY_DIR)
14) the reoriented MRI data were stored in PATH_OUTPUT.
