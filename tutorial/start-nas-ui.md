# 快速体验start-nas-ui

欢迎您使用Serverless Devs开发者工具进行项目开发，本实验是基于Serverless Devs部署start-nas-uis案例到阿里云函数计算, 实现 web 版本 windows 对 NAS 进行可视化文件管理。

**前提条件**

开通以下两个产品：

- [函数计算](https://fcnext.console.aliyun.com/overview)

- [文件存储](https://nasnext.console.aliyun.com/overview)

整个实验过程包括：
- 初始化项目
- 部署项目

> start-nas-ui案例仓库地址：https://github.com/devsapp/start-nas-ui

## 初始化项目

进行项目初始化：

```
s init start-nas-ui -d start-nas-ui
```

按照提示， 在命令行交互式中输入您的 NAS 挂载点和对应的 vpc 信息

![](https://img.alicdn.com/imgextra/i4/O1CN01798jXu21VveDo7w8h_!!6000000006991-2-tps-981-455.png)

> 注意， NAS 挂载点的交换机最好在 FC 的可用区， 或者在对应的 VPC 里面新增一个 FC 支持的可用区的交换机

<details>
<summary>函数计算支持的可用区</summary>

| **地域** | **地域ID** | **函数计算支持的可用区** |
| --- | --- | --- |
| 华东1（杭州） | cn-hangzhou | cn-hangzhou-f、cn-hangzhou-g、cn-hangzhou-h |
| 华东2（上海） | cn-shanghai | cn-shanghai-b、cn-shanghai-e、cn-shanghai-g、cn-shanghai-f |
| 华北1（青岛） | cn-qingdao | cn-qingdao-c |
| 华北2（北京） | cn-beijing | cn-beijing-h、cn-beijing-c、cn-beijing-e、cn-beijing-f |
| 华北3（张家口） | cn-zhangjiakou | cn-zhangjiakou-b、cn-zhangjiakou-a |
| 华北5（呼和浩特） | cn-huhehaote | cn-huhehaote-a、cn-huhehaote-b |
| 华南1（深圳） | cn-shenzhen | cn-shenzhen-e、cn-shenzhen-d |
| 西南1（成都） | cn-chengdu | cn-chengdu-a、 cn-chengdu-b |
| 中国香港 | cn-hongkong | cn-hongkong-c |
| 新加坡 | ap-southeast-1 | ap-southeast-1a、ap-southeast-1b |
| 澳大利亚（悉尼） | ap-southeast-2 | ap-southeast-2a、ap-southeast-2b |
| 马来西亚（吉隆坡） | ap-southeast-3 | ap-southeast-3a |
| 印度尼西亚（雅加达） | ap-southeast-5 | ap-southeast-5a、ap-southeast-5b |
| 日本（东京） | ap-northeast-1 | ap-northeast-1b、ap-northeast-1a |
| 英国（伦敦） | eu-west-1 | eu-west-1a |
| 德国（法兰克福） | eu-central-1 | eu-central-a、eu-central-1a、eu-central-1b |
| 美国（硅谷） | us-west-1 | us-west-1a、us-west-1b |
| 美国（弗吉尼亚） | us-east-1 | us-east-1b、us-east-1a |
| 印度（孟买） | ap-south-1 | ap-south-1a、ap-south-1b |
</details>

[文档详情](https://help.aliyun.com/document_detail/72959.html)

## 部署项目

- 进入项目 

  ```
  cd start-nas-ui
  ```

- 部署：

  ```
  s deploy
  ```

部署过程中可能需要阿里云密钥的支持，部署完成之后会获得到临时域名可供测试

![](https://img.alicdn.com/imgextra/i3/O1CN017kCh1T1Jnw7885XO7_!!6000000001074-2-tps-1244-794.png)

浏览器打开域名登录，默认初始化账号和密码是 admin/admin， 您可以登录后， 就得到一个 web 版 windows 用户体验的文件管理系统

![](https://img.alicdn.com/imgextra/i3/O1CN01WRjMv428OKNAu7gjq_!!6000000007922-2-tps-1733-1007.png)

> **注意:**
> 如果您想改成您自己的的域名，通知[自定义域名](https://help.aliyun.com/document_detail/90763.html) 设置成您的域名即可， 如果是通过工具部署的话， 将 s.yaml 中的 domain 中的 auto 换成您自己的域名（需要将您的域名提前设置 CNAME 到 FC 的 endpoint, 详情看自定义域名文档）， 然后 `s deploy` 重新部署即可。

## 其他

> - Serverless Devs 项目：https://www.github.com/serverless-devs/serverless-devs   
> - Serverless Devs 文档：https://www.github.com/serverless-devs/docs   
> - Serverless Devs 钉钉交流群：33947367
