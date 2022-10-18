# FloodNet - Low point flood depth estimation & inundation modeling
Repo housing code related to the estimation of flood depth at low points and initial inundation modeling work

## Python environment setup
The commands below setup a conda environment for this repo.

Use the following if the machine you are using does not have conda installed and is running the `zsh` shell:
```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o ~/miniconda.sh
bash ~/miniconda.sh -b -p $HOME/miniconda
source ~/miniconda/bin/activate
conda init zsh
```

This sets up the conda environment:
```
conda env create -f environment.yml
conda activate inundation-model
python -m ipykernel install --user --name=inundation-model
```

To grab the data, unzip it and delete the zip file run this (uncompressed data is 121GB):
```
mkdir data && cd data
brew install wget (if on a machine without it)
wget https://sa-static-customer-assets-us-east-1-fedramp-prod.s3.amazonaws.com/data.cityofnewyork.us/NYC_DEM_1ft_Float_2.zip
unzip NYC_DEM_1ft_Float_2.zip && rm NYC_DEM_1ft_Float_2.zip
``` 

TODO: go from a sensor lat/lon to an image file of the surrounding elevations for that sensors
TODO: return loweest point within X meters of sensor location
TODO: add to readme
