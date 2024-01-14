# architecture_project

本次复现代码实验环境和硬件配置如下：

- python 3.9.7
- Ubuntu 20
- Anaconda
- pytorch 2.0.0
- cuda 11.8
- Nvidia GeForce RTX 3090



实验是在一个虚拟环境中做的，在虚拟环境中安装符合要求的python、pytorch、cuda版本：

确认pytorch版本：

```shell
python -c "import torch; print(torch.__version__)"
>>> 2.0.0
```

确保CUDA已与pytorch一起安装，版本保持兼容：

```shell
python -c "import torch; print(torch.version.cuda)"
>>> 11.8
```

运行安装脚本以得到torchsprase库：

```shell
python -c "$(curl -fsSL https://raw.githubusercontent.com/mit-han-lab/torchsparse/master/install.py)"
```

也可以从源码安装：

```shell
python setup.py install
```

在虚拟环境中输入python，启动python终端会话：

```shell
python
```

然后验证torchsparse是否已被成功安装：

```shell
>>import torchsparse
>>
```

然后逐一进行验证，复现论文工作：

```shell
python test.py
```

```shell
python example.py
```

```shell
python backbones.py
```

```shell
python performance.py
```

