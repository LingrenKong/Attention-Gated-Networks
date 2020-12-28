# 使用与修改记录

## 2020-12-28

创建了这个fork，并且添加了本文件、run.sh（暂时只有框架）

对train文件加了一些注释，但是没有完全看懂。

尝试在 自有数据运行一下，目前进行到虚拟环境，那个torchsample不在pypi而且停更4年了……

需要的命令（setup写法需要改变了）：
PIP功能的更改可以看这个讨论：https://stackoverflow.com/questions/26061610/pip-install-dependency-links
修改setup之后，采用pip install -e .（注意那个`.`是有用的，相比原本删了`--process-dependency-links`

气死了……NormalizeMedic是不存在于torchsample的内容，这就离谱（尤其是论文指定了版本……）

发现是因为作者fork并且修正了一个版本：pip uninstall torchsample；pip install git+https://github.com/ozan-oktay/torchsample@master

但是还是有其他依赖性不在setup里面
> cv2  opencv-python
> sklearn

到此为止可以确定代码的运行不存在问题了，接下来需要处理数据。