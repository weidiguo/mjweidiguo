# ChatGPT Web Midjourney Proxy
💡**声明**
- 此项目只发布于 GitHub，基于 MIT 协议，免费且作为开源学习使用。并且不会有任何形式的卖号、付费服务、讨论群、讨论组等行为。谨防受骗。
- 本开源是在 [ChenZhaoYu](https://github.com/Chanzhaoyu/chatgpt-web) 基础上做二次开发 ；使用 [midjourney-proxy](https://github.com/novicezk/midjourney-proxy) 提供的midjourney api 作为后端而形成的。


![cover](./docs/mj2a1.jpg)
## 支持功能
- ✅ 原chatgpt web 所有功能
- ✅ chatgpt web 支持自定义api key、base_url
- ✅ midjourney 文生图
- ✅ midjourney 垫图+文生图  
- ✅ midjourney 图变 U1到U4 、 V1到V4、重绘等操作
- ✅ midjourney 支持局部重绘
- ✅ midjourney 支持1.5倍变焦 2倍变焦
- ✅ midjourney 支持2倍高清 4倍高清
- ✅ midjourney 支持左、右、上、下延伸变化
- ✅ midjourney 同时支持[midjourney-proxy](https://github.com/novicezk/midjourney-proxy) 接口 和 [midjourney-proxy-plus](https://github.com/litter-coder/midjourney-proxy-plus) 接口
- ✅ midjourney 图生文
- ✅ 图片使用localforage实现本地存储
- ✅ 支持midjourney、niji 不同机器人
- ✅ 支持[InsightFace 人脸替换](https://discord.com/api/oauth2/authorize?client_id=1090660574196674713&permissions=274877945856&scope=bot)
- ✅ midjourney 混图
- ✅ midjourney 获取 seed
- ✅ dall-e-3 画图
- ✅ chatgpt 前端选择模型
- ✅ chatgpt 前端支持自定义模型、上下文对话数、回复数
- ✅ chatgpt 支持图片上传图片 供gpt-4-vision-preview使用
- ✅ chatgpt 支持文件后端上传（供给gpt-4-all gpt-4-gizmo-xxx 模型）！ 默认是关闭的 打开需要环境变量 API_UPLOADER=1
- ✅ chatgpt 支持逆向模型 gpt-4-all gpt-4-v gpt-4-gizmo-(gizmo_id)
- ✅ chatgpt 支持超链模型切换 https://vercel.ddaiai.com/#/m/gpt-4-all https://vercel.ddaiai.com/#/m/gpt-4-gizmo-g-2fkFE8rbu
- ✅ 支持ChatGPT试的超链模型切换 https://chat.openai.com/g/g-2fkFE8rbu 修改为 https://vercel.ddaiai.com/#/g/g-2fkFE8rbu
- ✅ chatgpt 支持 GPTs 多模态
- ✅ chatgpt 支持 tts whisper
- ✅ 即时语音识别(浏览器自带语音识别 ASR) `v2.15.7`以上版本
- ✅ 支持超链更换设置，适合 one-api 部署聊天 https://vercel.ddaiai.com/#/s/t?OPENAI_API_BASE_URL=https://abc.com&OPENAI_API_KEY=sk-xxxxx&MJ_SERVER=https://abc.com&MJ_API_SECRET=sk-xxx&UPLOADER_URL=
- ✅ 支持one-api部署聊天 https://vercel.ddaiai.com/#/?settings={%22key%22:%22sk-abc%22,%22url%22:%22https://www.abc.com%22} `(v.2.14.3)`
## 待开发
- ⏰ 支持 GPTs 多模态


## Vercel 一键部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Dooy/chatgpt-web-midjourney-proxy&env=OPENAI_API_BASE_URL&env=OPENAI_API_KEY&env=MJ_SERVER&env=MJ_API_SECRET&project-name=chatgpt-web-midjourney-proxy&repository-name=chatgpt-web-midjourney-proxy)

## env 环境变量

| 环境变量 | 说明 | 默认值 |docker等部署| vercel 部署|
| --- | --- | --- | --- | --- |
| OPENAI_API_BASE_URL | OpenAI API 接口地址 | https://api.openai.com | ✅ |  ✅|
| OPENAI_API_KEY | OpenAI API 密钥 |  sk-xxxxx | ✅ |  ✅|
| OPENAI_API_MODEL |  默认模型 | gpt-3.5-turbo  | ✅ |  ✅|
| MJ_SERVER |  mj proxy 接口地址 | https://api.openai.com  | ✅ |  ✅|
| MJ_API_SECRET |  mj proxy | 空  | ✅ |  ✅|
| AUTH_SECRET_KEY |  访问授权密码 | 无  | ✅ |   x|
| API_UPLOADER |  支持上传 | 关闭  | ✅ |  x|
| HIDE_SERVER |  前端ui隐藏服务端|    | ✅ |  x|
| CUSTOM_MODELS |  自定义可选模型 | 无  | ✅ |  ✅|
| TJ_BAIDU_ID |  百度统计ID | 无  | ✅ |  ✅|
| TJ_GOOGLE_ID |  谷歌统计ID | 无  | ✅ |  ✅|
| SYS_NOTIFY |  系统通知，支持HTML | 无  | ✅ |  ✅|
| DISABLE_GPT4 |  禁用GPT-4 | 无  | ✅ |  ✅|
| GPT_URL | 自定 GPT_URL=/gpts.json  | 无 也可自己的外链 | ✅ |  ✅|
| UPLOAD_IMG_SIZE | gpt4v 上传图片大小 |  1 | ✅ |  ✅|
| SYS_THEME | 默认主题 `light`或者`dark`  | dark | ✅ |  ✅|
| MJ_IMG_WSRV | 是否开启 `wsrv`图床  | 无(关闭)  | ✅ |  ✅|
| AUTH_SECRET_ERROR_COUNT | 防爆破验证：验证次数触发 NGINX 请设置 `proxy_set_header   X-Forwarded-For  $remote_addr`  | 无  | ✅ |  x|
| AUTH_SECRET_ERROR_TIME | 防爆破验证：停留时间 单位分钟  | 无  | ✅ |  x|
| CLOSE_MD_PREVIEW | 是否不关闭输入预览 | 无  | ✅ |  ✅|
| UPLOAD_TYPE | 指定上传方式 [`R2` R2上传] [`API` 跟随UI前端中转]、[`Container` 本地容器]、[`MyUrl` 自定义链接]  |  空 | ✅ |  x|

  

## docker 部署
**假设**:
- 你已经搭建好 [midjourney-proxy](https://github.com/novicezk/midjourney-proxy) 服务，开发端口服务器地址为 https://172.17.0.1:6013
- [midjourney-proxy](https://github.com/novicezk/midjourney-proxy) 服务 的 API_SECRET  为 abc123456
```bash
docker run --name chatgpt-web-midjourney-proxy  -d -p 6015:3002 \
-e OPENAI_API_KEY=sk-xxxxx \
-e OPENAI_API_BASE_URL=https://api.openai.com  \
-e MJ_SERVER=https://172.17.0.1:6013  \
-e MJ_API_SECRET=abc123456  ydlhero/chatgpt-web-midjourney-proxy
```
访问 http://ip:6015 

**文件上传**: 
```bash
docker run --name chatgpt-web-midjourney-proxy  -d -p 6015:3002 \
-e OPENAI_API_KEY=sk-xxxxx \
-e OPENAI_API_BASE_URL=https://api.openai.com  \
-e MJ_SERVER=https://172.17.0.1:6013  \
-e API_UPLOADER=1  -v /data/uploads:/app/uploads \
-e MJ_API_SECRET=abc123456  ydlhero/chatgpt-web-midjourney-proxy
```
如果是前端ui设置 OPENAI_API_KEY OPENAI_API_BASE_URL ; 图片上传也会随着走 OPENAI_API_BASE_URL走
```shell
curl -X POST -H "Content-Type: multipart/form-data" -F "file=@/path/to/file" http://OPENAI_API_BASE_URL/v1/upload
```
返回格式
```json
{
"url":"https://xxxxxxx.jpg"
}
```

### midjourney-proxy API docker部署
更多参考到 [midjourney-proxy](https://github.com/novicezk/midjourney-proxy) 开源光光
```bash
docker run -d --name mj6013  -p 6013:8080  \
-e mj.discord.guild-id=discord服务ID  \
-e mj.discord.channel-id=discord服务组ID   \
-e mj.queue.timeout-minutes=6 \
-e mj.api-secret=abc123456 \
-e mj.discord.user-token=**********  \
--restart=always novicezk/midjourney-proxy:2.5.5
```


## 更多展示

### 自定义服务端api key、base_url：
![base_url](./docs/gptbase.jpg)

### GPTS  GTP Store 
![多模态](./docs/gpts.jpg)
![多模态](./docs/gpts1.jpg)

### 录音 whisper  和  tts
![whisper--tts](./docs/tts-whisper.png)

### 局部重绘：
[![局部重绘](./docs/mj2.jpg)](./docs/mj2.jpg)

### 换脸
![换脸](./docs/mj2a2.jpg)

### 混图
![混图](./docs/mj2a3.jpg)

### 支持图片上传图片 供gpt-4-vision-preview使用
![混图](./docs/mj4a1.png)
手机端：
<div style="display: flex; flex-wrap: wrap">
 <img src="./docs/mjs1.jpg" style="width:200px" >
 <img src="./docs/mjs2.jpg"  style="width:200px">
 <img src="./docs/mjs3.jpg"  style="width:200px">
</div>


## 文件上传 支持cloudflare r2 存储

- cloudflare r2 存储 10 GB/月 免费 https://www.cloudflare.com/zh-cn/developer-platform/r2/
- 配置文档参考 https://zhuanlan.zhihu.com/p/658058503
- vercel 不支持 r2 存储
```yml
R2_DOMAIN=
R2_BUCKET_NAME=
R2_ACCOUNT_ID=
R2_KEY_ID=
R2_KEY_SECRET=
```
## 文件服务器请求优先顺序
R2> 前端UI设置文件服务> 后端文件服务 >跟随中转
## 防爆破验证设置

![防爆破](./docs/check_error.jpg)
- [x] vercel 不支持；仅支持Docker化部署
- [x] 如果前面挂载 `nginx` 请配置 `proxy_set_header   X-Forwarded-For  $remote_addr;`
- [x] 参数如下: 错误验证3次，只能在10分钟后再验证
```yml
# Secret key 注意: 只能拿事英文+数字
AUTH_SECRET_KEY=my888god
#爆破：验证次数 注意: 数字 ；nginx 请设置  proxy_set_header   X-Forwarded-For  $remote_addr;
AUTH_SECRET_ERROR_COUNT=3
#爆破：验证停留时间 单位分钟 注意: 是数字
AUTH_SECRET_ERROR_TIME=10
```
- [x] 脚本如下
```shell
docker run --name chatgpt-web-midjourney-proxy  -d -p 6015:3002 \
-e OPENAI_API_KEY=sk-xxxxx \
-e OPENAI_API_BASE_URL=https://api.openai.com  \
-e MJ_SERVER=https://172.17.0.1:6013  \
-e MJ_API_SECRET=abc123456 \
-e API_UPLOADER=1  -v /data/uploads:/app/uploads \
-e AUTH_SECRET_KEY=你的英文密码 -e AUTH_SECRET_ERROR_COUNT=3 \
-e AUTH_SECRET_ERROR_TIME=10 ydlhero/chatgpt-web-midjourney-proxy
```
- 
## License
MIT © [Dooy](./license)

## 其他
如果觉得这个项目对您有所帮助，请帮忙点个star 或者捐助我们

[![Star History Chart](https://api.star-history.com/svg?repos=Dooy/chatgpt-web-midjourney-proxy&type=Date)](https://star-history.com/#Dooy/chatgpt-web-midjourney-proxy&Date)

## 捐助
如果我的开源项目对你有帮助，请考虑通过以下任意一种方式赞助: 
<br> `付款备注上您的联系方式`
<div style="display: flex; flex-wrap: wrap">
    <div style="width:200px">
        <img src="./docs/wxpay.jpg"  style="width:200px">
        <div>微信捐助</div>
    </div>
    <div style="width:200px">
        <img src="./docs/alipay.jpg"  style="width:200px"> 
        <div>支付宝捐助</div>
    </div>
</div>