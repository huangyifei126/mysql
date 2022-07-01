# mysql
安装博客
https://www.cnblogs.com/linglei/p/14519416.html

sysbench安装
https://blog.csdn.net/weixin_34376562/article/details/93404795
https://blog.csdn.net/jolly10/article/details/80388217/

mysql 带宽测试_网络带宽如何影响 MySQL 性能
https://blog.csdn.net/weixin_42362491/article/details/113256039

Sysbench和Unixbench工具测试内存线程io和带宽
https://blog.csdn.net/weixin_51134188/article/details/116377801

Sysbench压力测试基准测试用例
https://blog.csdn.net/cdrcsy/article/details/73277591

1、研读Hadoop-master源码，添加白名单
方案：
（1）shell脚本
（2）Java编写socket
（3）c语言
最终：通过Java调C接口方式添加白名单

2、开源Hadoop、sqoop源码编译，rpm包制作
（1）修改了文件，添加白名单（DefaultContainerExecutor.java,LinuxContainerExecutor.java）
（2）新增文件（ChangLiuJavaTools.java）
（3）修改pom文件
（4）注释暂时用不到的模块（Hadoop-aws，hadoop-yarn-applications-catalog-webapp）
（5）编译
rpm包制作：
（1）拷贝编译好的tar.gz包指定目录SOURCE
（2）在SPECS目录制作spec文件
（3）执行构建rpm命令
3、组建开源组件大数据集群，设计离线数仓
（1）辅助自华离线数仓案例场景演示
（2）拉会讲解开源组件安装流程
（3）输出集群组件部署文档（大数据部署指南，大数据离线数仓分析应用场景技术详解）

4、组件开源组件大数据集群，设计实时数仓
（1）方案设计
（2）环境准备
（3）部署组件
（4）拉去服务
（5）基于spark实时计算Demo开发
（6）基于Flink实时计算Demo开发
（7）上机测试
（8）拉会评审
（9）输出文档（大数据实时分析应用场景技术详解，大数据部署指南）
测试结果：表明开源大数据组件基本上能在专用机拉起服务并且能够跑大数据业务

5、专用机MySQL性能
测试不同电口（1G和10G）下MySQL读取过程的实际网络传输速率
（1）测试环境

（2）组网
1台被测端Server用于数据库测试；一台客户端Client用于对被测端进行施压
（3）测试工具sysbench
(4)测试模型
sysbench性能测试
Jar包测试MySQL数据导出
Loader测试mysql数据导出

6、MRS使能过程的白名单问题
（1）FusionInsight MRS在专用机安装部署
Manager服务拉取过程中controller服务器启动失败，存在白名单
添加白名单，编译Java类，替换字节码，测试验证是ok
（2）提供白名单jar
将之前做的白名单工具做出jar，放在jre扩展包，供其他调用，测试验证是OK的

7、两节点MRS集群部署与安装
专用机的限制，安装过程较复杂，每一次不一定能部署成功
（1）补报
（2）用户预制（omm,ommdba）
（3）命令预制（tar,cp,ping,clswl）
（4）设置fimanager的tlsv1.1
（5）web界面安装oms
（6）使用killomm-2.12-1.aarch64.rpm杀死所有的omm进程

8、大数据组件功能验证

9、麒麟专用机MRS大数据组件适配
1	DBserver 2.70 底层服务
2	Meta	2.7.0	底层服务
3	LdapServer	2.7.0	底层服务
4	Krbserver	1.18	底层服务
5	Range	2.0.0	底层服务
6	Zookeeper	3.6.3	
7	Hadoop	3.2.1
8	HBASE	2.2.3
9	Hive	3.1.0
10	Sqoop(Loader)	1.99.3
11	Kafka	2.4.0
12	Redis	6.0.12
13	Elasticsearch	7.10.2
14	Hue	4.7.0
15	Oozie	5.1.0
16	Tez	0.9.2
17	CDL	1.0.0
18	Flink	1.12.2
19	Spark	3.1.1
20	Hudi	0.8.1
21	Flume	1.9.0
 
10、支援新疆大数据项目

11、专用机适配开源的ELK软件，搭建ELK集群，出软件版本

12、专用机适配开源canal和sqoop，并出软件版本

13、logstash组件白名单问题解决
14、大数据组件小场景业务案例
	logstash同步MySQL到ES
	clickhouse用户留存案例，行为漏斗转化案例
	sqoop将MySQL导入HDFS，将HDFS数据导出到MySQL
	canal增量同步MySQL数据到ES
15、Hadoop、hive、HBASE、ES的性能测试

16、es的web应用，用户管理系统；clickhouse的web应用，图书馆系统

17、实时车流量监控项目

18、航天科技MRS POC测试
	准备MRS集群环境，白名单加固；
	和EI团队对接，解决hetu计算集群启动失败，hetu测试hive和hbase失败，跨源查询失败
	FlinkServer对接hive创建集群连接失败，FlinkServer对接hudi数据导入失败；
	Flinkserver对接hbase数据未导入hbase

19、大数据白名单工具功能和性能测试

20、ELK出RPM包以及解决pulsar组件白名单问题

21、Graphhbase问题和EI沟通解决。修改脚本，注释了

22、OLAP引擎选型
