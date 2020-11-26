# chaoxing_action
使用Github Action自动完成学习通签到

# 食用方法 

在GitHub对应仓库中添加以下Secrt值:

```
LATITUDE   签到纬度
LONGITUDE   签到经度
PASSWORD   登录密码
RUN_TIME   持续轮询次数
SECRET    Serverchan的secret
USER      用户名
```

修改 `.github\workflows\run.yml` 将里面的 `30 2 * * *` 换成你自己的签到时间

时间格式为`分钟 小时 日 月 年`，默认为每天晚上北京时间`10：30`进行签到，详细格式详见cron设置

感谢[mkdir700/chaoxing_auto_sign](https://github.com/mkdir700/chaoxing_auto_sign)项目