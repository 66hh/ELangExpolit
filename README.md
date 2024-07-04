# ELangExpolit
 易语言支持库自动加载漏洞,此漏洞为本人发现的原创漏洞,因吴涛大概率不会修复(那么多年没更新了)故此直接发布,希望各位提高警惕

# 漏洞原理
 易语言检测到源代码缺失支持库会自动寻找当前目录下是否有缺失的支持库,有支持库就会自动加载,这时候在支持库的dllmain里动手脚就能直接远控

# 修复方法
 Hook LoadLibrary 先对fne, fnl文件进行扫描确定是否是官方支持库或lib中的支持库后再进行装载,发现是源代码目录下的支持库后弹窗提醒是否加载

# 截图
 ![img.png](img/img.png)

# 感谢
 POC改造自
 https://github.com/aiqinxuancai/EasyFne
