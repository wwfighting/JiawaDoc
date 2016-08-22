# JiawaDoc
家瓦接口文档


1.用户登录

**URL:**
http://192.168.1.54/DEMO/demo/test.php

**HTTP请求方式**
POST

**请求参数**

{"action":"login","username":"8990","password":"******"}

**请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
| ---------|:---------:| ---------:|
| action   | String    | login     |
| username | String    | 用户账号  |
| password | String    | 登录密码  |

**返回结果**

{"code":"400","info":"失败","data":""}
{"code":"200","info":"成功",
  data : {"id":"139","username":"8990","nickname":"俞妃","password":"757575","phone":"15358106068","wx_openid":"o78U2v6Zh5RtUjIJwKPZFYYKMWnI",
  "status":"100","createtime":"2015-09-27 01:21:34","headImg":"http://wx.qlogo.cn/mmopen/ajNVdqHZLLAq8171DGiaEfaHdPDetF5XavppaYOicZ7r1mPHNhnkVlZfw4pcsLdAEkjwWsSjJvPuVXoA6rAHEHibw/0",
  "area":"","credit":"1","lasttime":"2016-05-30 12:52:27","num":"50","auth_key":null,"updated_at":null,"email":"null"}
}

| 返回值字段 | 字段类型  | 字段说明  |
| ---------  |:---------:| ---------:|
| code       | String    | login     |
| info       | String    | 用户账号  |
| id         | String    | 登录密码  |
| username   | String    | 登录密码  |
| nickname        | String    | 登录密码  |
| password        | String    | 登录密码  |
| phone        | String    | 登录密码  |
| wx_openid       | String    | 登录密码  |
| status        | String    | 登录密码  |
| createtime   | String    | 登录密码  |
| headImg | String    | 登录密码  |
| area | String    | 登录密码  |
| credit| String    | 登录密码  |
| lasttime | String    | 登录密码  |
| num | String    | 登录密码  |
| auth_key | String    | 登录密码  |
| updated_at | String    | 登录密码  |
| email | String    | 登录密码  |


















