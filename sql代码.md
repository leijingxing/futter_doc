## sql代码

#### 1.sql查询

```sql
#查询所有
select *
from table # 查询指定字段
select id, name
from table # 查询指定字段并去重
select distinct id, name
from table # 查询指定字段并去重
select distinct id, name
from table
```

#### 2.sql条件查询

```sql
#查询id为1的数据
select *
from table
where id = 1 # 查询id为1或2的数据
select *
from table
where id = 1
   or id = 2 # 查询id为1或2或3的数据
select *
from table
where id in (1, 2, 3) # 查询id为1到3的数据
select *
from table
where id between 1 and 3
```

#### 3.sql排序查询

```sql
#
查询id为1的数据并按照id排序
select *
from table
where id = 1
order by id # 查询id为1的数据并按照id倒序排序
select *
from table
where id = 1
order by id desc
```

#### 4.sql分组查询

```sql
#
查询id为1的数据并按照id分组
select *
from table
where id = 1
group by id # 查询id为1的数据并按照id分组并按照id排序
select *
from table
where id = 1
group by id
order by id
```

#### 5.sql分页查询

```sql
#
查询id为1的数据并按照id分组并按照id排序并分页
select *
from table
where id = 1
group by id
order by id limit 0, 10
```

#### 6.sql聚合函数

```sql
#
查询id为1的数据并按照id分组并按照id排序并分页并求和
select sum(id)
from table
where id = 1
group by id
order by id limit 0, 10
# 查询id为1的数据并按照id分组并按照id排序并分页并求平均值
select avg(id)
from table
where id = 1
group by id
order by id limit 0, 10
# 查询id为1的数据并按照id分组并按照id排序并分页并求最大值
select max(id)
from table
where id = 1
group by id
order by id limit 0, 10
# 查询id为1的数据并按照id分组并按照id排序并分页并求最小值
select min(id)
from table
where id = 1
group by id
order by id limit 0, 10
# 查询id为1的数据并按照id分组并按照id排序并分页并求个数
select count(id)
from table
where id = 1
group by id
order by id limit 0, 10
```

#### sql查询user表中姓名为傻逼的数据

```sql
    select *
    from user
    where name = '傻逼'
```
