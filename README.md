<details>
<summary>✔️多用户版本</summary>
每日机场自动签到

根据 https://github.com/ne-21/sspanel-automaticcheckin 代码修改，不支持登陆需要人机验证的机场。

首先fork本项目到自己的仓库

进入自己fork的仓库，点击 Settings-> Secrets-> New Secrets 添加以下5个Secrets。

WEB     签到机场网址,多个网址用英文逗号分割。需要注意格式，否则可能会出现一些BUG，这个地址例如：https://www.iruanp.com 这种，带上协议，结尾不要斜杠

USER    签到机场登陆邮箱,与网站对应,多个用户用英文逗号分割。

PWD     签到机场登陆密码,与网站对应,多个密码用英文逗号分割。

SCKEY   可选设置，微信推送SCKEY码，详情参见http://sc.ftqq.com/

KTKEY   可选设置，QQ推送Skey码，详情参见https://cp.xuthus.cc/
| 参数  | 是否必须  | 内容  | 示例  |
| ------------ | ------------ | ------------ | ------------ |
| USER  | 是  | 注册机场所用邮箱  | a@example.com 401664491@qq.com,j0vp0dvh@chapedia.org,j0vp0dvh@truthfinderlogin.com |
| PWD  | 是  | 注册机场所用密码  | password1  |
| WEB  | 是  | 机场地址  | https://dy.juai.org  |
| SCKEY  | 否  | Sever酱秘钥  | SCTxxxxxxxxxxxxxx  |




</details>
<details>
<summary>✔️单用户版本</summary>
#单用户版本https://github.com/xiaocao666tzh/Airport-Checkin

| 参数  | 是否必须  | 内容  | 示例  |
| ------------ | ------------ | ------------ | ------------ |
| EMAIL  | 是  | 注册机场所用邮箱  | a@example.com  |
| PASSWORD  | 是  | 注册机场所用密码  | password1  |
| BASE_URL  | 是  | 机场地址  | https://examplea.com  |
| SCKEY  | 否  | Sever酱秘钥  | SCTxxxxxxxxxxxxxx  |
| TGBOT  | 否  | Telegram推送bot  | 5xxxxxxx:xxxxxxxxx  |
| TGUSERID  | 否  | Telegram推送人id  | 8xxxxxxxxx  |

转到`Actions`创建一个workflow，运行一次，以后每天项目都会自动运行。最后，可以到Run sign查看签到情况，同时也会通过Sever酱发送出去。
</details>