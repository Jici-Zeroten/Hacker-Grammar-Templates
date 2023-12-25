# Google-Dorks-Templates

这是一份Google Dorks的列表，基于原项目[google-dorks-bug-bounty](https://github.com/TakSec/google-dorks-bug-bounty/)的二开，进行了汉化并增加更多语法。

在线网址：https://jici-zeroten.github.io/Google-Dorks-Templates/

---

### 广域搜索（排除指定关键词）

> site:example.com -www -shop -share -ir -mfa

### PHP站点且带参数

> site:example.com ext:php inurl:?

### Disclosed XSS and Open Redirects

> site:openbugbounty.org inurl:reports intext:"example.com"

### 敏感文件扩展名披露

> site:"example[.]com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

### XSS 倾向性参数

> inurl:q= | inurl:s= | inurl:search= | inurl:query= | inurl:keyword= | inurl:lang= inurl:& site:example.com

### Open Redirect prone parameters

> inurl:url= | inurl:return= | inurl:next= | inurl:redirect= | inurl:redir= | inurl:ret= | inurl:r2= | inurl:page= inurl:& inurl:http site:example.com

### SQLi 倾向性参数

> inurl:id= | inurl:pid= | inurl:category= | inurl:cat= | inurl:action= | inurl:sid= | inurl:dir= inurl:& site:example.com

### SSRF 倾向性参数

> inurl:http | inurl:url= | inurl:path= | inurl:dest= | inurl:html= | inurl:data= | inurl:domain=  | inurl:page= inurl:& site:example.com

### LFI（本地文件包含）倾向性参数

> inurl:include | inurl:dir | inurl:detail= | inurl:file= | inurl:folder= | inurl:inc= | inurl:locate= | inurl:doc= | inurl:conf= inurl:& site:example.com

### RCE 倾向性参数

> inurl:cmd | inurl:exec= | inurl:query= | inurl:code= | inurl:do= | inurl:run= | inurl:read=  | inurl:ping= inurl:& site:example.com

### High % inurl keywords

> inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example[.]com

### Sensitive Parameters

> inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:example[.]com

### API文档搜索

> inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer site:"example[.]com"

### Code Leaks

> site:pastebin.com "example.com"

> site:jsfiddle.net "example.com"

> site:codebeautify.org "example.com"

> site:codepen.io "example.com"

### Cloud Storage

> site:s3.amazonaws.com "example.com"

> site:blob.core.windows.net "example.com"

> site:googleapis.com "example.com"

> site:drive.google.com "example.com"

> site:dev.azure.com "example[.]com"

> site:onedrive.live.com "example[.]com"

> site:digitaloceanspaces.com "example[.]com"

> site:sharepoint.com "example[.]com"

> site:s3-external-1.amazonaws.com "example[.]com"

> site:s3.dualstack.us-east-1.amazonaws.com "example[.]com"

> site:dropbox.com/s "example[.]com"

> site:box.com/s "example[.]com"

> site:docs.google.com inurl:"/d/" "example[.]com"

### JFrog Artifactory

> site:jfrog.io "example[.]com"

### Firebase

> site:firebaseio.com "example[.]com"

### 漏洞报告查询与漏洞提交

> "submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"

> site:example[.]com "bounty"
### Apache服务器状态暴露

> site:example[.]com inurl:/server-status "apache"

### WordPress

> site:example[.]com inurl:/wp-admin/admin-ajax.php

### Drupal

> site:example[.]com intext:"Powered by" & intext:Drupal & inurl:user

### Joomla

> site:example[.]com inurl:/joomla/login
### 文件上传（File upload endpoints）

> site:example[.]com & intext:"choose file"

> site:example[.]com & intext:"选择文件"

> site:example[.]com "choose file"
