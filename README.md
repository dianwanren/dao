feichangdao:                 正式版自用规则（主要适配普通内核）
https://raw.githubusercontent.com/dianwanren/dao/main/feichangdao.ini


daochangzai:                 增强版自用规则（主要适配META内核）
https://raw.githubusercontent.com/dianwanren/dao/main/daochangzai.ini



其余皆为个人搞实验




搭建docker本地转换步骤
依次点击 
容器——添加——命令行
复制粘贴以下命令行
```bash
docker run -d --restart=always -p 25500:25500 tindy2013/subconverter:latest
