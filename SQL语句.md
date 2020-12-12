# Record
编程记录

##常用sql语句

```sql
   
   常用关键字
   primary key 主键 唯一
   
   auto_increment 自增 （通常与主键一起使用）
   
   not null 不可为空
   
   unique 不可重复
   
   default 默认值
   
   order by 排序
   
   asc 升序
   
   desc 降序
   
   and 与操作符
   
   建表
   create table 表名称 
   
   删表
   drop table 表名称
   
   修改表
   alter table 表名称
   
   插入数据
   insert into 表名称(表字段1,表字段2) values(映射对应字段值1,映射对应字段值2);
   
   删除id为 ? 的数据
   delete form 表名称 where id = ?
   
   增加列
   alter table 表名称 add 字段名 tinyint not null default 0
   
   软删除id为 ? 的数据 同时插入更新时间
   update user set status = 0,update_at = now() where id = ?
   
   查询一行某字段不为null
   select * from user where update_at is not null
   
   sql函数
   now() 获取当前时间 yyyy-mm-dd hh-ss   
   
   count() 获取查询出符合条件的记录数量 select count(*) from user where update_at is not null
   
   
   
   
```
