# vCertification

## 基于沙箱实验室的微认证系统

A microCertification system based on sandbox lab for java.

### 主要特性 FEATURES

* 1.通过K8s/Docker/云底座提供沙箱环境，以cmdb插件定制环境

  Provide sandbox lab for java with K8s / Docker / Cloud vm. The environment settings from cmdb plugin.

* 2.沙箱实验室通过断言的方式，对实验步骤提供自动化检测能力，包括以下类型（不断丰富）：

  Sandbox Lab provide automatic check capacities, including:

    * 配置文件检查

      Check prop files

    * 接口响应断言

      Assert interface imp response

    * 交易性能检测

      Assert performance tuning

    * sql优化检测

      Assert sql explain plan tuning

    * linux基本操作如vi等

      Assert basic linux operations like vi/touch

    * 系统配置变更设置

      Assert system configuration applied

    * POC环境部署等能力

      Assert poc env systems deployed

* 4.提供web ssh访问沙箱，一站式支持，不需众多工具

  Provide web ssh to sandbox lab, all in one env, no additional tools.

* 5.实验模式提供实验手册，逐步骤引导

  Lab mode provide Laboratory manual, guid user step by step.

* 6.认证模式提供自动识别，完成进度同步进认证体系

  Certification mode provide auto assert to verify every step completed, and update progress in certification database for everyone.

* 7.支持企业级能力，提供多租户环境，使能学习型组织的个性定制需求

### 系统特性1.沙箱实验室

Feautre1. Sandbox Lab

<img width="416" alt="image" src="https://user-images.githubusercontent.com/94591164/142356421-bfb5c538-cbb7-45e0-9186-f943be1a58d1.png">

沙箱实验室通过容器化平台，生成真实环境，提供云端真实的实践、测试、验证； Sandbox lab provide real cloud env for practice / verification / testes, mainly base on container system.

<img width="1018" alt="image" src="https://user-images.githubusercontent.com/94591164/142356522-1f83dc68-7307-4bae-8aeb-fce0e3e1e975.png">

沙箱实验室以实验组装的方式来提供接近真实的环境，按加载顺序会有以下组件：

Sandbox lab assemble lab to supply simulated env.

* 1.环境管理器。（CMDB扩展）提供环境配置，如基础应用开发环境提供APP+DB，如SQL优化环境提供一组DB Cluster，如Spring Cloud体系实验提供Nginx负载+GW+Nacos+Apollo+APP+DB的模板；
* 2.实验手册库。由一堆基础步骤组成，如部署tomcat，如部署redis，如部署应用开发框架，如初始化数据库，如编写后台交易，如启动应用开发框架等；
* 3.实验步骤断言。校验部分是沙箱自动化运行的重要实现，检验能力+配置--->实验步骤断言，这些断言可以用来检测每个实验的步骤执行情况；
* 4.实验组装平台。实验是整个沙箱的价值所在，系统提供低代码方式的实验组装平台，从环境管理器、实验手册库、实验步骤断言中抽取能力，组装成实验直接上架到微认证体系；

