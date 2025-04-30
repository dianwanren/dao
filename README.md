第一次更新时

1. 拉取仓库源(第二次及之后跳过这一步)
```shell
curl -s -L https://github.com/nikkinikki-org/OpenWrt-nikki/raw/refs/heads/main/feed.sh | ash
```
2. 卸载 & 重置
```shell
curl -s -L https://github.com/nikkinikki-org/OpenWrt-nikki/raw/refs/heads/main/uninstall.sh | ash
```


3. 更新op软件仓库
```shell
opkg update
```

4. 安装
```shell
opkg install nikki
opkg install luci-app-nikki
opkg install luci-i18n-nikki-zh-cn
```

..................................................................................................................................................................................................................
































feichangdao:                 正式版自用规则（通用规则）

```bash
https://raw.githubusercontent.com/dianwanren/dao/main/feichangdao.ini
```

daochangzai:                 增强版自用规则（主要适配META内核）


```bash
https://raw.githubusercontent.com/dianwanren/dao/main/daochangzai.ini
```


其余皆为个人搞实验  




搭建docker本地转换步骤
依次点击  
容器——添加——命令行——复制粘贴以下其中一条命令后——提交。
以下命令行（二选一）  
  
tindy2013版本（该项目原作者的版本）

```bash
docker run -d --restart=always -p 25500:25500 tindy2013/subconverter:latest
```  

sdlokj1qpi23（肥羊）版本（基于上面原作者的修改版，增加了更多的类型支持）  


```bash
docker run -d --restart=always -p 25500:25500 asdlokj1qpi23/subconverter:latest
```  


   
返回——docker——容器——勾选复选框——启用（红字表示禁用，绿色表示启用）  


搭建后的地址  
```bash
http://localhost:25500/sub
```

docker搭建本地前端
```bash
docker run -d --name subweb --restart always \
  -p 18080:80 \
  -v /mnt/GZ/conf:/usr/share/nginx/html/conf \
  stilleshan/subweb
```
