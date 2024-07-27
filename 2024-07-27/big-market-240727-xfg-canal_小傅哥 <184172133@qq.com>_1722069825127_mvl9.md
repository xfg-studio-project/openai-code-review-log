根据提供的Git diff记录，以下是对代码变更的评审：

### .codechina-ci.yml
- **删除的测试任务**：`.codechina-ci.yml`文件中删除了两个测试任务`test-job1`和`test-job2`。没有提供删除原因，需要确认是否这些测试任务已经过时或被替代。
  - **建议**：如果测试任务被替代，应在相关文档中记录替代任务的信息。

### big-market-app/src/main/resources/application-dev.yml
- **数据库连接变更**：在`application-dev.yml`文件中，将数据库连接地址从`127.0.0.1`变更为`192.168.1.108`。这可能意味着数据库服务器的环境发生了变化。
  - **建议**：确认数据库服务器地址变更的原因，并确保所有相关服务配置已更新。
  - **注意**：地址变更可能影响其他依赖数据库的服务。

### big-market-app/src/test/java/cn/bugstack/test/trigger/RaffleActivityControllerTest.java
- **测试用例修改**：在`RaffleActivityControllerTest`类中，`test_draw`和`test_calendarSignRebate`测试用例中的循环次数从1改为10。这可能意味着测试用例的复杂度或测试覆盖率有所增加。
  - **建议**：确保增加循环次数的动机，并验证测试结果的正确性。

### big-market-domain/src/main/java/cn/bugstack/domain/activity/service/partake/RaffleActivityPartakeService.java
- **代码注释修改**：`RaffleActivityPartakeService`类中的注释从“创建月账户额度”改为“创建日账户额度”。这可能意味着功能实现有所变更。
  - **建议**：确认注释修改的准确性，并更新相关文档以反映功能变更。

### docs/dev-ops/canal-adapter/application.yml
- **新的配置文件**：添加了新的`application.yml`配置文件，用于配置Canal适配器。
  - **建议**：确保配置文件正确无误，并与其他配置文件保持一致。

### docs/dev-ops/canal-adapter/es7/... (多个文件)
- **新的配置文件**：添加了一系列Elasticsearch映射配置文件，用于将Canal数据同步到Elasticsearch。
  - **建议**：确保映射配置正确无误，并测试数据同步过程。

### docs/dev-ops/canal/instance.properties
- **新的配置文件**：添加了新的`instance.properties`配置文件，用于配置Canal实例。
  - **建议**：确保配置文件正确无误，并测试Canal实例的功能。

### docs/dev-ops/curl/... (多个文件)
- **新的脚本文件**：添加了多个curl脚本文件，用于管理Elasticsearch索引。
  - **建议**：确保脚本文件正确无误，并测试索引管理功能。

### docs/dev-ops/docker-compose-environment-aliyun.yml, docs/dev-ops/docker-compose-environment-private.yml, docs/dev-ops/docker-compose-environment.yml
- **新的Docker Compose配置文件**：添加了多个Docker Compose配置文件，用于部署整个系统。
  - **建议**：确保配置文件正确无误，并测试整个系统的功能。

### docs/dev-ops/kibana/config/kibana.yml
- **新的Kibana配置文件**：添加了新的Kibana配置文件，用于配置Kibana。
  - **建议**：确保配置文件正确无误，并测试Kibana的功能。

### docs/dev-ops/logstash/logstash.conf
- **新的Logstash配置文件**：添加了新的Logstash配置文件，用于配置Logstash。
  - **建议**：确保配置文件正确无误，并测试Logstash的功能。

### docs/dev-ops/mysql/my.cnf
- **新的MySQL配置文件**：添加了新的MySQL配置文件，用于配置MySQL。
  - **建议**：确保配置文件正确无误，并测试MySQL的功能。

### docs/dev-ops/mysql/sql/init.sql
- **新的MySQL初始化脚本**：添加了新的MySQL初始化脚本，用于创建用户和权限。
  - **建议**：确保脚本正确无误，并测试MySQL数据库的初始化过程。