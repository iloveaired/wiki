
## mysql log 계정 생성
#### 사용자 추가
```
mysql> use mysql;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> select host,user, password from user;
+-----------+-----------+-------------------------------------------+
| host      | user      | password                                  |
+-----------+-----------+-------------------------------------------+
| localhost | root      | *1CFF261F9DD6BB4599727C6F01C346659D7D1BE3 |
| 127.0.0.1 | root      | *1CFF261F9DD6BB4599727C6F01C346659D7D1BE3 |
| ::1       | root      | *1CFF261F9DD6BB4599727C6F01C346659D7D1BE3 |
| 210.92.%  | root      | *1CFF261F9DD6BB4599727C6F01C346659D7D1BE3 |
| localhost | wordpress | *C260A4F79FA905AF65142FFE0B9A14FE0E1519CC |
+-----------+-----------+-------------------------------------------+
5 rows in set (0.00 sec)

mysql> create user log@localhost  identified by  'log';
Query OK, 0 rows affected (0.01 sec)
mysql> flush privileges;
Query OK, 0 rows affected (0.00 sec)

mysql> create database log;
```
##### 특정아이피 허용
```
mysql> use mysql;
Database changed
mysql>  INSERT INTO mysql.user (host,user,password) VALUES ('210.92.%','log',password('log'));
Query OK, 1 row affected, 3 warnings (0.00 sec)

mysql> GRANT ALL PRIVILEGES ON *.* TO 'log'@'210.92.%';
Query OK, 0 rows affected (0.00 sec)

mysql> flush privileges;
Query OK, 0 rows affected (0.00 sec)

```
#### 테이블 스키마
```
CREATE TABLE `log12` (
  `_LOGFILE` CHAR(11) NOT NULL,
  `_LOGSEQ` INT(10) UNSIGNED NOT NULL,
  `_LOGDATE` DATETIME NOT NULL,
  `_LEVEL` CHAR(1) NOT NULL,
  `_IDENT` CHAR(32) DEFAULT NULL,
  `_SERVER_NAME` VARCHAR(50) DEFAULT NULL,
  `_SCRIPT_NAME` VARCHAR(100) DEFAULT NULL,
  `_QUERY_STRING` VARCHAR(255) DEFAULT NULL,
  `_SERVER_ADDR` INT(10) UNSIGNED DEFAULT NULL,
  `_REMOTE_ADDR` INT(10) UNSIGNED DEFAULT NULL,
  `TITLE` VARCHAR(20) DEFAULT NULL,
  `MSG` VARCHAR(255) DEFAULT NULL,
  `IDX1` VARCHAR(100) DEFAULT NULL,
  `IDX2` VARCHAR(100) DEFAULT NULL,
  `IDX3` VARCHAR(100) DEFAULT NULL,
  `IDX4` VARCHAR(100) DEFAULT NULL,
  `IDX5` VARCHAR(100) DEFAULT NULL,
  `ETC` TEXT,
  PRIMARY KEY  (`_LOGFILE`,`_LOGSEQ`),
  KEY `IDX_LOGDATE` (`_LOGDATE`),
  KEY `IDX_SERVER_NAME_LOGDATE` (`_SERVER_NAME`,`_LOGDATE`),
  KEY `IDX_IDX1` (`IDX1`),
  KEY `IDX_IDX2` (`IDX2`),
  KEY `IDX_REMOTE_ADDR` (`_REMOTE_ADDR`),
  KEY `IDX_TITLE` (`TITLE`)
) ENGINE=MYISAM DEFAULT CHARSET=euckr

```

