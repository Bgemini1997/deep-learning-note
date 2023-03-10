# 深度学习Pytorch(一)

前言：必须使用英伟达显卡才能使用cuda（显卡加速）！

移除环境：

```shell
conda remove -n pytorch --all
```

## 一、安装Pytorch

1. 下载Anaconda

2. 打开Anaconda Prompt

3. 创建一个Pytorch环境：

   ```shell
   conda create -n pytorch python=3.9
   ```

4. 激活Pytorch环境：

   ```shell
   conda activate pytorch
   ```

5. 查看当前包：

   ```shell
   pip list
   ```

6. 安装Pytorch

   ```shell
   conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
   ```

7. 查看torch是否安装成功

   ```shell
   python
   import torch
   torch.cuda.is_available()
   ```

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308163558.png)

   如果显示true说明torch可以使用咱们的英伟达显卡！

## 二、配置Pycharm

1. 打开Pycharm,创建新项目

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308164001.png)

   导入我们刚才创建的Pytorch环境的Python编译器

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308164051.png)

   测试是否可以导入使用conda，打开Python控制台

   ```
   import torch
   torch.cuda.is_available()
   ```

   出现True说明配置成功！

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308164909.png)

## 三、配置Jupyter

   因为最开始安装的Anaconda中的Jupyter只存在于base环境中，无法在我们新建的Pytorch环境        中使用，所以我们需要进行以下操作在新环境中安装Jupyter

   进入Pytorch环境中，需要安装一个包：

   ```shell
   conda install nb_conda
   ```

   安装完成后打开Jupyter：

   ```shell
   jupyter notebook
   ```

   打开后会弹出一个网页，使用Pytorch环境的Python新建一个代码：

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308170858.png)

   输入以下代码进行测试：

   ```python
   import torch
   torch.cuda.is_available()
   ```

   ![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308171000.png)

   输入完一行代码后，按Shift+Enter执行！出现上图说明配置成功！

## 四、Python学习中的两大法宝（也可以用在Pytorch中）

![](https://xuyuya.oss-cn-guangzhou.aliyuncs.com/img_for_typora/20230308172529.png)

以Pytorch包举例我们想了解一个包的构成和使用方法：

```
dir()   //打开，看见
help()   //说明书
比如:
dir(Pytorch)
输出：1、2、3、4

dir(Pytorch.3)
输出：a,b,c

help(Pytorch.3.a)
输出：将此扳手放在特定的地方，然后拧动
```

总结：dir()函数，能让我们知道工具箱以及工具箱中的分隔区有什么东西。

​			help()函数，能让我们知道每个工具是如何使用的，工具的使用方法。

​			具体使用help()函数时，指定到工具不加()，例如help(torch.cuda.is_available)



**更多内容请关注我的博客：[bgemini.com](https://bgemini.com/)**
