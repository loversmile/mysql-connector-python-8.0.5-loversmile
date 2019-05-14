
add class MysqlRow and class MySQLCursorMysqlRow

example

#!/usr/bin/env python
# coding=utf-8

import mylib.mysql.connector as mysql
#from ucmrow import *

conn = mysql.connect(host='localhost', user='root',passwd='admin',db='ucm_config',charset='utf8')

c = conn.cursor(mysqlrow=True)

c.execute("SELECT name,age FROM student;")

for row in c.fetchall():
    print row[1]
    print row["name"]
