mysql 5.7 이상인 경우 패스워드 초기화

````sql
UPDATE mysql.user
    set authentication_string=PASSWORD("password"),
    password_expired='N',
    plugin='mysql_native_password'
where User='root';
````
