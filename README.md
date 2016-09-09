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
            "createtime":"2015-09-2701:21:34",
            "headImg":"http://wx.qlogo.cn/mmopen/ajNVdqHZLLAq8171DGiaEfaHdPDetF5XavppaYOicZ7r1mPHNhnkVlZfw4pcsLdAEkjwWsSjJvPuVXoA6rAHEHibw/0",
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
| isrecom  | String    |是否推荐，0：不推荐 1：新品推荐 2：热门商品|

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

## 7.注册新用户

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

## 8.商品列表(可用于关键字查询)

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
| id         | int    | 商品id |
| picurl      | String    | 图片地址，多个以引文分号隔开 |
| goodsname         | String       | 商品标题 |
| myordercount      | int    | 预约数 |
| mycommentcount    | int    | 评论数 |

***

## 9.商品详细

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

## 10.添加商品到购物车

* **URL:**

http://192.168.1.54/test/jvawa/add_shoppingcart.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502","gid":"2789","action":"add"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| gid      | String    | 商品ID |
| action   | String    | num：获得购物车中商品个数 add：添加到购物车 |

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {"code":"200","info":"success","data":""}
        
* **返回字段说明**

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为商品列表中商品的个数，为400时显示内容为错误信息 |

***

## 11.删除购物车里的内容

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
| data       | Object    | null |

## 12.添加用户配送信息(地址)

* **URL:**

http://192.168.1.54/test/jvawa/add_address.php

* **HTTP请求方式**

POST

* **请求参数**

        {"uid":"2502","reciverName":"小明","phoneNum":"13770963698","address":"南京市江宁区九龙湖企业园B1座"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| uid      | String    | 用户ID |
| reciverName      | String    | 收货人姓名 |
| phoneNum   | String    | 收货人手机号 |
| address   | String    | 收货人地址 |

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {"code":"200","info":"success","data":""}
        
* **返回字段说明**
 
| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |

***

## 13.获取用户配送信息(地址)

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

* **返回字段说明**

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {
         code: "200",
         info: "success",
         data: 
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

## 14.删除用户配送信息(地址)

* **URL:**

http://192.168.1.54/test/jvawa/delete_address.php

* **HTTP请求方式**

POST

* **请求参数**

        {"aid":"393"}

* **请求字段说明**

| 请求字段  | 字段类型   | 字段说明  |
|:--------:|:---------:|:---------:|
| aid      | String    | 地址ID |

* **返回字段说明**

* **返回结果**

        {"code":"400","info":"error","data":""}
        
        {code:"200",info:"success","data":""} 

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| data       | Object    | null |

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

* **返回字段说明**

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

* **返回字段说明**

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

        无

* **请求字段说明**

        无

* **返回字段说明**

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

* **返回字段说明**

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
           "picurl": "uploads/1446711418.jpg",
           "price": "14999",
           "subtitle": "",
           "buycount": "1"
          },
          {
           "id": "3062",
           "goodsname": "二级过滤净水器-OLO-JS-02",
           "picurl": "uploads/1446513097.png",
           "price": "1248",
           "subtitle": "配件",
           "buycount": "5"
          },
          {
           "id": "3130",
           "goodsname": "台面边型-LMB07",
           "picurl": "uploads/1466391728.png",
           "price": "1629",
           "subtitle": "配件",
           "buycount": "1"
          },
          {
           "id": "2991",
           "goodsname": "米箱OLO-MX25",
           "picurl": "uploads/1446449359.png",
           "price": "1012",
           "subtitle": "配件",
           "buycount": "3"
          }
         ]
        }
        

| 返回值字段 | 字段类型  | 字段说明  |
|:----------:|:---------:|:---------:|
| code       | String    | 200：成功 400：失败 |
| info       | String    | code为200时显示内容为成功信息，为400时显示内容为错误信息 |
| id         | String    | 购物车 |
| goodsname       | String    | 商品名称 |
| picurl       | String    | 图片地址 |
| price       | String    | 商品价格 |
| subtitle       | String    | 商品子标题 |
| buycount       | String    | 购买数量 |




