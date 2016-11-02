# JiawaDoc
家瓦接口文档

***

## 1.图片地址说明

返回的图片地址 imgurl 为 "uploads/********.jpg" 形式</br>

客户端需要在前加上"http://www.jvawa.com/" 进行拼接</br>

最终的图片访问地址为 "http://www.jvawa.com/uploads/********.jpg" 形式</br>

例如："http://www.jvawa.com/uploads/1464942882.jpg"

***

## 2.用户登录

* **URL:**

http://192.168.1.54/test/jvawa/login.php

* **HTTP请求方式**

POST

* **请求参数**

        {"username":"15358106068","password":"******"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| username | String    | 手机号    |
| password | String    | 登录密码  |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code":"200",
          "info":"success",
          "data":
            {
            "id":"139",
            "username":"8990",
            "nickname":"俞妃",
            "password":"757575",
            "phone":"15358106068",
            "wx_openid":"o78U2v6Zh5RtUjIJwKPZFYYKMWnI",
            "status":"100",
            "createtime":"2015-09-2701:21:34",                                          "headImg":"http://wx.qlogo.cn/mmopen/ajNVdqHZLLAq8171DGiaEfaHdPDetF5XavppaYOicZ7r1mPHNhnkVlZfw4pcsLdAEkjwWsSjJvPuVXoA6rAHEHibw/0",
            "area":"",
            "credit":"1",
            "lasttime":"2016-05-30 12:52:27",
            "num":"50",
            "auth_key":null,
            "updated_at":null,
            "email":"null"
            }
        }

* **返回字段说明**

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
## 3.首页Banner

* **URL:**

http://192.168.1.54/test/jvawa/index_banner.php

* **HTTP请求方式**

POST

