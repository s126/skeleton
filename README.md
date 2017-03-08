# 参考步骤


## 在数据库中，创建用户和表

1. 打开 CMD 窗口，按照要求创建用户(`grant dba to vip identified by vip;`)
2. 创建 .sql 文件，编写相关建表语句
3. 将 sql 文件在 sqlplus 执行


## 创建 Eclipse 项目

1. 打开 eclipse，创建动态 Web 项目
2. 将 skeleton 中的 src, WebContent 文件夹覆盖到创建的 Web 项目中
3. 修改项目名字、数据库的用户名密码、spring 的扫描路径


## 实现项目

1. 创建 Entity 类。(注意，到时候，如果考试要求用 xml 的方式配置，那么。。。)
2. 创建 DAO 类，可以选择继承 BaseDao
3. 创建 Service 类 (注意 @Transactional)
4. 创建 Action 类 (注意 @Scope，还有异常处理)
5. 创建 Jsp 文件
6. 在 struts.xml 配置映射


# 注意事项

1. 代码要规范
2. 要有异常处理
3. 要有一定注释
4. 一定要有数据库的 sql 文件


# 常见错误

## ClassNotFoundException

可能原因：
1. Jar 包缺失
2. Jar 包没有配正确

解决方案：
1. 自己将缺失的 Jar 包加进去，或者重新配置
2. 老老实实把这个工程 lib 文件夹下的 jar 包拷贝到你的项目中！！！【强烈建议】


## NullPointerException

这是空指针异常。意思是，有些参数没有赋值成功，所以是 null.


解决方案：
检查为什么没有赋值成功，更改之！


## More than one table found in namespace (,): ...

原因：
在不同用户下存在相同名字的表，hibernate 解析出错。

解决方案：
强烈建议在定义实体类的时候，指定相应命名空间（也就是数据库的用户名）：

```
@Entity
@Table(catalog = "xiaomi")
public class Person {...}

```



## 各种 404 错误

原因不详，但基本都是 struts.xml 配置问题

解决方案：
1. 检查你请求的 url 是不是写错了，如果粗了，更正
2. 检查你的 action 是不是配对了。尤其注意，action 中的 class 要首字母小写！
3. 其他，待补充。


