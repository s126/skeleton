# 参考步骤


## 在数据库中，创建用户和表

1. 打开 CMD 窗口，按照要求创建用户(`grant dba to vip identified by vip;`)
2. 创建 .sql 文件，编写相关建表语句
3. 将 sql 文件在 sqlplus 执行


## 创建 Eclipse 项目

1. 打开 eclipse，创建动态 Web 项目
2. 将 skeleton 中的 src/WebContent 文件夹覆盖创建的 Web 项目中
3. 修改项目名字、数据库的用户名密码、spring 的扫描路径


## 实现项目

1. 创建 Entity 类
2. 创建 DAO 类
3. 创建 Service 类 (注意 @Transactional)
4. 创建 Action 类 (注意 @Scope，还有异常处理)
5. 创建 Jsp 文件
6. 在 struts.xml 配置映射


# 注意事项

1. 代码要规范
2. 要有异常处理
3. 要有一定注释
4. 一定要有数据库的 sql 文件