* **请求参数**

        {"status":"1"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| status   | String    |  暂无     |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code": "200",
          "info": "success",
          "data": [
            {
            "id": "27",
            "type": "1",
            "imgurl": "uploads/1461914226.jpg",
            "href": "productDetical.php?id=3234",
            "sort": "-1",
            "status": "1",
            "createtime": "2016-04-29 15:19:01"
            },
            {
            "id": "29",
            "type": "1",
            "imgurl": "uploads/1464942882.jpg",
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

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | int       | bannerid |
| type       | int       | 位置 0 首页 1 |
| title      | String    | 标题 |
| imgurl     | String    | banner广告图片地址 |
| href       | String    | 图片点击跳转地址 |
| sort       | int       | 排序 |
| status     | int       | "" |
| createtime | String    | 创建时间 |

***

## 4.首页商品（新品推荐，热门商品）

* **URL:**

http://192.168.1.54/test/jvawa/index_goods.php

* **HTTP请求方式**

POST

* **请求参数**

        {"isrecom":"1"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| isrecom  | String    |是否推荐，-1：全部 0：不推荐 1：新品推荐 2：热门商品|

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code":"200",
          "info":"success",
          "data":
          [
            {
              "id":"2896",
              "goodsno":"2015CG.01.01.01.001",
              "goodsname":"\u5c0f\u5eb7\u7f8e\u53a8",
              "subtitle":"\u5206\u7c7b",
              "picurl":"uploads/1443078651.jpg;uploads/1443078666.jpg",
              "price":"6999",
              "classifyid":"3",
              "goodsdesc":"",
              "isrecom":"1",
              "buylimit":"6",
              "tag":"\u96d5\u523b\u65f6\u5149A;15,17,18,19,20;4",
              "brandsid":"5",
              "status":"1",
              "createtime":"2015-10-10 17:14:56",
              "updatetime":"2016-03-2408:51:22",
              "ordercount":"18",
              "unit":"\u7c73",
              "recomtype":"0",
              "recomgoods":"",
              "adminid":"1",
              "type":"0",
              "reviewmark":"pass",
              "stock":"22",
              "guige":"3-10\u7c73\u5730\u67dc + 3-10\u7c73\u53f0\u9762 + 1-5\u7c73\u540a\u67dc",
              "price_old":"13996",
              "price1":"24999",
              "price_old1":"49996",
              "standard_fittings_id":"1"
            },
            {
              "id":"2897",
              "goodsno":"2015CG.03.01.01.001",
              "goodsname":"\u7cbe\u82f1\u60a6\u53a8",
              "subtitle":"\u5206\u7c7b",
              "picurl":"uploads/1443142494.jpg;uploads/1443142502.jpg;uploads/1443142512.jpg",
              "price":"10999",
              "classifyid":"5",
              "goodsdesc":"",
              "isrecom":"1",
              "buylimit":"6",
              "tag":"\u8fc8\u68eeB,\u7b80\u7231A,\u4e1d\u4e3d\u5361B,\u4e1d\u4e3d\u5361C,\u7eb8\u724c\u5c4b,\u632a\u5a01\u6d77\u5cb8;15,17,18,19,20;4,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,22,23,80,",
              "brandsid":"5",
              "status":"1",
              "createtime":"2015-10-10 17:16:24",
              "updatetime":"2016-03-24 09:03:34",
              "ordercount":"15",
              "unit":"\u7c73",
              "recomtype":"0",
              "recomgoods":"",
              "adminid":"1",
              "type":"0",
              "reviewmark":"pass",
              "stock":"18",
              "guige":"3-10\u7c73\u5730\u67dc + 3-10\u7c73\u53f0\u9762 + 1-5\u7c73\u540a\u67dc",
              "price_old":"20996",
              "price1":"28999",
              "price_old1":"74985",
              "standard_fittings_id":"1"
            }
          ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | int    | 商品id |
| goodsno       | int    | 商品编号 |
| goodsname         | int       | 商品标题 |
| subtitle       | String       | 子标题 |
| picurl      | String    | 图片地址，多个以引文分号隔开 |
| price     | double    | 商品价格 |
| classifyid  | int    | 分类id |
| goodsdesc       | text       | 商品描述 |
| isrecom     | int       | 是否推荐 0 不推荐 1 推荐 |
| buylimit | String    | 0：不限制 其他：限购数量 |
| tag | String    | 标签 |
| brandsid | int    | 品牌id |
| status  | int    | 状态 0 下架 1 上架 2 逻辑删除 3 待审核 4审核不通过 |
| createtime | String    | 创建时间 |
| updatetime | String    | 修改时间 |
| ordercount | int    | 预约数 |
| unit | String    | 商品单位 |
| recomtype | int    | 推荐类型 0 自动 1手动 |
| recomgoods | String    | 推荐的商品id，以英文逗号隔开（recomtype为1时有效） |
| adminid | int    | 发布者用户id |
| type | int    | 商品来源 0 自营 1供货商 |
| reviewmark | String    | 审核备注 |
| stock | int    | 库存 |
| guige | String    | 导购 |
| price_old | int    | 原价 |
| price1 | double    | 现价1 |
| price_old1 | double   | 原价1 |
| standard_fittings_id | int    | " |

***

## 5.注册新用户时发送验证码

* **URL:**

http://192.168.1.54/test/jvawa/sms/register.php

* **HTTP请求方式**

POST

* **请求参数**

        {"phoneNum":"13770936421"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| phoneNum | String    |手机号     |

* **返回结果**

        {"code":"400","info":"error","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | object    | null |

***

## 6.找回密码时发送验证码

* **URL:**

http://192.168.1.54/test/jvawa/sms/forgetpwd.php

* **HTTP请求方式**

POST

* **请求参数**

        {"phoneNum":"13770936421"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| phoneNum | String    |手机号     |

* **返回结果**

        {"code":"400","info":"error","data":""}

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | object    | null |

***

## 7.重置密码

* **URL:**

http://192.168.1.54/test/jvawa/reset_pwd.php

* **HTTP请求方式**

POST

* **请求参数**

        {"phoneNum":"13770936421","identifyCode":"5565","password":"******"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| phoneNum | String    |手机号     |
| identifyCode | String    |验证码     |
| password | String    |密码     |

* **返回结果**

        {"code":"400","info":"error","data":""}
        {"code":"200","info":"success","data":""}

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | object    | null |


***

## 8.注册新用户

* **URL:**

http://192.168.1.54/test/jvawa/register_new_user.php

* **HTTP请求方式**

POST

* **请求参数**

        {"phoneNum":"13770936421","identifyCode":"5565","password":"******"}

* **请求字段说明**

| 请求字段 | 字段类型  | 字段说明  |
|:--------:|:---------:|:---------:|
| phoneNum | String    |手机号     |
| identifyCode | String    |验证码     |
| password | String    |密码     |

* **返回结果**

        {"code":"400","info":"error","data":""}
        {"code":"200","info":"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | object    | null |

***

## 9.商品列表(可用于关键字查询)

* **URL:**

http://192.168.1.54/test/jvawa/product_list.php

* **HTTP请求方式**

POST

* **请求参数**

        {"isrecom":"-1","key":"精英悦厨"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| isrecom  | String    | 是否推荐，-1：所有 0：不推荐 1：新品推荐 2：热门商品 |
| key      | String    | 关键字     |


* **返回结果**

        {"code":"400","info":"error","data":""}
        {
          code: "200",
          info: "success",
          data:
          [
            {
              id: "3235",
              picurl: "uploads/1449556706.PNG;uploads/1449556714.PNG;uploads/1449556720.PNG",
              goodsname: "精英悦厨_丝丽卡B",
              myordercount: 435,
              mycommentcount: 27
            },
            {
              id: "2821",
              picurl: "uploads/1449555160.png;uploads/1449555275.png;uploads/1449555284.png",
              goodsname: "精英悦厨_简爱A",
              myordercount: 352,
              mycommentcount: 43
            },
            {
              id: "2825",
              picurl: "uploads/1444889885.jpg;uploads/1444889889.jpg;uploads/1444889894.jpg;uploads/1444889898.jpg",
              goodsname: "精英悦厨_迈森B",
              myordercount: 477,
              mycommentcount: 57
            },
            {
              id: "2832",
              picurl: "uploads/1444889688.jpg;uploads/1444889691.jpg",
              goodsname: "精英悦厨_挪威海岸",
              myordercount: 499,
              mycommentcount: 37
            },
            {
              id: "2835",
              picurl: "uploads/1449556706.PNG;uploads/1449556714.PNG;uploads/1449556720.PNG",
              goodsname: "精英悦厨_丝丽卡C",
              myordercount: 398,
              mycommentcount: 51
            },
            {
              id: "2838",
              picurl: "uploads/1459317400.jpg",
              goodsname: "精英悦厨_纸牌屋",
              myordercount: 329,
              mycommentcount: 19
            },
            {
              id: "2897",
              picurl: "uploads/1443142494.jpg;uploads/1443142502.jpg;uploads/1443142512.jpg",
              goodsname: "精英悦厨",
              myordercount: 492,
              mycommentcount: 51
            }
          ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | String    | 商品id |
| picurl      | String    | 图片地址，多个以引文分号隔开 |
| goodsname         | String       | 商品标题 |
| myordercount      | int    | 预约数 |
| mycommentcount    | int    | 评论数 |

***

## 10.商品详细

* **URL:**

http://192.168.1.54/test/jvawa/product_detail.php

* **HTTP请求方式**

POST

* **请求参数**

        {"gid":"2789"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| gid      | String    | 商品ID |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
           "code":"200",
           "info":"success",
           "data":
                {
                 "detail":
                 {
                  "gid":"3235",
                  "goodsname":"\u7cbe\u82f1\u60a6\u53a8_\u4e1d\u4e3d\u5361B",
                  "picurl":"uploads/1449556706.PNG;uploads/1449556714.PNG;uploads/1449556720.PNG",
                  "goodsdesc":"<img src=\"http://www.jvawa.com/uploads/1444889539.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889554.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889561.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889565.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889572.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889579.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889582.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889589.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889597.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889601.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889606.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889609.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889614.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889618.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889622.jpg\"><img src=\"http://www.jvawa.com/uploads/1444889626.jpg\">",
                  "subtitle":"",
                  "price_old":"20996",
                  "price":"10999",
                  "price_old1":"74985",
                  "price1":"28999",
                  "guide":"3-10\u7c73\u5730\u67dc + 3-10\u7c73\u53f0\u9762 + 1-5\u7c73\u540a\u67dc",
                  "tag":"\u4e1d\u4e3d\u5361B;15,17,18,19,20;4,6,19,20,22,23,84",
                  "ordermoney":2000,"ordercount":121
                  },
                 "colors":
                  [
                    {
                     "cid":"46",
                     "cname":"\u51e0\u4f55\u767dPVCD-0905",
                     "color":"\u4e1d\u4e3d\u5361B",
                     "cpath":"uploads/1444639102.png"
                     },
                     {
                      "cid":"47",
                      "cname":"\u51e0\u4f55\u9ed1PVCD-0905-1",
                      "color":"\u4e1d\u4e3d\u5361B",
                      "cpath":"uploads/1444639114.png"
                     },
                     {
                      "cid":"48",
                      "cname":"\u5e15\u91cc\u65afPVCD-0860-2",
                      "color":"\u4e1d\u4e3d\u5361B",
                      "cpath":"uploads/1444639127.png"
                      }
                   ],
                 "taimian":
                   [
                     {
                      "tid":"15",
                      "tname":"OLO-8886\u7389\u73ca\u745a",
                      "mode":"1459310048.png",
                      "tpath":"uploads/"
                      },
                      {
                       "tid":"17",
                       "tname":"OLO-8890-T\u5929\u5e55\u767d",
                       "mode":"1459310088.png",
                       "tpath":"uploads/"
                       },
                       {
                        "tid":"18",
                        "tname":"OLO-8893\u9713\u77f3\u970f",
                        "mode":"1459310104.png",
                        "tpath":"uploads/"
                        },
                        {
                         "tid":"19",
                         "tname":"OLO-8918\u5361\u666e\u8d5b\u8bfa",
                         "mode":"1459310124.png",
                         "tpath":"uploads/"
                        },
                        {
                         "tid":"20",
                         "tname":"OLO-8892\u5361\u74e6\u77f3",
                         "mode":"1459310655.png",
                         "tpath":"uploads/"
                        }
                   ],
                   "door":
                   [
                       {
                         "did":"84",
                         "dname":"L10",
                         "dpath":"uploads/1459317103.png",
                         "price":594,
                         "mode":"纸牌屋、简爱"
                        }
                    ]
                }
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为商品列表中商品的个数，为400时显示内容为错误信息 |
| gid        | int    | 商品id |
| goodsname         | String    | 商品标题 |
| picurl      | String    | 图片地址，多个以引文分号隔开 |
| goodsdesc    | text    | 商品描述 |
| subtitle    | String    | 副标题 |
| guige | String    | 导购 |
| price_old | int    | 原价 |
| price1 | double    | 现价1 |
| price_old1 | double   | 原价1 |
| tag | String    | 标签 |
| ordermoney    | String  | 预约金额 |
| ordercount    | String  | 预约数 |
| cid    | String    | 颜色ID |
| cname    | String    | 颜色名称 |
| color    | String    | 商品颜色 |
| cpath    | String    | 颜色图片地址 |
| tid    | String    | 台面ID |
| tname    | String    | 台面名称 |
| mode    | String    | 台面模式 |
| tpath    | text    | 台面图片地址 |
| did    | String    | 门ID |
| dname    | String    | 门名称 |
| dpath    | String    | 门图片地址 |
| price    | String    | 门价格 |
| mode    | String    | 门模式 |

***

## 11.添加商品到购物车

* **URL:**

http://192.168.1.54/test/jvawa/add_shoppingcart.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502","gid":"2789","action":"add","mode":"0","num":"1"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| gid      | String    | 商品ID |
| action   | String    | num：获得购物车中商品个数 add：添加到购物车 |
| mode     | String    | 添加到购物车的物品类型，0：橱柜或全屋定制，1：配件 |
| num      | String    | 购买配件的数量 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {"code":"200","info":"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为商品列表中商品的个数，为400时显示内容为错误信息 |

***

## 12.删除购物车里的内容

* **URL:**

http://192.168.1.54/test/jvawa/delete_shoppingcart.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"224","goodsstoreid":"2810"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| goodsstoreid      | String    | 商品id |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {code:"200",info:"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

## 13. 编辑用户配送信息(添加、更新、删除、设置默认地址 )

* **URL:**

http://192.168.1.54/test/jvawa/edit_address.php

* **HTTP请求方式**

POST

* **请求参数**

          添加：{"uid":"2502","reciverName":"小明","phoneNum":"13770963698","address":"南京市江宁区九龙湖企业园B1座","isDefault":"1","action":"add"}

          更新：{"uid":"2502","aid":"786""reciverName":"小明","phoneNum":"13770963698","address":"南京市江宁区九龙湖企业园B1座","isDefault":"0","action":"update"}

          删除：{"uid":"2502","aid":"786","action":"delete"}

          只设置默认地址：{"uid":"2502","aid":"786","isDefault":"1","action":"setDefault"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| aid      | String    | 地址ID |
| reciverName      | String    | 收货人姓名 |
| phoneNum   | String    | 收货人手机号 |
| address   | String    | 收货人地址 |
| isDefault   | String    | 是否设为默认地址 1：是 0：否 |
| action   | String    |  编辑方式 add：添加 update：更新 delete：删除      |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {"code":"200","info":"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |

***

## 14.获取用户配送信息(地址)

* **URL:**

http://192.168.1.54/test/jvawa/get_address.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
            "aid": "786",
            "receivername": "焦雁盛",
            "phone": "8451856969",
            "isdefault": "1",
            "address": "淮海路311号",
            "createtime": "2016-04-06 16:24:55"
          }
         ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| aid       | String    | 地址id |
| receivername       | String    | 收货人姓名 |
| phone       | String    | 收货人手机号 |
| isdefault       | String    | 是否为默认地址 1：是 0：否 |
| address       | String    | 收货人地址 |
| createtime       | String    | 该信息创建时间 |

***

## 15.获取门店相关信息(门店)

* **URL:**

http://192.168.1.54/test/jvawa/get_store_info.php

* **HTTP请求方式**

POST

* **请求参数**

        {"cityName":"南京", "storeName":"南京公司光华门店", "action":"store"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:---------:|:----------:|:---------:|
| cityName  | String    | 城市名 |
| storeName | String    | 门店名 |
| action    | String    | 获取数据的对象 store：门店信息 staff：门店员工信息 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
           "storeId": "629",
           "city": "南京",
           "trueName": "王庆霞",
           "phone": "15062285736",
           "address": "白下区光华路2号石林家居广场10号",
           "storeName": "南京公司光华门店",
           "userType": "2",
           "salerno": "NJ214"
          },
          {
           "storeId": "242",
           "city": "南京",
           "trueName": "田艳",
           "phone": "15358106566",
           "address": "雨花区卡子门大街88号石林家乐家",
           "storeName": "南京公司家乐家店",
           "userType": "2",
           "salerno": "NJ155"
          },
          {
           "storeId": "540",
           "city": "南京",
           "trueName": "王静",
           "phone": "15358106880",
           "address": "大桥北路48号弘阳广场弘阳家居A2馆2315号",
           "storeName": "南京公司桥北店",
           "userType": "2",
           "salerno": "NJ150"
          },
          {
           "storeId": "119",
           "city": "南京",
           "trueName": "经芳",
           "phone": "15358106759",
           "address": "雨花区卡子门红星美凯龙负一楼F8381号",
           "storeName": "南京公司红星店",
           "userType": "2",
           "salerno": "NJ020"
          },
          {
           "storeId": "635",
           "city": "南京",
           "trueName": "李青青",
           "phone": "13914485566",
           "address": "快特兰汀家居有限公司",
           "storeName": "南京公司达美店",
           "userType": "2",
           "salerno": "NJ205"
          },
          {
           "storeId": "185",
           "city": "南京",
           "trueName": "陈君",
           "phone": "15358106127",
           "address": "江宁区东山镇金宝装饰城精品洁具地板厅2号",
           "storeName": "南京公司金宝店",
           "userType": "2",
           "salerno": "NJ101"
          },
          {
           "storeId": "108",
           "city": "南京",
           "trueName": "徐云",
           "phone": "15358106312",
           "address": "建邺区江东中路80号-1楼B21-23号",
           "storeName": "南京公司金盛店",
           "userType": "2",
           "salerno": "NJ008"
          }
         ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| storeId       | String    | 门店id |
| city       | String    | 城市 |
| truename      | String    | 真实姓名 |
| phone       | String    | 门店手机号 |
| address       | String    | 门店地址 |
| storeName       | String    | 门店名 |
| userType       | String    | 0：超级管理员 1：门店管理员 2：门店店员 3：生产商 4:门店设计师 |
| salerno       | String    | 门店店员工号 |

***

## 16.获取门店员工相关信息(门店员工)

* **URL:**

http://192.168.1.54/test/jvawa/get_store_info.php

* **HTTP请求方式**

POST

* **请求参数**

        {"cityName":"南京", "storeName":"南京公司光华门店", "action":"staff"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:---------:|:----------:|:---------:|
| cityName  | String    | 城市名 |
| storeName | String    | 门店名 |
| action    | String    | 获取数据的对象 store：门店信息 staff：门店员工信息 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
           "salerno": "NJ023",
           "truename": "李兰兰",
           "storeId": "122",
           "storeName": "南京公司光华门店"
          },
          {
           "salerno": "NJ214",
           "truename": "王庆霞",
           "storeId": "629",
           "storeName": "南京公司光华门店"
          },
          {
           "salerno": "NJ213",
           "truename": "杨向北",
           "storeId": "628",
           "storeName": "南京公司光华门店"
          },
          {
           "salerno": "NJ223",
           "truename": "唐巍",
           "storeId": "627",
           "storeName": "南京公司光华门店"
          }
         ]
        }

 * **返回字段说明**       

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| salerno       | String    | 门店员工工号 |
| truename       | String    | 门店员工姓名 |
| storeId      | String    | 门店Id |
| storeName       | String    | 门店名称 |

***

## 17.商品分类

* **URL:**

http://192.168.1.54/test/jvawa/get_class.php

* **HTTP请求方式**

POST

* **请求参数**

        {"action":"class"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:---------:|:----------:|:---------:|
| class  | String    |   请求行为  |


* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
            "id": "1",
            "name": "橱柜",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "2",
            "name": "全屋定制",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "64",
            "name": "五金",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "65",
            "name": "台面、边型及垫条",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "66",
            "name": "水槽、龙头",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "67",
            "name": "净水器",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "68",
            "name": "厨电",
            "status": "1",
           parentid: "0"
          },
          {
            "id": "69",
            "name": "照明",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "74",
            "name": "礼品",
            "status": "1",
            "parentid": "0"
          },
          {
            "id": "3",
            "name": "小康美厨",
            "status": "1",
            "parentid": "1"
          }
         ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id       | String      | 分类id |
| name       | String    | 分类名称 |
| status      | String   | 状态 1启用 0未启用 |
| parentid       | String    | 商品归属的类的id |

***

## 18.获取用户购物车内容

* **URL:**

http://192.168.1.54/test/jvawa/get_shopping_cart.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"224"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
           "id": "2862",
           "goodsname": "名家雅厨_普瑞达A",
           "imgurl": "uploads/1446711418.jpg",
           "price": "14999",
           "subtitle": "",
           "buycount": "1"
          },
          {
           "id": "3062",
           "goodsname": "二级过滤净水器-OLO-JS-02",
           "imgurl": "uploads/1446513097.png",
           "price": "1248",
           "subtitle": "配件",
           "buycount": "5"
          },
          {
           "id": "3130",
           "goodsname": "台面边型-LMB07",
           "imgurl": "uploads/1466391728.png",
           "price": "1629",
           "subtitle": "配件",
           "buycount": "1"
          },
          {
           "id": "2991",
           "goodsname": "米箱OLO-MX25",
           "imgurl": "uploads/1446449359.png",
           "price": "1012",
           "subtitle": "配件",
           "buycount": "3"
          }
         ]
        }

* **返回字段说明**       

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | String    | 商品Id |
| goodsname       | String    | 商品名称 |
| imgurl       | String    | 图片地址 |
| price       | String    | 商品价格 |
| subtitle       | String    | 商品子标题 |
| buycount       | String    | 购买数量 |

***

## 19.获取用户礼券信息列表

* **URL:**

http://192.168.1.54/test/jvawa/get_coupons_list.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"224","status":"1"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| status      | String    | 优惠券状态，1：未使用 2：已使用 3：已过期 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
         [
          {
           "lpGoodid": "3215",
           "discount": "1",
           "lastTime": "2016-05-31 23:59:59",
           "name": "JJ61241449112187",
           "status": "1",
           "mode": "1、参加12.5-12.27当期活动，缴纳6000元订金后生效，签订合同时使用，一套橱柜产品仅能使用一张奖券。       2、2016新品尝鲜活动价活动不参与本活动（不可使用礼券）。 3、本礼券不可单独使用、折现等其他用途。"
          },
          {
           "lpGoodid": "0",
           "discount": "1",
           "lastTime": "2016-05-31 23:59:59",
           "name": "JJ72381452041262",
           "status": "1",
           "mode": " 1、本礼券为1.3-1.31活动发布，签订合同时冲抵现金。 2、可抵用范围为五金、电器。 3、本礼券不可折现、不找零、兑现。 4、本礼券每人每次仅可使用一张，不可叠加使用。"
          },
          {
           "lpGoodid": "3215",
           "discount": "1",
           "lastTime": "2017-03-16 23:59:59",
           "name": "JJ81881456277342",
           "status": "1",
           "mode": "1、	本礼券为厨艺复兴活动发布。 2、	合同金额超过9999元，方可使用本礼券。 3、	本礼券不可折现、不找零、兑现。 4、	本礼券每次仅可使用一张。"
          }
         ]
        }

* **返回字段说明**       

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| lpGoodid         | String    | 优惠券id |
| discount       | String    | 打折数 |
| lastTime       | String    | 礼券有效期 |
| name       | String    | 礼券名称 |
| status       | String    | 礼券状态 |
| mode       | String    | 礼券说明 |

***

## 20.获取用户订单列表

* **URL:**

http://192.168.1.54/test/jvawa/get_userorder_list.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"213"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         code: "200",
         info: "success",
         data:
          [
           {
            "erpstatus": "商机单",
            "subbillid": "99941008",
            "superbillid": "99901653",
            "picurl": "uploads/1449555160.png;uploads/1449555275.png;uploads/1449555284.png",
            "goodsname": "精英悦厨_简爱A",
            "billprice": "10999",
            "status": "1",
            "schedprice": "2000",
            "color": "diy预约，预约金",
            "createtime": "2016-02-29 15:23:53",
            "yyid": "SJ2016022917839",
            "price": "10999",
            "buynum": "1"
           },
           {
            "erpstatus": "商机单",
            "subbillid": "99940960",
            "superbillid": "99901605",
            "picurl": "uploads/1449650214.PNG;uploads/1449650223.PNG",
            "goodsname": "小康美厨_雕刻时光A",
            "billprice": "6999",
            "status": "1",
            "schedprice": "2000",
            "color": "diy预约，预约金",
            "createtime": "2016-02-27 18:31:17",
            "yyid": "SJ2016022717633",
            "price": "6999",
            "buynum": "1"
           },
           {
            "erpstatus": "商机单",
            "subbillid": "99940894",
            "superbillid": "99901539",
            "picurl": "uploads/1449555160.png;uploads/1449555275.png;uploads/1449555284.png",
            "goodsname": "精英悦厨_简爱A",
            "billprice": "10999",
            "status": "1",
            "schedprice": "2000",
            "color": "diy预约，预约金",
            "createtime": "2016-02-26 11:25:52",
            "yyid": "SJ2016022617561",
            "price": "10999",
            "buynum": "1"
           }
         ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| erpstatus         | String    | "" |
| subbillid       | String    | 子订单id |
| superbillid       | String    | 主订单id |
| goodsname       | String    | 商品名称 |
| billprice       | String    | 订单总价 |
| status       | String    | 订单状态 0：未付款 1：已预约 2：已付款 3：配送中 4：待评价 5：已完成 6：设计师已测量 -1：订单取消 |
| schedprice       | String    | 预约总价 |
| color       | String    | "" |
| createtime       | String    | 订单创建时间 |
| yyid       | String    | "" |
| price       | String    | 商品价格 |
| buynum       | String    | 购买数量 |

***

## 21.获取活动列表

* **URL:**

http://192.168.1.54/test/jvawa/get_activity_list.php

* **HTTP请求方式**

POST

* **请求参数**

        {"action":"activity"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:---------:|:----------:|:---------:|
| activity  | String    |   请求行为  |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
          [
           {
            "id": "29",
            "type": "1",
            "title": "6月活动",
            "imgurl": "uploads/1464942882.jpg",
            "href": "http://www.jvawa.com/new/game/AprilSpecial/special.php",
            "sort": "1",
            "status": "1",
            "createtime": "2016-06-03 16:22:32"
           },
           {
            "id": "20",
            "type": "1",
            "title": "大转盘",
            "imgurl": "uploads/1452045879.jpg",
            "href": "#",
            "sort": "2",
            "status": "0",
            "createtime": "2015-10-13 14:17:19"
           },
           {
            "id": "22",
            "type": "1",
            "title": "双十一活动",
            "imgurl": "uploads/1446538960.jpg",
            "href": "#",
            "sort": "3",
            "status": "0",
            "createtime": "2015-11-02 10:36:06"
           }
          ]
        }

* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | String    | 活动id |
| type       | String    | 位置类型 |
| title       | String    | 标题 |
| imgurl       | String    | 图片地址 |
| href       | String    | 点击图片跳转地址  #：不可跳转|
| status       | String | 活动状态 0：往期活动 1：正在进行|
| createtime       | String    | 活动创建时间 |

***

## 22.生成配件订单

* **URL:**

http://192.168.1.54/test/jvawa/generate_parts_order.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502", "billprice":"5000", "schedprice":"2000", "storeid":"122",
          "phone":"13770936421", "receivername":"焦哥", "receiveraddress":"南京市九龙湖企业园阿米巴",
          "isperfe":"0", "salerno":"NJ023", "goodsid":"2789", "picurl":"uploads/1449650214.PNG",
          "num":"1", "desingerprice":"0",
        }

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| billprice      | String    | 总价 |
| schedprice      | String    | 预约总价 |
| storeid      | String    | 门店id |
| phone      | String    | 联系号码 |
| receivername      | String    | 收件人姓名 |
| receiveraddress      | String    | 收件人地址 |
| isperfe      | String    | 是否活动价格(0：否 1：是) |
| salerno      | String    | 店员工号 |
| goodsid      | String    | 商品编号 |
| picurl      | String    | 图片地址 |
| num      | String    | 购买数量 |
| desingerprice      | String    | 修改后的价格 客户端目前默认传 0 即可 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code": "200",
          "info": "success",
          "data":
          {
            "superbillid": 99902818,
            "price": "5000",
            "allSchedprice": 200000,
            "goodsName": "小康美厨_雕刻时光A",
            "imgurl": "uploads/1449650214.PNG"
          }
        }


* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| superbillid       | int    | 订单号 |
| price       | String    | 单价 |
| allSchedprice       | int    | 总价 |
| goodsName       | String    | 商品名 |
| imgurl       | String    | 图片地址 |

***

## 23.生成主件(橱柜之类)订单

* **URL:**

http://192.168.1.54/test/jvawa/generate_main_order.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"213", "billprice":"", "schedprice":"", "storeid":"",
          "phone":"", "receivername":"", "receiveraddress":"",
          "isperfe":"", "salerno":"", "goodsid":"", "picurl":"",
          "num":"", "desingerprice":"", "colorid":"",
          "taimianid":"", "doorid":"", "mishu1":"",
          "mishu2":"", "huodongneirong":"", "kehuyaoqiu":"",
          "lingjifeixiang":"","beizhu":"", "bzpj":"", "diypj":"",
          "goodsname":"", "cityName":"", "color":""
        }

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| billprice      | String    | 总价 |
| schedprice      | String    | 预约总价 |
| storeid      | String    | 门店id |
| phone      | String    | 联系号码 |
| receivername      | String    | 收件人姓名 |
| receiveraddress      | String    | 收件人地址 |
| isperfe      | String    | 是否活动价格(0：否 1：是) |
| salerno      | String    | 店员工号 |
| goodsid      | String    | 商品编号 |
| picurl      | String    | 图片地址 |
| num      | String    | 购买数量 |
| color      | String    | 支付方式 |
| desingerprice      | String    | 修改后的价格 客户端目前默认传 0 即可 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
         "code": "200",
         "info": "success",
         "data":
          {
            "superbillid": 99902840,
            "allSchedprice": 100,
            "goodsName": "尚品魅厨_诺特",
            "imgurl": "uploads/1444890402.jpg;"
          }
        }


* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| superbillid       | int    | 订单号 |
| allSchedprice       | int    | 总价 |
| goodsName       | String    | 商品名 |
| imgurl       | String    | 图片地址 |

***

## 24.生成全屋订单

* **URL:**

http://192.168.1.54/test/jvawa/generate_home_order.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502", "billprice":"5000", "schedprice":"2000", "storeid":"122",
          "phone":"13770936421", "receivername":"焦哥", "receiveraddress":"南京市九龙湖企业园阿米巴",
          "isperfe":"0", "salerno":"NJ023", "goodsid":"3471", "picurl":"uploads/1449650214.PNG",
          "desingerprice":"0",
        }

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| billprice      | String    | 总价 |
| schedprice      | String    | 预约总价 |
| storeid      | String    | 门店id |
| phone      | String    | 联系号码 |
| receivername      | String    | 收件人姓名 |
| receiveraddress      | String    | 收件人地址 |
| isperfe      | String    | 是否活动价格(0：否 1：是) |
| salerno      | String    | 店员工号 |
| goodsid      | String    | 商品编号 |
| picurl      | String    | 图片地址 |
| desingerprice      | String    | 修改后的价格 客户端目前默认传 0 即可 |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code": "200",
          "info": "success",
          "data":
          {
            "superbillid": 99902818,
            "price": "5000",
            "allSchedprice": 200000,
            "goodsName": "波尔多",
            "imgurl": "uploads/1449650214.PNG"
          }
        }


* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| superbillid       | int    | 订单号 |
| price       | String    | 单价 |
| allSchedprice       | int    | 总价 |
| goodsName       | String    | 商品名 |
| imgurl       | String    | 图片地址 |

***

## 25.修改密码

* **URL:**

http://192.168.1.54/test/jvawa/change_pwd.php

* **HTTP请求方式**

POST

    {"uid":"138", "orgPwd":"*******", "newPwd":"********"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| orgPwd      | String    | 旧密码 |
| newPwd      | String    | 新密码 |

* **返回结果**

        {"code": "400","info": "输入的旧密码有误！","data": ""}

        {"code": "200","info": "新密码设置完成！","data": ""}

* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

## 26.保存已支付订单

* **URL:**

http://192.168.1.54/test/jvawa/save_bill.php

* **HTTP请求方式**

POST

        {"tradeNo":"138", "superBillId":"*******", "price":"2000", "payType":"微信支付"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| tradeNo      | String    | BeeCloud(微信或支付宝或其他)返回的支付单号 |
| superBillId      | String    | 商品订单号 |
| price      | String    | 支付金额 |
| payType      | String    | 支付方式，(微信支付或支付宝支付或其他 由BeeCloud返回 |

* **返回结果**

       {"code": "400","info": "生成支付订单失败！","data": ""}

       {"code": "200","info": "success","data": ""}

* **返回字段说明**    

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

***

## 27.删除用户订单

* **URL:**

http://192.168.1.54/test/jvawa/delete_order.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2540","superbillid":"99902940", "subbillid":"99942635"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| superbillid      | String    | 主订单id |
| subbillid      | String    | 子订单id |

* **返回结果**

        {"code":"400","info":"error","data":""}

        {code:"200",info:"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

***

## 28.增减购物车配件的数量

* **URL:**

http://192.168.1.54/test/jvawa/shop_buycount.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2540", "id":"****", "buyCount":"4"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| id       | String    | 购物车列表返回的id|
| buyCount      | String    | 购买的数量 |


* **返回结果**

        {"code":"400","info":"error","data":""}

        {code:"200",info:"success","data":""}

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

***

## 29.生成购物车订单

* **URL:**

http://192.168.1.54/test/jvawa/generate_shoppingcart_order.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2540", "payId":"", "phone":"", "receiverAddress":"", "receiverName":"",
         "salerno":"", "storeId":"", "schedprice":"", "city":""}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| payId      | String    | 购物车的gid，如果是多个商品购买，那么payId为多个购物车gid拼接而成，且用","逗号分割 |
| phone      | String    | 收货人手机号 |
| receiverAddress      | String    | 收货人地址 |
| receiverName      | String    | 收货人姓名 |
| salerno      | String    | 店员工号 |
| storeId      | String    | 门店Id |
| schedprice      | String    | 预约总价，此处不必传所有商品总价 |
| city      | String    | 城市 |

注：一次只能选择一件（橱柜或全屋商品）！

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
          "code": "200",
          "info": "success",
          "data":
          {
            "superbillid": 99902818,
            "price": "5000",
            "allSchedprice": 200000,
            "goodsName": "波尔多,垃圾桶,水槽",
            "imgurl": "uploads/1449650214.PNG"
          }
        }
* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| superbillid       | int    | 订单号 |
| allSchedprice       | int    | 总价 |
| goodsName       | String    | 商品名 |
| imgurl       | String    | 图片地址 |

***

## 30.获取用户礼券列表

* **URL:**

http://192.168.1.54/test/jvawa/get_coupons_list.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"213", "mode":"1"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| mode     | String    | 礼券状态 mode：1：未使用 2：已使用 3：已过期|

* **返回结果**

        {"code":"400","info":"error","data":""}

        {
        "code": "200",
        "info": "success",
        "data": 
         [
          {
          "lpGoodid": "3215",
          "discount": "1",
          "lastTime": "2016-05-31 23:59:59",
          "name": "JJ61221449112187",
          "title":"2016双十一活动礼券"
          "status": "1",
          "mode": "1、参加12.5-12.27当期活动，缴纳6000元订金后生效，签订合同时使用，一套橱柜产品仅能使用一张奖券。 2、2016新品尝鲜活动价活动不参与本活动（不可使用礼券）。 3、本礼券不可单独使用、折现等其他用途。"
          }
         ]
        }

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| lpGoodid         | String    | 礼券id |
| discount       | String    | "" |
| lastTime       | String    | 使用时间 |
| name       | String    | 礼券单号 |
| title       | String    | 礼券标题 |
| status       | String    | 礼券状态 1：未使用 2：已使用 3：已过期 |
| mode       | String    | 礼券使用规则 |

***

## 31.双十一1元抢购接口

* **URL:**

http://192.168.1.54/test/jvawa/onebuy_event.php

* **HTTP请求方式**

POST

* **请求参数**

        {"tradeNo":"213","payType":"微信支付"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| tradeNo     | String    | 微信支付渠道单号 |
| payType     | String    | 支付方式，如：微信支付，银联支付|

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {"code":"200","info":"success","data":""}
    

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |


***

## 32.双十一1元抢购判断接口

* **URL:**

http://192.168.1.54/test/jvawa/onebuy_has.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"213","goodsId":"3505"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| goodsId  | String    | 活动产品id|

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {"code":"200","info":"success","data":""}
    

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |

***

## 33.双十一签到接口

* **URL:**

http://192.168.1.54/test/jvawa/signin_event.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"213","goodsId":"3506"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户id |
| goodsId  | String    | 活动产品id|

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {"code":"200","info":"success","data":""}
    

* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | String    | "" |






