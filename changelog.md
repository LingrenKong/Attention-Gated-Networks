# 使用与修改记录

## 2020-12-28

创建了这个fork，并且添加了本文件、run.sh（暂时只有框架）

对train文件加了一些注释，但是没有完全看懂。

尝试在 自有数据运行一下，目前进行到虚拟环境，那个torchsample不在pypi而且停更4年了……

需要的命令（setup写法需要改变了）：
PIP功能的更改可以看这个讨论：https://stackoverflow.com/questions/26061610/pip-install-dependency-links
修改setup之后，采用pip install -e .（注意那个`.`是有用的，相比原本删了`--process-dependency-links`

气死了……NormalizeMedic是不存在于torchsample的内容，这就离谱（尤其是论文指定了版本……）