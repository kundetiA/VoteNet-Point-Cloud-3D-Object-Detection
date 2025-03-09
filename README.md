# VoteNet 3D Object Detection on SUNRGBD Point Cloud Dataset in Colab Notebook

This notebook provides a comprehensive guide for setting up **VoteNet** for 3D object detection using the **SUNRGBD Point Cloud Dataset**. The following steps are covered:

### Important Steps covered:
- **Setting up the virtual environment** with an older Python version in a Colab notebook.
- **Compiling CUDA/C++ extensions** for **PointNet2**, which is used as the backbone for **VoteNet**.
- **Training VoteNet** with the **SUNRGBD Dataset**.

---

### Prepare the Training and Validation Dataset:

Please follow these steps to correctly set up the dataset for training.

#### 1. Clone the GitHub repository to your local machine:
```bash
git clone https://github.com/YOUR_USERNAME/VoteNet.git
```

#### 2. Download the SUNRGBD Dataset:
You can download the dataset from [SUNRGBD dataset](https://rgbd.cs.princeton.edu/data/).

Download the following files:
- **SUNRGBD.zip**
- **SUNRGBDMeta2DBB_v2.mat**
- **SUNRGBDMeta3DBB_v2.mat**
- **SUNRGBDtoolbox.zip**

#### 3. Move and unzip the files:
Move all the downloaded files into the **OFFICIAL_SUNRGBD** folder inside the cloned **VoteNet** repository. Then, unzip the files.

#### 4. Extract Point Clouds and Annotations:
Open **MATLAB** and navigate to the **VoteNet repository** folder. Run the following scripts to extract point clouds and annotations (class, 2D bounding boxes, 3D bounding boxes):
- `extract_split.m`
- `extract_rgbd_data_v2.m`
- `extract_rgbd_data_v1.m`

These scripts are located inside the `matlab` folder of the **VoteNet** repository.

#### 5. Prepare the Dataset:
Run the following Python script to generate the **train** and **validation** folders:
```bash
python sunrgbd_data.py --gen_v1_data
```

This will prepare the dataset for training.

#### 6. Training Data is Ready:
After completing the steps above, your **train** and **test** datasets will be ready for use in training VoteNet.

---

### Getting Started:

To start training the model, follow the instructions inside the notebook and make sure you have successfully set up the **virtual environment** and compiled the necessary **PointNet2** extensions.

Good luck with your 3D object detection task! 
