We are using this for MSSQL

--script=ms-sql-info

--script=ms-sql-ntlm-info --script-args=mssql.instance=port=1433

--script=ms-sql-brute --script-args userdb=file,passdb=file

--script=ms-sql-empty-password

--script=ms-sql-query --script-args mssql.username=user,mssql.password=pass,ms-sql-query.query="SELECT * FROM QUERY

--script=ms-sql-dump-hashes --script-args=mssql.username=user,mssql.password=pass

--script=ms-sql-xp-cmdshell --script-args mssql.username=user,mssql.password=pass,ms-sql-xp-cmdshell.cmd=
