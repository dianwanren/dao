feichangdao:                 正式版自用规则（主要适配普通内核）

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
容器——添加——命令行
复制粘贴以下命令行（二选一）
  
tindy2013版本（该项目原作者的版本）

```bash
docker run -d --restart=always -p 25500:25500 tindy2013/subconverter:latest
```

sdlokj1qpi23（肥羊）版本（基于上面原作者的修改版，增加了更多的类型支持）


```bash
docker run -d --restart=always -p 25500:25500 asdlokj1qpi23/subconverter:latest
```
