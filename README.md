# dump-database
dump is export and import data in database from old database to new database.
You can use it with move from dev database to uat or to production

# How to dump and restore database mongodb
# install mongodb tool ()
  # download tool: https://www.mongodb.com/try/download/database-tools
  # how to install and config:  https://www.mongodb.com/docs/database-tools/installation/installation-windows/
  
# how to dump database (export your database)
  1. open terminal
  2. use command:
     mongodump --uri="your database url"
     
# example dump all database from url: 
  C:\Users\ter> mongodump --uri="mongodb+srv://hackter77:%3CZPnaI2z 0bvBrgE4G%3E@cluster0.7xduomn.mongodb.net/"
# example dump single database from url: 
  C:\Users\ter> mongodump --uri="mongodb+srv://hackter77:%3CZPnaI2z0bvBrgE4G%3E@cluster0.7xduomn.mongodb.net/database1"
  
# you can check your database after dump database in the path you use command 
# example my dump: C:\Users\ter\dump\

# how to restore database(import dump data to new database)
# restore all database to new database  from folder dump:
C:\Users\ter> mongodump mongodb+srv://hackter77:%3CZPnaI2z 0bvBrgE4G%3E@cluster0.7xduomn.mongodb.net/ dump\
# restore single database to new database from folder dump\your database: 
C:\Users\ter> mongodump --uri="mongodb+srv://hackter77:%3CZPnaI2z0bvBrgE4G%3E@cluster0.7xduomn.mongodb.net/database2" dump\database1\
