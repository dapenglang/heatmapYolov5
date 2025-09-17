# YOLO-V5 GRADCAM

我一直想知道对象检测模型更关注对象的哪个部分。所以我搜索了一下，但没有找到Yolov5。
这是我为YOLO-v5实现的Grad cam。为了加载模型，我使用了yolov5的主代码，为了计算GradCam，我使用的是GradCam_plus_plus-pytorch存储库中的代码。


## Update:
yolov5-v6.1


## Installation
`pip install -r requirements.txt`

## Infer
`python main.py --model-path yolov5s.pt --img-path images/cat-dog.jpg --output-dir outputs`

**NOTE**: 
如果你没有任何权重，只是想测试，不要更改模型路径参数。由于yolov5的下载功能，yolov5s型号将自动下载。

**NOTE**: 有关更多输入参数，请查看main.py或运行以下命令：

```python main.py -h```

### Custom Name
要传入自定义模型，您可能还需要传入自定义名称，具体操作如下：
```
python main.py --model-path cutom-model-path.pt --img-path img-path.jpg --output-dir outputs --names obj1,obj2,obj3 
```
## Examples
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pooya-mohammadi/yolov5-gradcam/blob/master/main.ipynb)

<img src="https://raw.githubusercontent.com/pooya-mohammadi/yolov5-gradcam/master/outputs/eagle-res.jpg" alt="cat&dog" height="300" width="1200">
<img src="https://raw.githubusercontent.com/pooya-mohammadi/yolov5-gradcam/master/outputs/cat-dog-res.jpg" alt="cat&dog" height="300" width="1200">
<img src="https://raw.githubusercontent.com/pooya-mohammadi/yolov5-gradcam/master/outputs/dog-res.jpg" alt="cat&dog" height="300" width="1200">


## TO Do
1. Add GradCam++
2. Add ScoreCam
3. Add the functionality to the deep_utils library

# References
1. https://github.com/1Konny/gradcam_plus_plus-pytorch
2. https://github.com/ultralytics/yolov5
3. https://github.com/pooya-mohammadi/deep_utils

## Citation

Please cite **yolov5-gradcam** if it helps your research. You can use the following BibTeX entry:
```
@misc{deep_utils,
	title = {yolov5-gradcam},
	author = {Mohammadi Kazaj, Pooya},
	howpublished = {\url{github.com/pooya-mohammadi/yolov5-gradcam}},
	year = {2021}
}
```
