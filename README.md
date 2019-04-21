# JHipster 服务注册中心

[![Build Status][travis-image]][travis-url]  [![Docker Pulls](./src/main/resources/static/eureka/images/docker-pull.svg)](https://hub.docker.com/r/jhipster/jhipster-registry/)

这是基于[Spring Cloud Netflix](http://cloud.spring.io/spring-cloud-netflix/)、[Eureka](https://github.com/Netflix/eureka)和[Spring Cloud Config](http://cloud.spring.io/spring-cloud-config/)的[JHipster](https://www.jhipster.tech/)注册服务。

完整的文档可以在[JHipster文档](https://www.jhipster.tech/microservices-architecture)中找到。

## 在Heroku上部署

单击此按钮可部署您自己的服务注册中心实例:

[![Deploy to Heroku](./src/main/resources/static/eureka/images/depoloy-to-heroku.png)](https://heroku.com/deploy)

在部署到Heroku时存在一些限制。

* 服务注册中心将只与[本机配置](https://www.jhipster.tech/jhipster-registry/#spring-cloud-config)(而不是Git配置)一起工作。
* 服务注册中心不能扩展到多个dynos实现高可用。您必须部署多个应用程序(即多次单击按钮)。这是因为Eureka需要不同的url来同步实例之间的内存状态。

## 在本地运行

在源代码当前目录下运行;
* 开发环境下运行`./mvnw -Pdev,webpack`或 `./mvnw`仅仅是启动后端代码，运行`yarn && yarn start`将热启动客户端代码。
* 通过执行`./mvnw -Pprod`在生产环境下运行

[travis-image]: ./src/main/resources/static/eureka/images/build-passing.svg?branch=master
[travis-url]: https://travis-ci.org/jhipster/jhipster-registry
