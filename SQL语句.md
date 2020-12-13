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
   
   count(distinct 字段名称) 字段名称 将根据字段名统计
   
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
   
   查询分页
   seelect * from 表名称 limit 从第几个元素查找,返回几个元素
   
   查询分组
   select 需要分组的字段名称 count(*) as 别名 from 表名称 group by 需要分组的字段名称
   
   通过字段查询分组 排序 降序
   select goods_id, sum(goods_num * goods_price) as 别名 from "order" group by 需要分组字段名称 order by 别名 desc
   
   通过给定字段连接其他表查询 join 默认为内连接 取两表之交集
   select 当前表.关联外表字段1, 当前表.关联外表字段2, 外表.关联字段1 from 当前表 
   join 外表 on 当前表.关联外表字段1 = 外表.关联外表字段1(内外表关系字段) 
   
   通过给定字段连接其他表查询 left join 取左表存在 不在乎右表是否存在
   select 当前表.关联外表字段1, 当前表.关联外表字段2, 外表.关联字段1 from 当前表 
   join 外表 on 当前表.关联外表字段1 = 外表.关联外表字段1(内外表关系字段) 
   
   通过给定字段连接其他表查询 right join 与left join 反之
   select 当前表.关联外表字段1, 当前表.关联外表字段2, 外表.关联字段1 from 当前表 
   join 外表 on 当前表.关联外表字段1 = 外表.关联外表字段1(内外表关系字段) 
   
   关联三张表
   select 当前表.关联外表字段1, 当前表.关联外表字段2, 外表1.关联字段1 from 当前表 
   join 外表1 on 当前表.关联外表字段1 = 外表1.关联外表字段1(内外表关系字段) 
   join 外表2 on 当前表.关联外表字段1 = 外表2.关联外表字段1
   where 外表2.字段 = 给定字段
   
   
   增加列
   alter table 表名称 add 字段名 tinyint not null default 0
   
   软删除id为 ? 的数据 同时插入更新时间
   update user set status = 0,update_at = now() where id = ?
   
   查询一行某字段不为null
   select * from user where update_at is not null
   
   sql函数
   now() 获取当前时间 yyyy-mm-dd hh-ss   
   
   count() 获取查询出符合条件的记录数量 select count(*) from user where update_at is not null
   
   sum(num * num) 求和
   
   
   
```
