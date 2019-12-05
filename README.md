# mini3

mini3 project




import MySQLdb


db = MySQLdb.connect("localhost", "testuser", "test123", "TESTDB", charset='utf8' )
 
cursor = db.cursor()

cursor.execute("DROP TABLE IF EXISTS EMPLOYEE")

sql = """CREATE TABLE EMPLOYEE (
         FIRST_NAME  CHAR(20) NOT NULL,
         LAST_NAME  CHAR(20),
         AGE INT,  
         SEX CHAR(1),
         INCOME FLOAT )"""

cursor.execute(sql)

db.close()
