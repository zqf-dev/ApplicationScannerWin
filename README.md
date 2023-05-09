# ApplicationScannerWin

## 介绍
ApplicationScannerWin为Windows平台版本的App代码扫描工具，原框架只能支持Mac / Linux环境。本框架仅仅为学习记录，思路来源于查看源码后，python部分的跨平台和将检测部分改为用win doc命令，在此声明不用做任何的推广滥用。有任何疑问欢迎留言。

再次感谢原作者，奉上链接：

原作者框架github：https://github.com/paradiseduo/ApplicationScanner

```bash

                      _____
    /\               / ____|
   /  \   _ __  _ __| (___   ___ __ _ _ __  _ __   ___ _ __
  / /\ \ | '_ \| '_ \___ \ / __/ _` | '_ \| '_ \ / _ \ '__|
 / ____ \| |_) | |_) |___) | (_| (_| | | | | | | |  __/ |
/_/    \_\ .__/| .__/_____/ \___\__,_|_| |_|_| |_|\___|_|
         | |   | |
         |_|   |_|

                             ParadiseDuo  [2.4]

    Usage:
        python3 AppScanner.py -i *.apk/*.ipa/*.aab

        -h help
        -i <inputPath>
        -s save cache (Default clear cache)
        -l language ['zh', 'en'] (Default zh)
        -f <CheckList Path>
```
## 要求
* 仅支持 Windows 版本.

* 确保在电脑上已经安装了 python3.x 和 Java 11.

* 安装打印美化 js-beautify

	```bash
	npm -g install js-beautify
	```

## 使用
```bash
> git clone https://github.com/paradiseduo/ApplicationScanner.git
> cd ApplicationScanner
> pip install -r requirements.txt
> python3 AppScanner.py -i xxx.apk
```
### 扫描SDK
支持扫描.framework/.a/.so/.aar/.jar file
```bash
> python3 AppScanner.py -i test.framework -f checklist
```
检测列表是一个文本文件，如下所示(支持扫描中文):

```bash
dlsym
dlopen
respondsToSelector
performSelector
method_exchangeImplementations
支付宝
微信
```

## License

This software is released under the GPL-3.0 license.

