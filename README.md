# chaoxing_action
使用Github Action自动完成学习通签到

# 食用方法 

fork本仓库，在GitHub对应仓库中添加以下Secret值:

```
LATITUDE   签到纬度
LONGITUDE   签到经度
PASSWORD   登录密码
RUN_TIME   持续检测签到次数,每一分钟检测一次，十次就是每隔一分钟检测一次，共检测十次
SECRET    ServerChan的SCKEY
USER      用户名
```

修改 `.github\workflows\run.yml` 将里面的 `30 14 * * *` 换成你自己的签到时间，程序将会在这个时间开始检测是否有签到任务

时间格式为`分钟 小时 日 月 星期`，默认为每天晚上北京时间`10:30`进行签到，如果你需要修改签到时间则必须将你的时间转化为UTC时间再填入(例如北京时间晚上`10:30`转换为`14:30`)，你可以使用在线工具进行转换，时间详细格式详见cron设置

仓库可以在公开状态运行，所有关键内容只会被保存在Secret里

## ServerChan的SCKEY获取方式:

打开此网页[http://sc.ftqq.com/?c=code](http://sc.ftqq.com/?c=code)，完成登录并绑定微信即可看到SCKEY

![](https://cdn.jsdelivr.net/gh/mzdluo123/blog_imgs/img/20201126210836.png)

添加完成后应该是这样的

![](https://cdn.jsdelivr.net/gh/mzdluo123/blog_imgs/img/20201126210549.png)



感谢[mkdir700/chaoxing_auto_sign](https://github.com/mkdir700/chaoxing_auto_sign)项目
