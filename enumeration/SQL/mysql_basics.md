Extremely common open implementation of SQL. Very often misconfigured or vulnerable.

Common port 3306

commands

DON'T FORGET SEMI COLON

mysql -h < ip address > -u < username
-h host
-u username

login

show database

use database

show tables

select load_file ("file/name");


QUERY CHEATSHEETS:

https://learnsql.com/blog/sql-basics-cheat-sheet/

https://www.w3schools.com/sql/sql_quickref.asp

If you want to skip queries you can use tools like msfconsole

auxiliary/scanner/mysql/mysql_writable_dirs ( finds writable directories )

auxuliary/scanner/mysql/hashdump ( dumps user hashes )

nmap scripts

--script=mysql-empty-password

--script=mysql-info

--script=mysql-users --script-args="mysql-user='root',mysqlpass='password'"

--script=mysql-databases --script-args="mysql-user='root',mysqlpass='password'"

--script=mysql-variables --script-args="mysql-user='root',mysqlpass='password'"

--script=mysql-audit --script-args="mysqlaudit.username='root',mysqlpass='password',mysqlaudit.filename='/usr/share/nselib/data/mysql-cis.audit'"

--script=mysql-dump-hashes --script-args="mysql-username='root',mysqlpass='password'"

--script=mysql-query --script-args="query='select * from table',mysql-username='root',mysqlpass='password'"

