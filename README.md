# ApplicationScannerWin

## 介绍
​		ApplicationScannerWin为Windows平台版本的apk、ipa、so、aar、jar等库代码扫描工具，本框架仅仅为学习记录，思路来源于查看原框架**ApplicationScanner**源码后，python部分具跨平台特性和尝试把检测部分改为用win doc查询命令。使用检测命令原理和原框架基本保持一致，达到完美兼容。

**在此声明不用做任何的推广滥用。欢迎各位大佬们留言issues**

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

* 确保在电脑上已经安装了 python3.8+ 和 Java 11.

* 安装打印美化 js-beautify（可选）

```bash
npm -g install js-beautify
```

## 使用
```bash
> git clone https://github.com/zqf-dev/ApplicationScannerWin.git
> cd ApplicationScannerWin
> pip install -r requirements.txt
> python AppScanner.py -i xxx.apk
```
## 扫描结果保存

```bash
python AppScanner.py -i xxx.apk > result.txt
```

## 扫描SDK

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

## 案例

- **部分截图如下**

![](./images/1.jpg)

![](./images/2.jpg)

![](./images/3.jpg)

![](./images/4.jpg)

![](./images/6.jpg)

![](./images/2.jpg)

## 计划

进一步完善在一些复杂app上出现的问题如：

- FINDSTR: 搜索字符串太长、找不到文件 - '*.js'等情况
- ...
- ...

## License

This software is released under the GPL-3.0 license.

