forked from epigen/crop-seq

modify the codes to make it work on gc5 server

--------------------------------------------------------
what I did:

1) create a conda python environment with the following packages installed
argparse
FlowCytometryTools
h5py
matplotlib
numpy>=1.6.1
pandas>=0.16
scikit-learn==0.17
scipy
seaborn
statsmodels

by:
conda create -n cropseq python=3 numpy scipy scikit-learn=0.17 pandas matplotlib
conda activate cropseq
conda install -c pdrops argparse
conda install -c conda-forge h5py seaborn statsmodels
pip install FlowCytometryTools

2) manually install looper and pypiper

make a temporary "requirements" file "/tmp/1" by including the following two lines:
-e git+https://github.com/epigen/looper.git@v0.7.2#egg=looper
-e git+https://github.com/epigen/pypiper.git@v0.6#egg=pypiper

then type:
pip install -r /tmp/1

This will install the two packages under directory:
#       src/looper/
#       src/pypiper/

mask these two folders by adding them to the ".gitignore" file

