# MySQL 技术

## 读写分离


- 初始化数据
.\bin\mysqld --initialize-insecure --datadir=data  --console
.\bin\mysqld --initialize-insecure --datadir=data1 --console
.\bin\mysqld --initialize-insecure --datadir=data2 --console

- 启动数据库实例
.\bin\mysqld  --defaults-file=config\master.cnf --console
.\bin\mysqld  --defaults-file=config\mysql1.cnf --console
.\bin\mysqld  --defaults-file=config\mysql2.cnf --console



GRANT REPLICATION SLAVE ON *.* TO 'mysql1'@'localhost' IDENTIFIED BY '123456';
FLUSH PRIVILEGES;


- 异步复制配置

change master to master_host='localhost',master_port=3306,master_user='mysql1',master_password='123456',master_log_file='mysql-bin.000001',master_log_pos=747;