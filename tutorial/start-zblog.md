# 快速体验start-zblog

1. 通过命令`npm install -g @serverless-devs/s`安装Serverless devs命令行工具（**由于本系统已经默认集成了Serverless Devs，所以该步骤在本次试验中可以跳过**）
2. 进行密钥的配置
    - 阿里云的密钥获取方法可以参考页面：http://config.devsapp.net/account/alibaba
    - **在本系统中，可以执行`s config add -a default-aliyun -kl AccountID,AccessKeyID,AccessKeySecret -il ${ALIBABA_CLOUD_ACCOUNT_ID},${ALICLOUD_SECRET_KEY},${ALIBABA_CLOUD_ACCESS_KEY_SECRET}`，在执行过程中如果提醒`Alias already exists. Please select a type`，可以直接选择`overwrite`并按回车确定**
3. 进行项目初始化：`s init devsapp/start-zblog`，并按照引导进行项目名称的输入，例如此时输入项目名称`start-zblog`
4. 根据上一步输入的项目名称，进入到项目，例如上一步输入的项目名称是`start-zblog`，此时则可以`cd start-zblog`
5. 执行部署指令`s deploy`，稍等片刻，即可完成项目的部署
