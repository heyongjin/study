# JobServer

Job Server对所有的轮询任务进行管理，把需要轮询的任务从每个分散的节点集合到一个完整的容器里去。独立运行，不影响到主应用，功能完整的日程任务调度系统,基于开源的Quartz Job Scheduling Framework开发

## 介绍说明

目录大概：

    jobserver
    └── config  配置文件目录
	└──shell 启停JobServer的脚本
	│    │    └── jobserver.bat
	│    │    └──jobserver.sh
    └── jobserver 工程目录
	│    └──src
	│    │    └── main
	│    │    │    └──java
	│    │    │    └──resources
	│    │    └── test
	│    └──pom.xml
    └── scripts  数据库脚本
	│    └──ftf_v8_jobserver_tables_oracle.sql
	│    └──ftf_v8_jobserver_tables_sybase.sql
    └── README.MD

## jar包依赖

环境准备

- 需要maven工程，配置本地maven环境

		<dependency>
            <groupId>com.ztesoft.zsmart.job</groupId>
            <artifactId>jobserver</artifactId>
            <version>8.1.0-SNAPSHOT</version>
        </dependency>

## 原文件下载：

    git clone http://gitlab.ztesoft.com/jobserver/jobserver.git

	
## 使用详解
关于部署需要的jar包以及启动脚本需要的jobserver.properties请参考 [maven插件使用][2]


关于JobServer的资料，请参考[前台框架SVN上的资料][1]


  [1]: http://10.45.7.141:9050/svn/Development_Dept/%E5%BC%80%E5%8F%91%E4%B8%80%E9%83%A8%E9%83%A8%E9%97%A8%E6%96%87%E6%A1%A3/%E6%8A%80%E6%9C%AF%E8%B5%84%E6%96%99/Development/%E5%89%8D%E5%8F%B0%E6%A1%86%E6%9E%B6/07%20%E6%9C%8D%E5%8A%A1%E7%AB%AF%E6%A1%86%E6%9E%B6/Job%
  [2]: http://10.45.4.178:8081/nexus/doc/maven-zsmartdependency-plugin/commanduse.html