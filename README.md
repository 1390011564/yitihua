

- 首页使用freemarker完全静态化处理，减轻服务器和数据库的压力

- 后台相关js只在第一次登录时加载，各功能网页通过ajax load到content div中，包括异步前后台表单验证，所有的请求都是通过ajax来完成。

- 批量删除功能，查询、新增、修改全部在一个网页当中，减少与服务器交互

- 对datatables进行封装，增删改查基本的操作封装成插件，降低开发难度

- 严格的代码规范，对于每个类都有对应的单元测试覆盖

## 模块介绍

1. wetech-parent

>   是所有子模块的父类，同时也是项目聚合器，以及版本申明管理，无实质代码

2. wetech-basic-common

主要是放一些通用工具类

3. wetech-basic-hibernate

>   对hibernate进行封装，目前就放了IBaseDao和BaseDao

4. wetech-core

>   项目核心模块，用来放POJO、DAO对象，以及ORM映射

5. wetech-topic

>   服务层文章相关

7. wetech-user

>   服务层用户相关

6. wetech-web

>   用来放前台页面，以及控制层相关代码

## 本地部署

- 通过git下载源码
- 创建数据库wetech_cms，数据库编码为UTF-8
- 执行docs/sql/init.sql文件，初始化数据
- 修改wetech-core模块下jdbc.properties文件，更改MySQL账号和密码
- 在项目根模块执行【mvn clean package】
- 在wetech-core模块执行【mvn jetty:run】命令，即可运行项目
- 项目访问路径：http://localhost:8888/wetech-cms
- 账号密码：admin/123456



