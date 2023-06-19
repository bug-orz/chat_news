[TOC]

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
$ git clone https://github.com/bug-orz/chat_news.git
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

# 效果展示

头条查询 & 日期理解
---

**问题：**  
_What are the top news stories yesterday?_

**回答：**  
Searching:    yesterday

It appears that the topics of interest for yesterday include:

1. Microsoft outages and cyberattack
2. Reddit blackout
3. Elon Musk's opinions
4. BlackRock applying for a spot Bitcoin ETF
5. U.S. representative introducing bill to fire SEC's chief Gary Gensler

These topics may have been covered in the news articles you provided. However, it is important to note that the accuracy and completeness of the information in the news articles may vary.

**问题：**  
_What business news has there been in the past 7 days?_

**回答：**  
Searching:   business the past 7 days

There have been several business news articles in the past 7 days related to:

* The SEC launching two lawsuits over retail crypto trading
* A change to Facebook's algorithm causing a drop in traffic to news and media websites
* The start of Summer Game Fest and its impact on the gaming industry
* First Citizens announced job cuts after buying the US operations of another troubled lender
* Microsoft's OpenAI deal, with GPT-4-backed chatbot and generative capabilities coming to Office products

Please note that this is only a partial list and there may be other business news articles that I have not covered.

假新闻检测
---

**问题：**  
_Is it true that Donald Trump has recently been accused of a crime after June 5th?_

**回答：**  
Searching:  Trump   June 5th

Yes, it is true that Donald Trump has been indicted on seven counts in a special counsel probe into his handling of a cache of classified documents. The indictment was announced on June 10, 2021. However, it is important to note that this is a separate case from the ongoing investigations into Russian interference in the 2016 election, and whether Trump's campaign collaborated with the Russian government. It is also possible that the charges in this case are related to other matters that have not been publicly disclosed.

新闻查询
---

**问题：**  
_What recent news is there about Elon Musk?_

**回答：**  
Searching:  Musk   

There are several recent news articles about Elon Musk. Here are some of the main events:

* A shareholder lawsuit against Elon Musk has been thrown out by a judge.
* Elon Musk was scheduled to visit Tesla's Shanghai plant on Wednesday night.
* He launched his bid for the White House on Twitter, but it has been revealed that the platform has technical and political limitations.
* Elon Musk hosts an event for an anti-vaxx Democratic candidate on Twitter.

Overall, it appears that Elon Musk is involved in several different projects and events in the past few weeks.

事实问答
---

**问题：**  
_Which company recently released the Vision Pro product?_

**回答：**  
Searching:  Vision Pro   

Apple released the Vision Pro product.

# 常见问题

1. 自动下载模型或是请求API可能会遇到联网问题，请使用代理。

1. 如果GPU显存不足，推荐使用 ChatGLM-6b-int4 量化版本大模型
