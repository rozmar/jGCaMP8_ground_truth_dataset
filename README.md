# jGCaMP8_mouse_cell_attached_pipeline

## The data generated with this pipeline is in the following DANDIset:
https://dandiarchive.org/dandiset/000168/

## Please read the paper for additional information:
https://doi.org/10.1101/2021.11.08.467793 

## Please see the following notebook on how to use the dataset:
https://github.com/rozmar/jGCaMP8_mouse_cell_attached_pipeline/blob/master/NWB_tutorial.ipynb

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

## Dependencies 
python >=3.7 <br>
jupyter-notebook - for running this example<br>
dandi - for downloading data<br>
pynwb - for opening nwb files<br>
h5py hdf5 - for streaming nwb files directly from DANDI Archives <br>
matplotlib - plotting <br>
#### To install, type:
```
conda create --name GCaMP8Mouse python=3.7
conda activate GCaMP8Mouse
conda install --channel=conda-forge jupyter dandi pynwb h5py hdf5 matplotlib
```
### Additional packages
nwbwidgets - for browsing .nwb files:<br>
#### To install, type:
```
pip install nwbwidgets
```

## Download data
You can either stream data from DANDI archives, download the whole dataset, or download the data of a single cell. <br>
If you wish to download the whole dataset (1.4 TB) locally, please go to the desired download directory in the command line, then enter:
```
dandi download DANDI:000168
```
Please refer to (https://www.dandiarchive.org/handbook/10_using_dandi/) for more details. <br>
Alternatively, [this tutorial](https://github.com/rozmar/jGCaMP8_mouse_cell_attached_pipeline/blob/master/NWB_tutorial.ipynb) describes below how to stream the data or download the data of a single cell of interest.

