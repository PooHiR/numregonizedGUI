# 基于Tensorflow的手写数字识别

## 一、项目介绍

本项目基于Tensorflow框架对是数据集进行训练与目标推理，GUI界面使用PyQt5进行编写，基本实现单个数字识别的功能，支持手写识别与导入图片识别。

mnist数据集来自keras官方库，置于根目录下datasets文件夹中。



## 二、项目部署

1、在anaconda环境下，创建新的虚拟环境

`conda create -n XXX pythton==3.7`     xxx为你想设置的环境名

2、切换至新创建的虚拟环境

`conda activate xxx`

3、根据根目录下requirements.txt文件安装对应依赖库

例：安装keras

`conda install keras=2.7.0` 或 `pip install keras=2.7.0`

注：因为本项目使用gpu加速推理 因此需要安装Nvidia Cuda Toolkit，该开发者工具版本因个人机器而异，

Tensorflow也对应不同版本，请注意！

若没有gpu，可以使用tensorflow cpu版，但相应源码需要进行一些变动，不然会导致无法运行

例：GUi.py中

`config = tf.compat.v1.ConfigProto(allow_soft_placement=True)`

应改为 `config = tf.ConfigProto(allow_soft_placement=True)`



## 三、项目运行

方法一：用pycharm打开本项目，解释器设置为你的conda虚拟环境，直接运行即可

方法二：在conda命令窗口切换到对应环境后，进入项目目录

​                执行 `python GUI.py`



## 四、项目展示

![image](https://github.com/PooHiR/numregonizedGUI/blob/main/main.png)

![image](https://github.com/PooHiR/numregonizedGUI/blob/main/1.png)

![image](https://github.com/PooHiR/numregonizedGUI/blob/main/2.png)



## 五、项目部署可能发生的问题

若在项目进行推理时，报错提示找不到zlibwapi，请将根目录中.dll文件放入你的CUDA\bin目录下，.lib文件放入CUDA\lib目录下。



