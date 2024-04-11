## anaconda 相关
### 下载安装

anaconda清华大学开源软件镜像站[地址](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/ )

安装时记得选取添加环境变量

验证：

````
conda --version 
conda info
````

配置conda下载源：[清华](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/) 目前用不了，不知道以后能不能用

配置 pip 下载源：[阿里云](https://developer.aliyun.com/mirror/pypi)

````
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/
````

常见命令

````cmd
#更新
conda update conda
conda update anaconda
conda update --all

#创建环境
conda create -n py38 python=3.8
#删除环境
conda remove --name 环境名称 --all
#激活环境
conda activate py38
#查看环境列表
conda env list
conda info --envs
#安装包
conda install 包名称
#更新包
conda update 包名称
#删除包
conda remove 包名称
````



### 安装cuda

先在cmd输入 ``nvidia-smi`` 查看最高可支持的版本

然后去[官网](https://developer.nvidia.com/cuda-toolkit-archive)下载对应的版本

### 安装 torch

去[官网](https://download.pytorch.org/whl/torch_stable.html) 下载对应的版本，然后使用以下命令安装，注意cu111代表cuda版本为11.1，cp38代表python版本为3.8

````cmd
pip install torch-1.10.0+cu111-cp38-cp38-win_amd64.whl
````

### 安装cudnn

前往[官网](https://developer.nvidia.com/cudnn-downloads)下载对应安装包，直接复制到cuda安装目录

## jupyter notebook 配置

