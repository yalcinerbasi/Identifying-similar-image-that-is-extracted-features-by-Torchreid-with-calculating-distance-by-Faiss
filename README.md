# Getting Started

This project has been developed that compares a person image in input_image folder with person images in all_images folder and returns the closest person images to output_images.

5 different people images were captured from the video at 5 different times and their coordinates were determined and cut using BBox Tool (https://github.com/puzzledqs/BBox-Label-Tool)

# How to Work

First of all, feature extractions of all person images were calculated using Torchreid, and cosine distance between all person images and the person image given as input was calculated using Facebook Faiss, and the most similar pictures according to this distance metric were saved in the output-images file.

# Built With

Python (Conda Enviroment) and Bash Script are used to complete these tasks.

* [Python] Version = 3.7


# Dependencies

### create environment
conda create --name torchreid_faiss python=3.7
conda activate torchreid_faiss

git clone https://github.com/KaiyangZhou/deep-person-reid.git
cd deep-person-reid/

### install dependencies 
###### make sure `which python` and `which pip` point to the correct path
pip install -r requirements.txt

##### install torch and torchvision (select the proper cuda version to suit your machine)
conda install pytorch torchvision cudatoolkit=9.0 -c pytorch

### install torchreid (don't need to re-build it if you modify the source code)
python setup.py develop

### install faiss
conda install -c pytorch faiss-cpu
conda install -c pytorch/label/nightly faiss-cpu

# Installation

cd ../ ## go to main directory
### show path of test image
bash pathofimage.sh input_image/test.png 

### activate enviroment
conda activate torchreid_faiss

### run python script
python script.py

# Contact

Yalçın Han Erbaşı - yalcinerbasi@sabanciuniv.edu






# Identifying-similar-image-that-is-extracted-features-by-Torchreid-with-calculating-distance-by-Faiss
