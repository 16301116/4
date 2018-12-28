# 4
![Image text](https://github.com/16301116/4/blob/master/1.png)  
![Image text](https://github.com/16301116/4/blob/master/2.png)  
![Image text](https://github.com/16301116/4/blob/master/3.jpg)  
Room其实就是一个orm，抽象了SQLite的使用，原生支持LiveData和Rxjava嵌套使用。  
Room有3个主要组件  
Database ：数据库  
Entity : 代表数据库一个表结构  
Dao : 包含访问数据库的方法  
这次作业主要对老师给的sample进行了模仿  
我也在网上查阅了相关的资料和官方给出的ROOM API的使用方法。
当一个类用@Entity注解并且被@Database注解中的entities属性所引用，Room就会在数据库中为那个entity创建一张表。  

Room默认把类名作为数据库的表名。如果你想用其它的名称，使用@Entity注解的tableName属性。  

默认Room会为entity中定义的每一个field都创建一个column。和tableName属性类似，Room默认把field名称作为数据库表的column名。如果你想让column有不一样的名称，为field添加@ColumnInfo属性。如果一个entity中有你不想持久化的field，那么你可以使用@Ignore来注释它们。  

要持久化一个field，Room必须有获取它的渠道。你可以把field写成public，也可以为它提供一个setter和getter。如果你使用setter和getter的方式，记住它们要基于Room的Java Bean规范。  

每个entity必须至少定义一个field作为主键（primary key）。即使只有一个field，你也必须用@PrimaryKey注释这个field。如果你想让Room为entity设置自增ID，你可以设置@PrimaryKey的autoGenerate属性。如果你的entity有一个组合主键，你可以使用@Entity注解的primaryKeys属性。  
