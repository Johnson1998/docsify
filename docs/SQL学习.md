# SQL学习

## MYSQL语句练习笔记

### day1

​		leetcode  sql 184题

>子查询前置基础知识补充：
>
>按返回的结果集区分子查询： 1、变量子查询 那些只返回一个单一值的子查询称之为标量子查询，比如这样： SELECT * FROM t1 WHERE m1 = (SELECT MIN(m2) FROM t2);
>
>2、行子查询 就是返回一条记录的子查询，不过这条记录需要包含多个列（只包含一个列就成了标量子查询了）。比如这样： SELECT * FROM t1 WHERE (m1, n1) = (SELECT m2, n2 FROM t2 LIMIT 1);
>
>3、列子查询 列子查询自然就是查询出一个列的数据喽，不过这个列的数据需要包含多条记录（只包含一条记录就成了标量子查询了）。比如这样 SELECT * FROM t1 WHERE m1 IN (SELECT m2 FROM t2);
>
>4、表子查询（也就是本答案） SELECT * FROM t1 WHERE (m1, n1) IN (SELECT m2, n2 FROM t2);   其中的(SELECT m2, n2 FROM t2)就是一个表子查询，这里需要和行子查询对比一下，行子查询中我们用了LIMIT 1来保证子查询的结果只有一条记录，表子查询中不需要这个限制。
>
>以上来自于 《从根上理解MySQL》14章，感兴趣的同学可以去看

leetcode  sql 182题 [查找重复的电子邮箱](https://leetcode.cn/problems/duplicate-emails/)

>使用group by和having。还需要记得优先顺序。where>group by>having>order by

