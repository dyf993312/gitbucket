云谷学堂 Spring Cloud 配置
===============

# 一、配置说明

## 1、application.yml

所有系统都需要的统一配置，某个系统的特殊参数配置到`{project-name}.yml`文件中。

## 2、application-base.yml

基础数据的配置信息，现在主要配置了年级、学段、学科等。

## 3、gateway.yml

网关的配置信息。

## 4、apidoc.yml

SwaggerUI的配置信息。

## 5、{project-name}.yml

项目的特殊配置。

# 二、如何增加一个项目

例如增加了一个名称为`example`的项目。

## 1、增加配置文件example.yml

端口号请参考下面的项目列表，按顺增加。

```
server:
  port: 60xx
management:
  server:
    port: 70xx
```

## 2、配置gateway.yml

```
zuul:
  routes:
    example-route:
      path: /example/**
      serviceId: example
```

## 3、配置apidoc.yml

```
ygxt:
  swagger2:
    modules:
      - code: example
        name: 演示系统
```

# 附：项目列表

|Name       |Http Port |Management|
|:----------|:---------|:---------|
|Base       |6001      |7001      |
|User       |6002      |7002      |
|Klass      |6003      |7003      |
|CourseSch  |6004      |7004      |
|Note       |6005      |7005      |
|Mall       |6006      |7006      |
|Work       |6007      |7007      |
|Diag       |6008      |7008      |
|Category   |6009      |7009      |
|Repository |6010      |7010      |
|File       |6011      |7011      |
|Media      |6012      |7012      |
|Message    |6013      |7013      |
|Lesson     |6014      |7014      |
|Wrongwork  |6015      |7015      |
|Record     |6016      |7016      |
|Chat       |6017      |7017      |
|Notice     |6018      |7018      |
|Incentive  |6019      |7019      |
|Diag-lesson|6020      |7020      |
|Diag-period|6021      |7021      |
|Learn      |6022      |7022      |
|Home       |6023      |7023      |
|Exam       |6024      |7024      |
|Word       |6025      |7025      |
|Reading    |6026      |7026      |
|Diag-screen|6027      |7027      |
|Preconception|6028      |7028      |
|React      |6029      |7029      |
|voice      |6030      |7030      |
|Home-Edu      |6031      |7031      |
|Financial  |6032      |7032      |
