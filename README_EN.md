This repository is available in [English](README.md).

# About this repository  
This repository was used in the study session of [関西情報系学生団体交流会 (KC3)](https://kc3.me/conf/) held on September 4 and 5, 2021.  
It provides a program to run YOLOX object detection using the ONNX model created in [this repository](https://github.com/yusuke-1105/YOLOX).  

See [カスタムモデルを使用してOpenVINOで高速推論してみた(coming soon)]() for details.

# File structure  
- [OpenVINO_Bread_Detection.ipynb](OpenVINO_Bread_Detection.ipynb)  
This program detects breads in an image.  

- [AI_Bread_Register.ipynb](AI_Bread_Register.ipynb)  
A virtual register program that detects breads in an image and calculates their total price.  

- [yolox-s.onnx](yolox-s.onnx)  
ONNX model to detect the following five kind of breads.  
  > "malitozzo", "curry bread", "hot dog", "krone", "melon bread"  

# Usage  
Use Google Colab and run [OpenVINO_Bread_Detection.ipynb](OpenVINO_Bread_Detection.ipynb). The program reads images and models in the `YOLOX-s` folder of Google Drive. So, by default, you need to put `yolox-s.onnx` model and a bread image in `YOLOX-s` folder. You can change this setting as you like. In this case, change the `model_path`, `img_path`, and `output_path` in the program under `if __name__ == '__main__':`.  
You can also use [AI_Bread_Register.ipynb](AI_Bread_Register.ipynb) to execute the program as well.  


# LICENSE
These programs are released under the Apache License 2.0.  
This repository is based on [YOLOX](https://github.com/roboflow-ai/YOLOX) / [openvino_inference.py](https://github.com/roboflow-ai/YOLOX/blob/main/demo/OpenVINO/python/openvino_inference.py) by [roboflow-ai](https://github.com/roboflow-ai).   

# Acknowledgements  

This notebook is based on [the Megvii Team](https://github.com/Megvii-BaseDetection)'s [YOLOX repository](https://github.com/Megvii-BaseDetection/ YOLOX) of [the Megvii Team](https://colab.research.google.com/drive/1_xkARB35307P0-BTnqMy0flmYrfoYi5T#scrollTo=igwruhYxE_a7) and [roboflow-ai's notebook](https://colab.research.google.com/drive/1_xkARB35307P0-BTnqMy0flmYrfoYi5T#scrollTo=igwruhYxE_a7). This notebook is based on Thanks to the Megvii team for creating this repository and to roboflow-ai for creating the notebook.  

# references  
[How to Train YOLOX On a Custom Dataset](https://blog.roboflow.com/how-to-train-yolox-on-a-custom-dataset/)  