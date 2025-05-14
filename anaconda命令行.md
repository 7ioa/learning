

1. 创建新的虚拟环境：

```
conda create --name myenv python=3.8
```

这里的`myenv`是虚拟环境的名称，`python=3.8`指定了Python的版本。

1. 激活虚拟环境：

```
conda activate myenv
```

激活名为`myenv`的虚拟环境。

1. 退出虚拟环境：

```
conda deactivate
```

1. 列出所有虚拟环境：

```
conda env list
```

```
conda info --envs
```

1. 删除虚拟环境：

```
conda env remove --name myenv
```

删除名为`myenv`的虚拟环境。

1. 克隆虚拟环境：

```
conda create --name mynewenv --clone myenv
```

将名为`myenv`的虚拟环境克隆为`mynewenv`。

1. 在虚拟环境中安装包：

```
conda install numpy
```

在当前激活的虚拟环境中安装`numpy`包。

1. 查看虚拟环境中的包：

```
conda list
```

1. 更新虚拟环境中的包：

```
conda update numpy
```

更新`numpy`包。

1. 卸载虚拟环境中的包：

```
conda remove numpy
```

