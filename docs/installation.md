## Installation
The code is tested with Python3.8, Pytorch == 1.13.1, CUDA == 11.6, mmdet3d == 1.4.0, mmcv == 2.0.0, mmdet == 3.2.0 and MinkowskiEngine == 0.5.4. We recommend you to use Anaconda to make sure that all dependencies are installed correctly.

**Step 1**: Download and install Miniconda from the [official website](https://docs.conda.io/en/latest/miniconda.html).

**Step 2**: Create a new conda environment and activate it:
```bash
conda create -n os3d python=3.8
conda activate os3d
```
**Step 3**: Install PyTorch following [official instructions](https://pytorch.org/get-started/locally/), e.g.
```bash
conda install pytorch torchvision -c pytorch
```

**Step 4**: Follow [mmdetection3d](https://github.com/open-mmlab/mmdetection3d/blob/22aaa47fdb53ce1870ff92cb7e3f96ae38d17f61/docs/en/get_started.md) to install mmcv, mmdet3d and mmdet.

**Step 5**: Install MinkowskiEngine:
```bash
conda install openblas-devel -c anaconda
pip install -U git+https://github.com/NVIDIA/MinkowskiEngine -v --no-deps --install-option="--blas_include_dirs=/opt/conda/include" --install-option="--blas=openblas"
```

**Step 6**: Install SAM & FastSAM:
* Please follow [here](https://github.com/facebookresearch/segment-anything/blob/main/README.md) for installation of SAM. Then download the checkpoint for [Vit-H SAM model](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth) and put it in the folder 'data'.

* Please follow [here](https://github.com/CASIA-IVA-Lab/FastSAM/blob/main/README.md) for installation of FastSAM. Then download the checkpoint for [FastSAM](https://drive.google.com/file/d/1m1sjY4ihXBU1fZXdQ-Xdj-mDltW-2Rqv/view?usp=sharing) and put it in the folder 'data'.

**Step 7**: Install other dependencies:
```bash
pip install -r requirements.txt
```