[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-FF6C00?style=for-the-badge&logo=langchain&logoColor=white)](https://github.com/langchain-ai/langchain)
[![LangGraph](https://img.shields.io/badge/LangGraph-00324d?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4NS4zMzMiIGhlaWdodD0iODUuMzMzIiB2ZXJzaW9uPSIxLjAiIHZpZXdCb3g9IjAgMCA2NCA2NCI+PHBhdGggZD0iTTEzIDcuOGMtNi4zIDMuMS03LjEgNi4zLTYuOCAyNS43LjQgMjQuNi4zIDI0LjUgMjUuOSAyNC41QzU3LjUgNTggNTggNTcuNSA1OCAzMi4zIDU4IDcuMyA1Ni43IDYgMzIgNmMtMTIuOCAwLTE2LjEuMy0xOSAxLjhtMzcuNiAxNi42YzIuOCAyLjggMy40IDQuMiAzLjQgNy42cy0uNiA0LjgtMy40IDcuNkw0Ny4yIDQzSDE2LjhsLTMuNC0zLjRjLTQuOC00LjgtNC44LTEwLjQgMC0xNS4ybDMuNC0zLjRoMzAuNHoiLz48cGF0aCBkPSJNMTguOSAyNS42Yy0xLjEgMS4zLTEgMS43LjQgMi41LjkuNiAxLjcgMS44IDEuNyAyLjcgMCAxIC43IDIuOCAxLjYgNC4xIDEuNCAxLjkgMS40IDIuNS4zIDMuMi0xIC42LS42LjkgMS40LjkgMS41IDAgMi43LS41IDIuNy0xIDAtLjYgMS4xLS44IDIuNi0uNGwyLjYuNy0xLjgtMi45Yy01LjktOS4zLTkuNC0xMi4zLTExLjUtOS44TTM5IDI2YzAgMS4xLS45IDIuNS0yIDMuMi0yLjQgMS41LTIuNiAzLjQtLjUgNC4yLjguMyAyIDEuNyAyLjUgMy4xLjYgMS41IDEuNCAyLjMgMiAyIDEuNS0uOSAxLjItMy41LS40LTMuNS0yLjEgMC0yLjgtMi44LS44LTMuMyAxLjYtLjQgMS42LS41IDAtLjYtMS4xLS4xLTEuNS0uNi0xLjItMS42LjctMS43IDMuMy0yLjEgMy41LS41LjEuNS4yIDEuNi4zIDIuMiAwIC43LjkgMS40IDEuOSAxLjYgMi4xLjQgMi4zLTIuMy4yLTMuMi0uOC0uMy0yLTEuNy0yLjUtMy4xLTEuMS0zLTMtMy4zLTMtLjUiLz48L3N2Zz4=&logoColor=white)](https://github.com/langchain-ai/langgraph)


# 我的LangGraph聊天机器人

这是我之前做的一个小项目，主要是用LangGraph实现了一个简单的聊天机器人。它能够记住之前的对话内容，这样聊天就能保持连贯性了。

我把核心代码放在了src/agent/graph.py里，还算比较简单明了。基本上就是接收用户消息，然后根据历史记录生成回复。

## 这个机器人能做什么

简单来说就是：

- 接收用户消息
- 记住我们的对话历史
- 根据上下文生成回复
- 把新的对话加入历史记录中

代码结构很简单，我觉得以后要是想加功能也挺方便的。

## 如何运行

前提是你已经装了LangGraph Studio，然后：

1. 复制个.env文件
2. 把需要的API密钥填进去
3. 按需修改一下代码
4. 用LangGraph Studio打开就可以了

## 我的自定义部分

如果你想改动的话，主要有这几个地方：

1. 系统提示词在configuration.py里，可以改一下让机器人有不同的性格
2. 默认用的是Claude 3 Sonnet，不过也可以换成别的，比如gpt-4什么的
3. 如果想改对话流程，就去修改graph.py

我还想过以后可以加些功能，比如：

- 加点自定义工具让它能做更多事
- 加点逻辑处理特定的问题
- 可能再接入一些外部API