---
title: IDE
date: 2020-10-15 14:38:17
tags:
---



# 背景

实现自定义语言的IDE之悬停提示，提供开发过程代码提示功能。

![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/161219/1611806740203-7e80bd7a-9dde-4104-97ae-9d995fda4fe9.png)



# 关键点

## IDE 如何进行语法提示



使用Language Server Protocol(LSP)协议，屏蔽了ide前后端交互方式，让语言服务器更专注与实现语言相关的语法分析功能。



![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/161219/1611806350105-fd380482-f418-4d5c-93b2-192e63b1cc2a.png)



## 如何定义一个新语言

### 1. 词法、语法规则



![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/161219/1611729949532-32ef2862-e450-48e9-ae86-eb14d2c0713c.png)



### 2. 语法解析器



![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/161219/1611729909547-2b0c129f-fae0-4f4b-ae4d-cb653ab5636f.png)



## 语法提示的流程



http://gitlab.alibaba-inc.com/shuaiming.jsm/gs-lsp-vscode/merge_requests/1142406/diffs?view=parallel



![image.png](https://intranetproxy.alipay.com/skylark/lark/0/2021/png/161219/1611815194401-60ea202a-178f-4f86-8f1b-8da4be14cd13.png)