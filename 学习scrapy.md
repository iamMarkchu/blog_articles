![](http://qiniu.mcgoldfish.com/image/1/oyr2vIINTnK5ZZykUIaffzQYGk4oLuZ5Zf3epHKG.png )



> Scrapy是一个用于抓取网站并提取可用于广泛的有用应用程序的结构化数据的框架，广泛应用于如据挖掘，信息处理等场景中 



[TOC]

## 1. 介绍 **Scrapy**

### 运作流程图





![](http://qiniu.mcgoldfish.com/image/1/MtMV070a5cY13NlaCekqTqB7Bqd7nZmlJDYA83Qs.png)



## 2. 安装，初始化 **Scrapy**

### 安装

``` bash
pip3 install Scrapy    ## 通过python3的管理工具 pip3安装
```



### 创建一个scrapy项目

``` bash
scrapy startproject scrapy_demo
```



> 创建的scrapy项目的目录结构

``` 
.
├── scrapy.cfg                # 配置文件
└── scrapy_demo
    ├── __init__.py
    ├── items.py			 # item定义文件, 相当于model
    ├── middlewares.py        # 中间件定义文件
    ├── pipelines.py          # 管道定义文件  
    ├── __pycache__
    ├── settings.py           # 配置文件
    └── spiders               # 爬虫文件夹
        ├── __init__.py
        └── __pycache__
```



## 3. **Scrapy** 组件介绍

## 4. 通过一个demo了解 **Scrapy**