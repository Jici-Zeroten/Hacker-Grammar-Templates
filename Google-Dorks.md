# Google-Dorks-Templates

### 子域名搜索（使用 *.主域 指定 ）

> site:example.com

> site:example.com -www -shop -share -ir -mfa

### PHP站点

> site:example.com ext:php inurl:?

> site:example.com ext:php intitle:phpinfo "published by the PHP Group"

> site:example.com inurl:php?=id1 | inurl:index.php?id= | inurl:pageid= | inurl:.php?

### Disclosed XSS and Open Redirects

> site:openbugbounty.org inurl:reports intext:"example.com"

### 敏感文件披露（凭据文件、日志文件、备份文件等）

> site:"example.com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

> site:example.com "password" filetype:doc | filetype:pdf | filetype:docx | filetype:xls | filetype:dat | filetype:log

> site:example.com ext:xml | ext:conf | ext:cnf | ext:reg | ext:inf | ext:rdp | ext:cfg | ext:txt | ext:ora | ext:ini | ext:log

> site:example.com ext:bkf | ext:bkp | ext:bak | ext:old | ext:backup

> site:example.com intext:"TARGET" & ext:txt | ext:sql | ext:cnf | ext:config | ext:log & intext:"admin" | intext:"root" | intext:"administrator" & intext:"password" | intext:"root" | intext:"admin" | intext:"administrator"

### XSS 倾向性参数

> inurl:q= | inurl:s= | inurl:search= | inurl:query= | inurl:keyword= | inurl:lang= inurl:& site:example.com

### Open Redirect 倾向性参数（开放式重定向）

> inurl:url= | inurl:return= | inurl:next= | inurl:redirect= | inurl:redir= | inurl:ret= | inurl:r2= | inurl:page= inurl:& inurl:http site:example.com

> site:example.com inurl:redir | inurl:url | inurl:redirect | inurl:return | inurl:src=http | inurl:r=http

> site:example.com inurl:return_to

![image-20231225232830312](Google-Dorks/image-20231225232830312.png)

### SQLi 倾向性参数

> inurl:id= | inurl:pid= | inurl:category= | inurl:cat= | inurl:action= | inurl:sid= | inurl:dir= inurl:& site:example.com

> site:example.com inurl:php?id=

> site:example.com inurl:asp?id=

> site:example.com inurl:aspx?id=

> site:example.com inurl:list.php?id=

> site:example.com intext:"sql syntax near" |  intext:"incorrect syntax near"

注：参数不一定要是id，也可以是pid、tid、keyword之类的其它参数

### SSRF 倾向性参数

> inurl:http | inurl:url= | inurl:path= | inurl:dest= | inurl:html= | inurl:data= | inurl:domain=  | inurl:page= inurl:& site:example.com

### LFI（本地文件包含）倾向性参数

> inurl:include | inurl:dir | inurl:detail= | inurl:file= | inurl:folder= | inurl:inc= | inurl:locate= | inurl:doc= | inurl:conf= inurl:& site:example.com

### RCE 倾向性参数

> inurl:cmd | inurl:exec= | inurl:query= | inurl:code= | inurl:do= | inurl:run= | inurl:read=  | inurl:ping= inurl:& site:example.com

### 敏感目录

> inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example.com

### 敏感参数（Sensitive Parameters）

> inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:example.com

### API文档搜索

> inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer site:"example.com"

### 云存储（Cloud Storage）

> site:s3.amazonaws.com "example.com"

> site:blob.core.windows.net "example.com"

> site:googleapis.com "example.com"

> site:drive.google.com "example.com"

> site:dev.azure.com "example.com"

> site:onedrive.live.com "example.com"

> site:digitaloceanspaces.com "example.com"

> site:sharepoint.com "example.com"

> site:s3-external-1.amazonaws.com "example.com"

> site:s3.dualstack.us-east-1.amazonaws.com "example.com"

> site:dropbox.com/s "example.com"

> site:box.com/s "example.com"

> site:docs.google.com inurl:"/d/" "example.com"

### AWS 访问密钥（AWS Access Keys）

> site:example.com filetype:pem intext:PRIVATE KEY

### JFrog Artifactory

> site:jfrog.io "example.com"

### Firebase

> site:firebaseio.com "example.com"

### 漏洞报告查询与漏洞提交

> "submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"

> site:example.com "bounty"
### Apache服务器状态暴露

> site:example.com inurl:/server-status "apache"

### WordPress

> site:example.com inurl:/wp-admin

> site:example.com inurl:/wp-login.php

> site:example.com inurl:"_wpeprivate"

> site:example.com inurl:wp- | inurl:wp-content | inurl:plugins | inurl:uploads | inurl:themes | inurl:download

### Drupal

> site:example.com intext:"Powered by" & intext:Drupal & inurl:user

### Joomla

> site:example.com inurl:/joomla/login
### 文件上传（File upload endpoints）

> site:example.com & intext:"choose file"

> site:example.com & intext:"选择文件"

> site:example.com "choose file"

### 剑指src

> site:example.com intext:"手册"

> site:example.com intext:"文档"

> site:example.com 学号|学工号

> site:example.com 奖学金|公示

> site:example.com 工号|教职工工号

> site:example.com intext:"忘记密码"

> site:example.com intext:"工号"

> site:example.com intext:"优秀员工"

> site:example.com intext:"身份证号码"

> site:example.com intext:"手机号"

### 数据库相关

> site:example.com intext:"sql syntax near" | intext:"syntax error has occurred" | intext:"incorrect syntax near" | intext:"unexpected end of SQL command" | intext:"Warning: mysql_connect()" | intext:"Warning: mysql_query() | intext:"Warning: pg_connect()" | filetype:sqlext:sql | ext:dbf | ext:mdb

### 登录页面

> site:example.com inurl:login | inurl:signin | intitle:Login | intitle: signin | inurl:auth | intitle:登录

### 赏金项目查找（Bug Bounty Programs，更适用于国外赏金）

> site:example.com inurl:bug inurl:bounty

> site:example.com inurl:security intext:bounty

> site:example.com inurl:security ext:txt

> site:example.com inurl:responsible-disclosure

> site:example.com inurl:/.well-known/security

> site:example.com intext:bug bounty program

> site:example.com intext:responsible disclosure program

> site:example.com intext:vulnerability disclosure program

> site:example.com intext:security rewards

> site:example.com intext:bug bounty payout

> site:example.com inurl:security ext:txt -inurl:hackerone -inurl:bugcrowd -inurl:synack

> site:example.com inurl:responsible-disclosure -inurl:hackerone -inurl:bugcrowd -inurl:synack

> site:example.com intext:bug bounty -inurl:hackerone -inurl:bugcrowd -inurl:synack

> inurl:/security

> responsible disclosure hall of fame

> responsible disclosure europe

> responsible disclosure white hat

> white hat program

> responsible disclosure r=h:nl

> responsible disclosure r=h:uk

> responsible disclosure r=h:eu

> responsible disclosure bounty r=h:nl

> responsible disclosure bounty r=h:uk

> responsible disclosure bounty r=h:eu

> responsible disclosure swag r=h:nl

> responsible disclosure swag r=h:uk

> responsible disclosure swag r=h:eu

> responsible disclosure reward r=h:nl

> responsible disclosure reward r=h:uk

> responsible disclosure reward r=h:eu