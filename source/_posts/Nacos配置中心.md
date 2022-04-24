---
title: Nacos配置中心
date: 2022-04-2 22:51:12
tags: 
---
随手先来一个bootstrap配置文件（properties或者yml都可）
```java
server.port=80
spring.application.name=applicationName

# Nacos作为配置注册中心的地址，以及配置文件的类型
spring.cloud.nacos.config.server-addr=42.192.51.93:8848
spring.cloud.nacos.config.file-extension=properties
# 选择Nacos配置注册中心上的配置文件分组，默认使用DEFAULT_GROUP
# spring.cloud.nacos.config.group=
# 选择Nacos配置注册中心上的配置文件的命名空间，默认使用public
# spring.cloud.nacos.config.namespace=
# Data ID ${spring.application.name}-${spring.profile.active}.${spring.cloud.nacos.config.file-extension}
# Nacos作为服务注册中心的地址
spring.cloud.nacos.discovery.server-addr=42.192.51.93:8848
```
namespace、group、dataid三者的关系是`namespace`包含`group`包含`dataid`；
主要起到的是环境隔离的效果。

注意！！！
在SpringCloud 2020.0.0 版本之后，bootstrap.yml将不会被自动加载了（咱也不知道为什么，出于什么情况下的考虑。好好的自动加载配置文件就不自动了）
需要手动引入依赖

```xml
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-bootstrap</artifactId>
</dependency>
```
