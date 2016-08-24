# JiawaDoc
家瓦接口文档

***

## 1.用户登录

**URL:**
http://192.168.1.54/DEMO/demo/login.php

**HTTP请求方式**
POST

**请求参数**

{"username":"8990","password":"******"}

**请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| username | String    | 用户账号  |
| password | String    | 登录密码  |

**返回结果**

{"code":"400","info":"失败","data":""}  <br />

{"code":"200","info":"成功",
  "data":{"id":"139","username":"8990","nickname":"俞妃","password":"757575","phone":"15358106068","wx_openid":"o78U2v6Zh5RtUjIJwKPZFYYKMWnI","status":"100","createtime":"2015-09-2701:21:34","headImg":"http://wx.qlogo.cn/mmopen/ajNVdqHZLLAq8171DGiaEfaHdPDetF5XavppaYOicZ7r1mPHNhnkVlZfw4pcsLdAEkjwWsSjJvPuVXoA6rAHEHibw/0",
  "area":"","credit":"1","lasttime":"2016-05-30 12:52:27","num":"50","auth_key":null,"updated_at":null,"email":"null"}
}

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败     |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息  |
| id         | int       | 用户id |
| username   | String    | 用户名 |
| nickname   | String    | 用户昵称  |
| password   | String    | 用户密码  |
| phone      | String    | 手机号  |
| wx_openid  | String    |微信openid  |
| status     | int       | 状态 0：屏蔽 1：正常  |
| createtime | String    | 创建时间  |
| headImg    | String    | 头像 目前默认为微信头像  |
| area       | String    | 用户所在地  |
| credit     | int       | 用户积分  |
| lasttime   | String    | 上次登录时间  |
| num        | int       | ""  |
| auth_key   | String    | 登录密码  |
| updated_at | String    | 更新时间  |
| email      | String    | 邮箱  |

***
## 2.首页Banner

**URL:**

http://192.168.1.54/DEMO/demo/index_banner.php

**HTTP请求方式**

POST

**请求参数**

{"status":"1"}

**请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| status   | String    |  暂无     |

**返回结果**

        {
          "code": "200",
          "info": "success",
          "data": [
            {
            "id": "27",
            "type": "1",
            "imgurl": "http://www.jvawa.com/uploads/1461914226.jpg",
            "href": "productDetical.php?id=3234",
            "sort": "-1",
            "status": "1",
            "createtime": "2016-04-29 15:19:01"
            },
            {
            "id": "29",
            "type": "1",
            "imgurl": "http://www.jvawa.com/uploads/1464942882.jpg",
            "href": "http://www.jvawa.com/new/game/AprilSpecial/special.php",
            "sort": "1",
            "status": "1",
            "createtime": "2016-06-03 16:22:32"
            },
            {
            "id": "30",
            "type": "1",
            "imgurl": "http://www.jvawa.com/uploads/1466997596.png",
            "href": "peijianDetical.php?id=3475",
            "sort": "-1",
            "status": "1",
            "createtime": "2016-06-27 11:04:31"
            }
          ]
        }















