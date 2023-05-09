# ApplicationScannerWin

## 介绍
​		ApplicationScannerWin为Windows平台版本的apk、ipa、so、aar、jar等库代码扫描工具，本框架仅仅为学习记录，思路来源于查看原框架**ApplicationScanner**源码后，python部分具跨平台特性和尝试把检测部分改为用win doc查询命令。使用检测命令和原框架保持一致，达到完美兼容。

**在此声明不用做任何的推广滥用。有任何疑问欢迎留言。**

**感谢原作者，奉上github链接：https://github.com/paradiseduo/ApplicationScanner**

```bash
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
* 支持 Mac、Linux、Windows 版本.

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

