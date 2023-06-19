# ChatNews 本地实时的新闻问答助手

# 项目介绍

此项目使用本地部署的大模型 ChatGLM-6b 和 newsapi.org 新闻API，实现了一个新闻版New Bing

<br>

# 支持功能

- 新闻头条查询
- 假新闻检测
- 事实问答
- 支持识别特定的人们、组织、地名
- 支持日期理解

<br>

# 使用教程

## 下载项目

下载项目

```bash
$ git clone https://github.com/wanhebin/clash-for-linux.git
```

## 安装

为了运行此代码，你需要安装一些Python包。你可以使用`pip`来安装这些依赖：

```bash
 pip install transformers paddlenlp sentence-transformers
```

### 获取 API Key

可以进入 [newsapi.org](https://newsapi.org/account) 获取自己的key

进入到项目目录，编辑`chat_news.ipynb`文件，修改变量`CLASH_URL`的值。

<br>

# 常见问题

1. 自动下载模型或是请求API可能会遇到联网问题，请使用代理。

1. 如果GPU显存不足，推荐使用 ChatGLM-6b-int4 量化版本大模型
