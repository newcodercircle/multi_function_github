# multi_function_github
运行环境：Java8，maven

- ChatGPT接入企业微信成为聊天机器人

## 脚本使用
### ChatGPT 3.5接入企业微信
- 修改application.properties文件的chatgpt开头 和wechat开头的配置，配置内容看注释
- 默认访问超时时间是30s，如需修改，可自行修改`OkHttpUtils`中`DEFAULT_TIME_OUT`的值
- 发送`开始连续对话`进入连续对话模式，注意连续对话模式下，chatGPT账号额度消耗是累加（每次发消息，会累加这次和过去所有对话的额度消耗）
- 发送`结束连续对话`关闭连续对话模式
- 可修改application.properties文件里的`chatgpt.flow.num`配置，自行修改最大对话次数（不建议太大，官方限制的消息最大长度是4096 token，大概20次对话之后就会超了）
