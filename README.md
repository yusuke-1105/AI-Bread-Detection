※ This repository is available in [English](README_EN.md).

# このレポジトリについて  
2021年9月4,5日に開催された[関西情報系学生団体交流会 (KC3)](https://kc3.me/conf/)の勉強会で使用したものです．  
CVATによって作成したデータセットを用いて，[このレポジトリ](https://github.com/yusuke-1105/YOLOX)でONNXモデルを作成し，それを用いることでYOLOX物体検出を実行可能にするプログラムを提供しています．  
CVATの初期設定や，自動アノテーションを行う方法に関しては[CVATの自動アノテーション機能を使ってみた](https://qiita.com/yusuke-1105/items/8375eff45054197caf96)を参照してください．  
また，モデルの学習に関しては[CVATとYOLOXで機械学習やってみた(近日公開)]()を参照してください．

# ファイル構成  
- [OpenVINO_Bread_Detection.ipynb](OpenVINO_Bread_Detection.ipynb)  
画像の中のパンを検出するためのプログラムです．  

- [AI_Bread_Register.ipynb](AI_Bread_Register.ipynb)  
画像の中のパンを検出し，それらの合計値段を計算する仮想レジプログラムです．  

- [yolox-s.onnx](yolox-s.onnx)  
以下の5種類のパンを検出するためのONNXモデルです．  
  > "malitozzo", "curry bread", "hot dog", "krone", "melon bread"  

# 使い方  
Google Colabを使用して，[OpenVINO_Bread_Detection.ipynb](OpenVINO_Bread_Detection.ipynb)を実行してください．プログラム中ではGoogle Driveの`YOLOX-s`フォルダにある画像とモデルを読み込み，それを検出します．なので，初期設定では`YOLOX-s`フォルダに`yolox-s.onnx`モデルと下記のパンの画像を入れておく必要があります．この辺りはお好きに変更してください．その際はプログラム中の`if __name__ == '__main__':`以下の`model_path`, `img_path`, `output_path` の部分を適宜変更してください．  
[AI_Bread_Register.ipynb](AI_Bread_Register.ipynb)でも同様にプログラムを実行できます．  

# ライセンス  
これらのプログラムはApache License 2.0にて公開しています．  
なお，このレポジトリは[roboflow-ai](https://github.com/roboflow-ai)さんの[YOLOX](https://github.com/roboflow-ai/YOLOX) / [openvino_inference.py](https://github.com/roboflow-ai/YOLOX/blob/main/demo/OpenVINO/python/openvino_inference.py)を参考にして作成しました．  

# 謝辞  

このノートブックは、[the Megvii Team](https://github.com/Megvii-BaseDetection)の[YOLOX repository](https://github.com/Megvii-BaseDetection/YOLOX)と[roboflow-ai's notebook](https://colab.research.google.com/drive/1_xkARB35307P0-BTnqMy0flmYrfoYi5T#scrollTo=igwruhYxE_a7)に基づいています。それらのリポジトリを作成して下さったMegviiチームと, notebookを作成して下さったroboflow-aiさんに感謝します。  

# 参照  
[How to Train YOLOX On a Custom Dataset](https://blog.roboflow.com/how-to-train-yolox-on-a-custom-dataset/)  
