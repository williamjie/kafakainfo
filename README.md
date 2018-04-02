# kafakainfo

Error while executing topic command : replication factor: 1 larger than available brokers: 0

清空kfka data目录文件（打包机data目录文件与mac文件目录机构不一致导致）
出现这种错误有很多，我只说我的是怎么解决的

1.有可能是你的server.properties配置的问题，其中的每一台机子的

broker.id=1
都要不相同
2.你可能没启动kafka中的broker

进入{zookeeper_home}/bin目录下

./zkCli.sh

然后

ls /brokers/ids

你会看到自己的节点数（是否是和你启动的是一样的）

如果不一样，那就重新启动kafka
