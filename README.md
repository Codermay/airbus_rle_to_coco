## COCO数据集制作
本代码是针对Kaggle比赛 [Airbus Ship Detection Challenge](https://www.kaggle.com/c/airbus-ship-detection) 制作的RLE-->COCO 数据集转换工具;

主要有以下几个功能：

1. 数据集中存在大量的负样本，将其删除，只保留存在实例的图片

2. airbus提供的数据是RLE格式的，将其转化为COCO数据集格式，得到标准的.json标注文件

## 文件结构

    airbus_dataset
    ├─input
    │  ├─annotations            # 标注文件
    │  └─ships_train2018        # 图片
    ├─src                       # 本代码所在文件夹
    │  └─ xxx.py                # 可执行脚本
    └─tmp                       # 中间文件夹


## 安装步骤

1、安装pycocotool

    git clone https://github.com/waleedka/coco
    cd coco/PythonAPI
    make
    python setup.py install

2、安装pycococreator

下面给出的安装命令不一定是最新的，使用时可参考[项目Github](https://github.com/waspinator/pycococreator)


    pip install git+git://github.com/waspinator/pycococreator.git@0.2.0

3、安装pandas

    pip install pandas
