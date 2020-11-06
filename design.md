## 前台

<br/>

用户表 TCustomer

|字段名称|字段|类型|备注|
|-------|----|----|----|
|用户ID|u_id|int|pk，not null|
|登录账号|login_name|varchar(64)|not null|
|登录密码|password|varchar(64)|not null|
|用户姓名|username|varchar(64)|not null|
|手机号|telenumber|varchar(20)|...|
|电子邮箱|email|varchar(64)|...|
|注册时间|reg_time|datetime|not null|
|登陆时间|login_time|datetime|...|
|上次登录时间|last_login_time|datetime|...|
|登录次数|count|int|not null|

<br/>

报销业务表 TBusiness

|字段名称|字段|类型|备注|
|-------|----|----|----|
|记录标识|b_id|int|pk,not null|
|创建时间|gen_time|datetime|not null|
|上传时间|upload_time|datetime|...|
|上次上传时间|last_upload_time|datetime|...|
|业务状态|state|int|not null|
|文件路径|path|????|not null|
|二维码|qrcode|varchar(200)|...|
|用户ID|u_id|int|fk，not null|




------
<br/>

## 后台

<br/>

用户表 TUser

|字段名称|字段|类型|备注|
|-------|----|----|----|
|用户ID|u_id|int|pk，not null|
|登录账号|login_name|varchar(64)|not null|
|登录密码|password|varchar(64)|not null|
|用户姓名|username|varchar(64)|not null|
|手机号|telenumber|varchar(20)|...|
|电子邮箱|email|varchar(64)|...|
|创建时间|gen_time|datetime|not null|
|登陆时间|login_time|datetime|...|
|上次登录时间|last_login_time|datetime|...|
|登录次数|count|int|not null|

<br/>

角色表 TRole  

|字段名称|字段|类型|备注|
|-------|----|----|----|
|角色ID|r_id|int|pk,not null|
|父角色|parent_r_id|int|not null|
|角色名称|role_name|varchar(64)|not null|
|创建时间|gen_time|datetime|not null|
|角色描述|description|varchar(200)|...|

<br/>

权限表 TRight

|字段名称|字段|类型|备注|
|-------|----|----|----|
|权限ID|ri_id|int|pk,not null|
|父权限|parent_ri_id|int|not null|
|权限名称|right_id|varchar(64)|not null|
|权限描述|description|varchar(200)|not null|

<br/>

用户角色表 TUserRoleRelation

|字段名称|字段|类型|备注|
|-------|----|----|----|
|记录标识|ur_id|int|pk,not null|
|用户|u_id|int|fk,not null|
|角色|r_id|int|fk,not null|
|创建时间|gen_time|datetime|not null|

<br/>

角色权限表 TRoleRightRelation

|字段名称|字段|类型|备注|
|-------|----|----|----|
|记录标识|ur_id|int|pk,not null|
|角色|r_id|int|fk,not null|
|权限|ri_id|int|fk,not null|
|创建时间|gen_time|datetime|not null|



-----
<br/>

## URL

客户 customer
- /login
- /register
- /account
    - /home
    - /security
- /u_id
    - /b_id
        > /add  
        > /qrcode
    - /business
    - /datetime
     










