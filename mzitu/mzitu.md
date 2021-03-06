## mzitu网站图片下载器

### 用法

```
.\getmzitu.py -h
命令行用法: getmzitu [-f] [-c] [-r] [-h]
                     -f 仅下载失败图集
                     -c 图集已经存在并下载完成，后续图集仍会检查或下载；当程序非正常退出时，需要加上此选项
                     -r 从最后一个图集开始下载；缺省是从第一个图集开始下载
                     -h 打印此帮助信息
```

- [getmzitu.py](getmzitu.py)，将图片保存在新建的目录images下，一个图集一个文件夹，文件夹按"图集名称_图集ID"命名
- 第一次下载，耗时比较长，全部图集总共有近20G
- 再次运行下载器程序，如碰到已下载完成的图集，程序认为下载已完成将会停止
- 如前次运行没有顺利完成，运行时需要加上-c参数，这将会检查或下载所有图集

### 运行环境要求

- python 3
- 安装了requests和BeautifulSoup
- 词云还需要jeiba、wordcloud和matplotlib

### 打包成exe独立运行

- 安装了pyinstaller
- 运行winpack.bat，生成可执行文件getmzitu.exe

### [图集描述词云图](wordcloud.py)

![MZITU网站图集描述词云词](wordcloud.png)
