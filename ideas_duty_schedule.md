## 值班安排
---
* 在excel里生成数据： 
  > { id,
      name,
      tel,
      duty_date,
    }
* 利用python将xlr导入sqlite;
  > { 创建表：
        id int,
        name text,
        tel int,
        duty_date text
    }

---
### python知识点
> * xlrd库知识点：
    { xlrd.open_workbook, ` 打开excel表;`
      sheet_by_name,   ·` 按照sheet名字读取;`
      sheet.row_value, ·` 获取表一行值;`
      sheet.col_value, ·` 获取表一列值;`
      xlrd.xldate.xldate_as_datetime(x, 0),·` x为xlrd读取日期整数值;`
    }
    参考: [使用xlrd](http://www.cnblogs.com/lhj588/archive/2012/01/06/2314181.html)
> * datetime库知识点
    { datetime.date.strftime('%Y-%m-%d'），·` 将xlrd读取的日期整数值转换为字符串；`
    `例如： date1 = xlrd.xldate.xldate_as_datetime(42429,0）
    	   date1.strftime('%Y-%m-%d'）
    	   '2016-02-29'`
    }
    参考：[datetime使用](http://blog.csdn.net/zithan/article/details/6719397)
> * sqlite库知识点
    {conn = sqlite3.connect('test.db')·` 创建或连接数据库；`
     conn.execute('''CREATE TABLE DUTY_SCHEDULE  ·` 创建一个数据库表；`
       (ID INT PRIMARY KEY     NOT NULL,
       NAME           TEXT    NOT NULL,
       TEL            INT     NOT NULL,
       DUTY_DATE      TEXT);''')
     conn.executemany('INSERT INTO stocks VALUES (?,?,?,?,?)', purchases)·` purchases is a seq;`
     conn.commit()
     conn.close() 
    }
    参考：[sqlite3使用](http://www.tutorialspoint.com/sqlite/sqlite_python.htm)
> * jinja2库知识点
    {
    	
    }