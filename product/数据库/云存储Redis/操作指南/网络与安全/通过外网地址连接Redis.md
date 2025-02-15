## 通过外网地址连接数据库（本地 Windows 系统）
redis-cli 是原生 Redis 自带的命令行工具，您可以本地设备上安装 redis-cli，通过外网地址连接云数据库 Redis，进行数据管理。 

**redis-cli 命令行的连接方法**

1. [下载 redis-cli](https://github.com/microsoftarchive/redis/releases)，并解压至待安装目录，例如：解压至 `D:\Redis-x64-3.2.100` 目录中 。
2. 在本地设备上，使用 Windows 键 + R 组合键打开**运行**对话框，输入 cmd 单击**确定**，打开 Windows 命令行窗口。
3. 执行如下命令，进入 redis-cli 的安装目录。
```
**cd** /d <path> 
```
其中，path 为 redis-cli 的安装目录。例如：cd /d D:\Temp\Redis-x64-3.2.100
4. 执行如下命令，访问数据库。
```
redis-cli -h <hostname> -p <port> -a <password>
```
其中，hostname：指已申请的外网地址；-p：外网地址对应的网络端口；password：实例默认账号访问密码。若连接时使用的是 [自定义账号](https://cloud.tencent.com/document/product/239/36710)，自定义账号的鉴权方式为`账号名@密码`，作为访问 Redis 的密码参数。
执行示例，请参见下图。
![](https://qcloudimg.tencent-cloud.cn/raw/fff9e2358332579cd84411647e13b6c2.png)


**通过 Redis 客户端连接**
下载 Redis Windows 系统的客户端，配置如下参数，单击**测试连接**，连接数据库实例。
<img src="https://qcloudimg.tencent-cloud.cn/raw/e55154907d4c8df98798cb0a0b9b56d1.png" style="zoom: 30%;" />

| 参数名称 | 参数解释                                                     |
| -------- | ------------------------------------------------------------ |
| **名字** | 连接数据库实例的连接名称。                                   |
| **地址** | 请输入数据库实例的外网地址及其端口号。                       |
| **验证** | 输入数据库实例的连接密码。如果为默认账号，直接输入实例访问密码；如果为[自定义账号](https://cloud.tencent.com/document/product/239/36710)，鉴权方式为 `账号名@密码`。 |

## 使用 redis-cli 通过外网地址连接数据库（本地 Linux 系统）
1. 下载最新稳定的源码包，以6.2.6版本为例。
```
wget https://download.redis.io/releases/redis-6.2.6.tar.gz
```
2. 执行以下命令，对源码包进行解压。
```
tar -zxvf redis-6.2.6.tar.gz
```
3. 进入到源码目录并编译源码文件。
```
cd redis-6.2.6/
```
4. 编译时间根据机器配置决定，请耐心等待。
```
make
```
5. 执行以下命令，通过外网地址，连接数据库。以下 Redis-cli 的路径为默认路径。
```
src/redis-cli -h <hostname> -p <port> -a <password>
```
其中，hostname：指已申请的外网地址；-p：外网地址对应的网络端口；password：实例默认账号访问密码。若连接时使用的是 [自定义账号](https://cloud.tencent.com/document/product/239/36710)，自定义账号的鉴权方式为`账号名@密码`，作为访问 Redis 的密码参数。

   
