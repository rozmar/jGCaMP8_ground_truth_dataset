# How to download and use the jGCaMP8 mouse ground truth dataset

## To install the dependencies for this notebook, type in terminal or anaconda prompt:
```
conda create --name GCaMP8Mouse dandi pynwb h5py hdf5 matplotlib python=3.8 --channel=conda-forge
conda activate GCaMP8Mouse
pip install nwbwidgets jupyterlab
```
## To download and start the script:
```
git clone https://github.com/rozmar/jGCaMP8_ground_truth_dataset.git
cd jGCaMP8_ground_truth_dataset
jupyter-notebook NWB_tutorial.ipynb
```
(Alternatively, just download the NWB_tutorial.ipynb instead of the first two lines.)
## The data is in the following DANDIset:
https://dandiarchive.org/dandiset/000168/

## Please read the paper for additional information:
https://doi.org/10.1101/2021.11.08.467793 

# Dataset description

This dataset contains simultaneous 2-photon calcium imaging movies and loose-seal cell attached recordings of upper layer 2 pyramidal cells and interneurons of the primary visual cortex of wild type mouse, in vivo, during drifting gratings stimulus in the contralateral eye.
jGCaMP8f, jGCaMP8m, jGCaMP8s, jGCaMP7f and XCaMPgf were expressed via AAV injections using synapsin-1 promoter.

Multiple neurons were recorded in each mouse, and multiple ~3-minutes-long recordings (movies&sweeps) were performed for each cell. One .nwb file contains all the data for a given cell. 

The dataset contains:
- motion corrected 2-photon movies
- raw cell attached loose-seal electrophysiology traces of a single neuron in the imaging field of view
- somatic cellular and neuropil ROIs that were segmented with Suite2p
- the fluorescence traces for all ROIs
- details of the drifting gratings stimuli presented to the contralateral eye


## Download data - optional
You can either stream data from DANDI archives, download the whole dataset, or download the data of a single cell. <br>
If you wish to download the whole dataset (1.4 TB) locally, please go to the desired download directory in the command line, then enter:
```
dandi download DANDI:000168
```
Please refer to (https://www.dandiarchive.org/handbook/10_using_dandi/) for more details. <br>
Alternatively, this tutorial describes how to stream the data or download the data of a single cell of interest.

