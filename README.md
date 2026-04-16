# SAM3 on VOC2012

This repository experiments with **SAM 3** (Segment Anything Model 3) on the **PASCAL VOC 2012** dataset. The code is based on Meta's official repository: [facebookresearch/sam3](https://github.com/facebookresearch/sam3).

## How to Run

### Step 1: Download SAM 3 Model Weights
1. Visit the SAM 3 model page on Hugging Face and **request access**:
   - [https://huggingface.co/facebook/sam3](https://huggingface.co/facebook/sam3)
2. Once approved, download the `sam3.pt` file.

### Step 2: Download VOC2012 Dataset
Download the dataset from:  
[http://host.robots.ox.ac.uk/pascal/VOC/voc2012/index.html#devkit](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/index.html#devkit)

- Download **VOCtrainval_11-May-2012.tar** known as **Download the training/validation data (2GB tar file) at Development Kit**
- Extract it into the project directory

### Step 3: Prepare Files
Place the following in the root directory of the project (same level as the notebooks):
- The extracted VOC2012 folder
- The model weight file `sam3.pt`

## Notebooks

| Notebook                        | Description                                                                 | 
|--------------------------------|-----------------------------------------------------------------------------|
| `test_all_local.ipynb`         | Test SAM3 on local machine                                                   | 
| `sam3-not-resize.ipynb`        | Run SAM3 without image resizing on kaggle                                    |
| `visual_bbox_5class.ipynb`     | Visualize bounding boxes of 5 weak classes: `diningtable`, `sofa`, `chair`, `bicycle`, `pottedplant` |
| `sam3-improve-5first.ipynb`    | Attempt to improve segmentation results for the 5 weak classes (still in progress) |

**Note**:  
The classes `diningtable`, `sofa`, `chair`, `bicycle`, and `pottedplant` are currently the weakest performing classes for SAM3. The notebook `sam3-improve-5first.ipynb` is where experiments to improve segmentation quality for these classes are being conducted.

