# mongodb 入门
* 官方下载地址 [https://www.mongodb.com](https://www.mongodb.com/download-center?jmp=docs&_ga=1.77682269.851258951.1470304931)
* manual [下载指南](https://docs.mongodb.com/manual/)

### 使用步骤
* 下载到本后查看二进制文件

+ ```
bsondump
mongo
mongod
mongodump
mongoexport
mongofiles
mongoimport
mongooplog
mongoperf
mongorestore
mongos
mongosniff
mongostat
mongotop
```
### 本地搭建简单的数据服务
* 创建一个文件 mkdir mongodb
* 在文件中 创建 data文件 mkdir data 存储数据的文件
* 在创建个conf文件，mkdir conf 在conf文件中，创建个启动服务的conf文件



	```
	port = 1234 #服务的端口
	dbpath = data # 存储数据的文件
	logpath = log/mongod.log #日志文件
	fork = true
	```
* 在创建个log文件 mkdir log 存储日志
* 在创建个bin文件，mkdir bin 此文件是存储mongodb的而建文件 cp -R -n <mongodb-install-directory>/bin:$PATH /bin
* 然后执行 mongod -f conf/mongod.conf 启动服务

### 启动数据的本地服务
* mongo --help

	``` 
	usage: mongo [options] [db address] [file names (ending in .js)]

	```
	
* mongo 127.0.0.1:12345/test 启动服务