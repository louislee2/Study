# Study
just resolve some questions
# 步骤

## 1.配置环境

- conda create -n DeepONet
- conda activate DeepONet
- 将安装位置切换到虚拟环境中
- 下载python3.9.18
- conda install python=3.9.18 -c https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/

![](https://github.com/louislee2/Study/blob/main/images/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-02-24%20091016.png)

- 打开pycharm配置解释器
- 安装pytorch  pip install torch torchvision torchaudio -i https://pypi.tuna.tsinghua.edu.cn/simple --index-url https://download.pytorch.org/whl/cpu 一般来说问下ai就行了，看官方文档的是看gpu版本的是否兼容。（pyhtorch的兼容性比较好，这里可以直接用pip指令，但是tesnorflow一定要指定版本）

- 下载requirements里面的包，我看了下里面没有指定版本，而且sklearn现在是scikit-learn包库。（**这里只是包的名字变了，用法没有变，pycharm提示没有sklearn直接忽略就行了）**还是一个一个下吧。用conda指令或者pip指令都可以。
- 先下载tensorflow,用到了deepxde包，一般下载tensorflow2.x，这里使用pip install tensorflow==2.15.0 -i https://pypi.tuna.tsinghua.edu.cn/simple （这里为什么先下载tensorflow的原因是其他的包要与该tesnorflow版本兼容，使用deepxde任意选择一个后端就行了，这里下载tesorflow是因为代码里面用到了）
- 下载deepxde包，看readme对应的版本 ：pip install deepxde==0.11.2
- 下载剩下其他的包

## 2.注意事项

- 你昨晚运行的seq2seq_main.py中的代码要进行改动，它默认的是**gpu**运行，改成**cpu**。

![](https://github.com/louislee2/Study/blob/main/images/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-02-24%20095759.png)

运行结果为：

![](https://github.com/louislee2/Study/blob/main/images/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-02-24%20100031.png)

- 红色的地方是我自己的原因（numpy下载了两次）对结果不影响。使用**crtl+c**终止训练。cpu训练有点慢。。。
- 一定要注意它的代码部分，有些是默认gpu运行的，要改成cpu,一般代码都会有注释。
- 要根据readme.tx的指示来下载。
- 用 powershell prompt或者pycharm的终端都可以。
- 昨晚的报错很像是pytorch的包损坏了，所以使用国内的镜像源好些，但是有些包还是下载比较慢的，所以等等，不要着急。
- 有什么问题联系我。
