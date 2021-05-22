# 快速体验start-koa

欢迎您使用Serverless Devs开发者工具进行项目开发，本实验是基于Serverless Devs部署start-koa案例到阿里云函数计算。

整个实验过程包括：
- 下载工具
- 配置密钥
- 初始化项目
- 部署项目

> start-koa案例仓库地址：https://github.com/devsapp/start-koa

## 下载工具

通过`npm`安装Serverless Devs开发者工具：

```
npm install -g @serverless-devs/s
```

> 由于本系统已经默认集成了Serverless Devs，所以该步骤在本次试验中可以跳过

## 配置密钥

配置阿里云账号的AccountID,AccessKeyID,AccessKeySecret以及密钥别名。其中，阿里云的密钥信息获取方法可以通过文档：[http://config.devsapp.net/account/alibaba](http://config.devsapp.net/account/alibaba)

配置方法可以通过`s config add`指令，选择`Alibaba Cloud`并根据提示进行配置。

> 在本系统中，可以执行：
>```
>s config add -a default-aliyun -kl AccountID,AccessKeyID,AccessKeySecret -il ${ALIBABA_CLOUD_ACCOUNT_ID},${ALIBABA_CLOUD_ACCESS_KEY_ID},${ALIBABA_CLOUD_ACCESS_KEY_SECRET}
>```
>在执行过程中如果提醒`Alias already exists. Please select a type`，可以直接选择`overwrite`并按回车确定

## 初始化项目

进行项目初始化：

```
s init devsapp/start-koa
```

并按照引导进行项目名称的输入，例如此时输入项目名称`start-koa`

## 部署项目

根据上一步输入的项目名称，进入到项目，例如上一步输入的项目名称是`start-koa`，此时则可以`cd start-koa`

执行部署指令`s deploy`，稍等片刻，即可完成项目的部署

## 其他

> - Serverless Devs 项目：https://www.github.com/serverless-devs/serverless-devs   
> - Serverless Devs 文档：https://www.github.com/serverless-devs/docs   
> - Serverless Devs 钉钉交流群：33947367    
