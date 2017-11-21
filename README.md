## AMCnet
# Computer Vision: African Motion Content Network
<p align="center">
  <img width="460" height="300" src="https://github.com/AfricaMachineIntelligence/AMCnet/blob/master/v_CricketShot_g04_c01_rgb.gif">
</p>
# Requirements

AMCnet tested with:

    Linux
    Intel Core i7
    Tensorflow version 1.4.0
    
# Installing Dependencies 

    pip install scipy
    pip install imageio
    pip install pyssim
    pip install joblib
    pip install Pillow
    pip install scikit-image
    pip install opencv-python
    pip install pytube
    sudo apt-get install unrar

FFMPEG needs to be installed as well to generate gif videos. If using anaconda, ffmpeg can be installed as follows:

    conda install -c menpo ffmpeg=3.1.3

# Downloading Data

    UCF101: 
            ./data/UCF101/download.sh

# UCF101 testing
      Testing with model:
             python test_ucf101.py --cpu=0
# Results
The generated gifs will be located in:
             ./results/images/<dataset>
The quantative results will be in:
              ./results/quantitative/<dataset>
The quantitative results for each video will be stored as dictionaries, a
nd the mean results for all test data instances at every timestep can be displayed as:

                        import numpy as np
                        results = np.load('<results_file_name>')
                        print(results['psnr'].mean(axis=0))
                        print(results['ssim'].mean(axis=0))
This project was inspired by the work that was done by Ruben Villegas and team on the GPU.
We took it upon ourselves to modernize the orginal MCnet code to be optimized for the CPU.
# Please note that this project is not complete yet!!!!!
# References

@article{villegas17mcnet,
  author = {Ruben Villegas and Jimei Yang and Seunghoon Hong and Xunyu Lin and Honglak Lee},
  title = {Decomposing Motion and Content for Natural Video Sequence Prediction},
  journal = {ICLR},
  year = {2017},
}
