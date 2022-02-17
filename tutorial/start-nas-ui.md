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

## 部署项目

- 进入项目 `cd start-nas-ui`

- 进入项目后：
  - 将 s.yaml 中对应的 NAS 信息改成成您自己的，如下图:
    - ![](https://img.alicdn.com/imgextra/i4/O1CN01CfRqMv234ZCoI2ZyN_!!6000000007202-2-tps-870-414.png)
  - 执行 `s fc-nas-filemgr nas upload -r code/kodbox /mnt/nas/.fc-nas-filemgr` 将 web UI 管理工程上传到 NAS
  - 部署：`s deploy`
- 部署过程中可能需要阿里云密钥的支持，部署完成之后会获得到临时域名可供测试

![](https://img.alicdn.com/imgextra/i3/O1CN017kCh1T1Jnw7885XO7_!!6000000001074-2-tps-1244-794.png)

## 体验 NAS 的WEB UI 管理

浏览器打开域名登录，默认初始化账号和密码是 admin/admin， 您可以登录后， 就得到一个 web 版 windows 用户体验的文件管理系统

![](https://img.alicdn.com/imgextra/i3/O1CN01WRjMv428OKNAu7gjq_!!6000000007922-2-tps-1733-1007.png)

## 其他

> - Serverless Devs 项目：https://www.github.com/serverless-devs/serverless-devs   
> - Serverless Devs 文档：https://www.github.com/serverless-devs/docs   
> - Serverless Devs 钉钉交流群：33947367    
