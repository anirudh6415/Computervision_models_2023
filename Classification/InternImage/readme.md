# InternImage Unoffical Implementation for Image Classification
This is an unoffical implementation of Internimage  for just classification. You can also change it as backbone for Segementation/Detection by using __forward_features_seq_out__

### Please the offical implementation 
[InternImage](https://github.com/OpenGVLab/InternImage.git)

## Example Usage

### Install

- Clone this repo:
```bash
git clone https://github.com/anirudh6415/CV_model2023.git
cd MLClassification/InternImage
```

- Create a conda virtual environment and activate it:

```bash
conda create -n internimage python=3.7 -y
conda activate internimage
```

For examples, to install torch==1.11 with CUDA==11.3:
```bash
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113  -f https://download.pytorch.org/whl/torch_stable.html
```

- Install `timm`
```bash
pip install timm==0.6.11
```
- Compiling CUDA operators
```bash
cd ./ops_dcnv3
sh ./make.sh
# unit test (should see all checking is True)
python test.py
```

- You can also install the operator using .whl files
[DCNv3-1.0-whl](https://github.com/OpenGVLab/InternImage/releases/tag/whl_files)

### Example Usange 
```Python
from intern_image import main
model = main(model_name="InternImage_T")
```


## Citations

If this work is helpful for your research, please consider citing the following BibTeX entry.

```bibtex
@article{wang2022internimage,
  title={InternImage: Exploring Large-Scale Vision Foundation Models with Deformable Convolutions},
  author={Wang, Wenhai and Dai, Jifeng and Chen, Zhe and Huang, Zhenhang and Li, Zhiqi and Zhu, Xizhou and Hu, Xiaowei and Lu, Tong and Lu, Lewei and Li, Hongsheng and others},
  journal={arXiv preprint arXiv:2211.05778},
  year={2022}
}
```
