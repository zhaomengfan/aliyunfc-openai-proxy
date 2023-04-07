
# aliyunfc-openai-proxy

<description>

快速部署一个代理 OpenAI API 的服务到阿里云，用于解决国内访问 OpenAI API 的问题。
使用的是阿里云函数计算，可以快速部署，无需搭建服务器。
需要先注册阿里云账号，开通函数计算服务。

</description>

# 使用流程

## 准备工作

1、注册阿里云账号并开通：函数计算 FC <https://fcnext.console.aliyun.com/> \
2、安装 Serverless Devs,参考文档<https://help.aliyun.com/document_detail/195474.html/>

```bash
npm install @serverless-devs/s -g
```

3、配置密钥信息,参考文档<https://help.aliyun.com/document_detail/295894.html/>

## 部署

1. 在code目录下执行`npm install`安装依赖
2. 在项目根目录下执行：`s deploy`，根据提示部署到阿里云

## 使用文档

部署完成之后可以再控制台查看\
<img src="https://img1.imgtp.com/2023/04/07/4SyJi9r1.png" width="500" />\
<img src="https://img1.imgtp.com/2023/04/07/e6JkJJyl.png" width="500" />\
这里的公网访问地址为阿里云生成的临时地址，可以直接使用，替代<https://api.openai.com> \
<img src="https://img1.imgtp.com/2023/04/07/tFVWqiHq.png" width="500" /> \
如果有需要可以在控制台配置自定义域名，参考文档<https://help.aliyun.com/document_detail/90763.html>

# 快速应用

推荐使用<https://github.com/mckaywrigley/chatbot-ui> 这个项目快速搭建一个聊天机器人界面，使用这个项目的时候需要修改`.env.local`中的`OPENAI_API_HOST`为上面的公网访问地址即可，如下图:\
<img src="https://img1.imgtp.com/2023/04/07/tItm8GUd.png" width="500" />

以上就可以快速搭建一个本地的聊天机器人了，可以在本地测试，也可以部署到服务器，不需要🪜
