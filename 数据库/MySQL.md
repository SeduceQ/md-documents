# InnoDB和MyISAM的区别

- MyISAM只有表级锁，MySQL有表级锁和行级锁
- InnoDB支持事物和崩溃后的安全恢复
- InnoDB支持外键
- InnoDB支持MVCC

# 事物

> 逻辑上的一组操作，要么都执行，要么都不执行

# 事物四大特性

1. 原子性
2. 一致性
3. 隔离性
4. 持久性

# 并发事物可能带来的问题

- 脏读
- 丢失修改
- 不可重复读
- 幻读

# MySQL事务隔离级别

- READ-UNCOMMITTED 读取未提交
- READ-COMMITTED 读取已提交
- REPEATABLE-READ 可重复读
- SERIALIZABLE 可串行化

# MySQL默认隔离级别

REPEATABLE-READ