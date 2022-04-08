---
title: 友链
layout: page
date: 2022-04-04 00:12:40
---

> 晚安啊

```graph
sequenceDiagram
Title: md时序图练习

    participant 客户端
    participant 控制器
    participant 业务
    participant 数据库

     客户端->>数据库:提交数据店铺
     Note right of 客户端:提交数据进行验证
     控制器->>控制器:验证数据完整性
     Note left of 控制器:返回错误的字段信息
     控制器-->>客户端:数据不完整
     Note over 客户端: 用户输入通行证的账号、密码
     控制器->>业务:保存店铺到数据库
     业务->>业务:save店铺数据
     业务-->>控制器:保存出现异常
     控制器-->>客户端:保存成功
     数据库-->>业务:success
     业务-->>控制器:success
     控制器-->>客户端:success 客户端
     Note left of 控制器:返回正确的提示，并跳转到审核第二步
```
