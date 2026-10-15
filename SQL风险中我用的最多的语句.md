# SQL风险中我用的最多的语句

以domains表为例子

```Plain Text
- 查看索引基本信息
SHOW INDEX FROM domains;

-- 查看表结构（含字段、类型，但不含索引详情）
DESC domains;

-- 查看完整建表语句（含所有索引定义）
SHOW CREATE TABLE domains;
```



创建索引

```Plain Text
ALTER TABLE 表名 ADD INDEX 索引名 (字段名)
```



```Plain Text
CREATE INDEX 索引名 ON 表名 (字段名)
```



更新统计信息

```Plain Text
-- 更新单表统计信息
ANALYZE TABLE domains;
```



```Plain Text
-- 删除索引
ALTER TABLE domains DROP INDEX idx_name;
```