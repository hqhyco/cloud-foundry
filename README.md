# IBM Cloud Foundry

## 安装 v2ray cloudfoundry

打开ibm官方shell

### 克隆项目

```bash
git clone https://github.com/badafans/v2ray-cloudfoundry.git
```

### 进入项目目录

```bash
cd v2ray-cloudfoundry
```

### 添加可执行权限

```bash
chmod +x v2ray/v2*
```

###  修改 `v2ray` 的配置文件 `config.json`

修改 alterId `64`

```bash
sed -i "s@64@88@g" v2ray/config.json
```

修改 uuid `8c35bef3-d51f-41ab-ac87-7b053410495b`

```
sed -i "s@8c35bef3-d51f-41ab-ac87-7b053410495b@565b7a05-1fae-4879-9216-986c7b7088ac@g" v2ray/config.json
```

### 修改 `manifest.yml` 文件

`name` 为你的应用名称

```bash
sed -i "s@GetStartedGo@AppName@g" manifest.yml
```

`memory` 为你为应用分配的内存, 实际 `64M` 就够用了

```bash
sed -i "s@128@64@g" manifest.yml
```

### PUSH

```bash
ibmcloud target --cf
ibmcloud cf push
```
