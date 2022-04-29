# how to download and use the jGCaMP8 ground truth dataset (NWB_tutorial.ipynb)


## The data generated with this pipeline is in the following DANDIset:
https://dandiarchive.org/dandiset/000168/

## Please read the paper for additional information:
https://doi.org/10.1101/2021.11.08.467793 

# Dataset description

This dataset contains simultaneous 2-photon calcium imaging movies and loose-seal cell attached recordings of upper layer 2 pyramidal cells and interneurons of the primary visual cortex of wild type mouse, in vivo, during drifting gratings stimulus in the contralateral eye.
jGCaMP8f, jGCaMP8m, jGCaMP8s, jGCaMP7f and XCaMPgf were expressed via AAV injections using synapsin-1 promoter.

Multiple neruons were recorded in each mouse, and multiple ~3-minutes-long recordings (movies/sweeps) were performed for each cell. One .nwb file contains all the data for a given cell. 

The dataset contains:
- raw 2-photon movies
- raw cell attached loose-seal electrophysiology traces of a single neuron in the field of view
- somatic cellular and neuropil ROIs that were segmented with Suite2p
- the fluorescence traces for all ROIs
- details of the drifting gratings stimuli presented to the contralateral eye

#### To install this script and dependencies, type in terminal (in a directory you want to have this script):
```
git clone https://github.com/rozmar/jGCaMP8_ground_truth_dataset.git
cd jGCaMP8_ground_truth_dataset
conda create --name GCaMP8Mouse python=3.7
conda activate GCaMP8Mouse
conda install --channel=conda-forge jupyter dandi pynwb h5py hdf5 matplotlib
pip install nwbwidgets
```

## Download data - optional
You can either stream data from DANDI archives, download the whole dataset, or download the data of a single cell. <br>
If you wish to download the whole dataset (1.4 TB) locally, please go to the desired download directory in the command line, then enter:
```
dandi download DANDI:000168
```
Please refer to (https://www.dandiarchive.org/handbook/10_using_dandi/) for more details. <br>
Alternatively, this tutorial describes how to stream the data or download the data of a single cell of interest.

