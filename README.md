# IBM Cloud Foundry

## 部署 V2ray

fork 本项目

Settings >  Secrets

添加

API_SERVER: `https://api.us-south.cf.cloud.ibm.com`
USERNAME: 账号
PASSWORD: 密码
APPNAME: 你应用名称
UUID: V2ray UUID, 可以作用 `http://www.uuid.online/` 生成一个。
ALTER_ID: 额外ID, 建议使用 `0`
WSPATH: 路径, 建议使用 `/`

## 定时重启
