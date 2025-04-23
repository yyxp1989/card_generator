
在线抠图地址: (https://burner.bonanza.com/) (https://www.gaoding.com/koutu)

## 直接下载程序

- 身份证构造器Windows版： [idcard_generator_win64.exe](https://github.com/bzsome/idcard_generator/releases/download/v1.1.0/idcard_generator_win64_1.1.0.exe)

- 身份证构造器Macos版：[idcard_generator_macos.zip](https://github.com/bzsome/idcard_generator/releases/download/v1.1.0/idcard_generator_macos_1.1.0.zip)

- 注意：macos版本启动大约需要时间70s，测试支持系统Macos 11




## 更新记录:

- 自动改变头像大小
- 自动从纯色背景中抠图
- 随机生成身份信息(姓名，出生日期，身份证号)
- 固定依赖版本(防止高版本不兼容)
- 生成图片时显示处理弹窗

## 软件环境

- numpy
- pillow
- opencv

## 源码安装

```
pip install idcard_generator -i http://mirrors.aliyun.com/pypi/simple --trusted-host mirrors.aliyun.com
python main.py
```

## 打包程序

- 安装pyinstaller

`pip install pyinstaller`

- Mac打包(打包成Mac app)

方法一(使用venv模式需要手动指定paths)： 

`pyinstaller -i asserts/ico.icns --windowed --clean --noconfirm --onefile --add-data ./asserts:./asserts --paths /Users/chao/PycharmProjects/idcard_generator/venv/lib/python3.7/site-packages main.py`

方法二(通过pathex指定依赖模块路径)：

`pyinstaller main.spec`


- Windows打包

`pyinstaller -i asserts/ico.ico --windowed --clean --noconfirm --onefile --add-data "asserts;asserts" main.py`

- Windows打包(控制台输出日志)

`pyinstaller -i asserts/ico.ico -c --clean --noconfirm --onefile --add-data "asserts;asserts" main.py`


