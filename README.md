# 基于web的酒店客房管理系统

## 简介

本代码仅供学习参考使用

加QQ(**3055269939**)免费获取项目和论文

## 主要内容

### 数据库设计表

酒店客房管理系统需要后台数据库，下面介绍数据库中的各个表的详细信息：

 

 

表4.1 在线客服

| 字段      | 类型       | 空   | 默认              | 注释     |
| --------- | ---------- | ---- | ----------------- | -------- |
| id (主键) | bigint(20) | 否   |                   | 主键     |
| addtime   | timestamp  | 否   | CURRENT_TIMESTAMP | 创建时间 |
| userid    | bigint(20) | 否   |                   | 用户id   |
| adminid   | bigint(20) | 是   | NULL              | 管理员id |
| ask       | longtext   | 是   | NULL              | 提问     |
| reply     | longtext   | 是   | NULL              | 回复     |
| isreply   | int(11)    | 是   | NULL              | 是否回复 |

表4.2 会员

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| zhanghao     | varchar(200) | 否   |                   | 账号     |
| mima         | varchar(200) | 否   |                   | 密码     |
| xingming     | varchar(200) | 是   | NULL              | 姓名     |
| nianling     | varchar(200) | 是   | NULL              | 年龄     |
| xingbie      | varchar(200) | 是   | NULL              | 性别     |
| shouji       | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng | varchar(200) | 是   | NULL              | 身份证   |
| zhaopian     | varchar(200) | 是   | NULL              | 照片     |

表4.3 会员取消

| 字段          | 类型         | 空   | 默认              | 注释     |
| ------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)     | bigint(20)   | 否   |                   | 主键     |
| addtime       | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yuyuebianhao  | varchar(200) | 是   | NULL              | 预约编号 |
| kefanghao     | varchar(200) | 是   | NULL              | 客房号   |
| shifouquxiao  | varchar(200) | 是   | NULL              | 是否取消 |
| jiage         | varchar(200) | 是   | NULL              | 价格     |
| tianshu       | int(11)      | 是   | NULL              | 天数     |
| zongjia       | varchar(200) | 是   | NULL              | 总价     |
| quxiaoyuanyin | longtext     | 是   | NULL              | 取消原因 |
| quxiaoshijian | datetime     | 是   | NULL              | 取消时间 |
| zhanghao      | varchar(200) | 是   | NULL              | 账号     |
| xingming      | varchar(200) | 是   | NULL              | 姓名     |
| shouji        | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng  | varchar(200) | 是   | NULL              | 身份证   |
| sfsh          | varchar(200) | 是   | 否                | 是否审核 |
| shhf          | longtext     | 是   | NULL              | 审核回复 |
| ispay         | varchar(200) | 是   | 未支付            | 是否支付 |

表4.4 会员入住

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| dingdanbianhao  | varchar(200) | 是   | NULL              | 订单编号 |
| kefanghao       | varchar(200) | 是   | NULL              | 客房号   |
| kefangleixing   | varchar(200) | 是   | NULL              | 客房类型 |
| suoshujiudian   | varchar(200) | 是   | NULL              | 所属酒店 |
| zhanghao        | varchar(200) | 是   | NULL              | 账号     |
| xingming        | varchar(200) | 是   | NULL              | 姓名     |
| shenfenzheng    | varchar(200) | 是   | NULL              | 身份证   |
| shouji          | varchar(200) | 是   | NULL              | 手机     |
| kefangzhuangtai | varchar(200) | 是   | NULL              | 客房状态 |
| ruzhuyajin      | float        | 是   | NULL              | 入住押金 |
| zhifufangshi    | varchar(200) | 是   | NULL              | 支付方式 |
| ruzhushijian    | datetime     | 是   | NULL              | 入住时间 |
| ispay           | varchar(200) | 是   | 未支付            | 是否支付 |

表4.5 会员退房

| 字段           | 类型         | 空   | 默认              | 注释     |
| -------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)      | bigint(20)   | 否   |                   | 主键     |
| addtime        | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| dingdanbianhao | varchar(200) | 是   | NULL              | 订单编号 |
| kefanghao      | varchar(200) | 是   | NULL              | 客房号   |
| kefangleixing  | varchar(200) | 是   | NULL              | 客房类型 |
| suoshujiudian  | varchar(200) | 是   | NULL              | 所属酒店 |
| zhanghao       | varchar(200) | 是   | NULL              | 账号     |
| xingming       | varchar(200) | 是   | NULL              | 姓名     |
| shenfenzheng   | varchar(200) | 是   | NULL              | 身份证   |
| shouji         | varchar(200) | 是   | NULL              | 手机     |
| ruzhuyajin     | varchar(200) | 是   | NULL              | 入住押金 |
| tuifangshijian | datetime     | 是   | NULL              | 退房时间 |
| ispay          | varchar(200) | 是   | 未支付            | 是否支付 |

表4.6 会员预约

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yuyuebianhao | varchar(200) | 是   | NULL              | 预约编号 |
| kefanghao    | varchar(200) | 是   | NULL              | 客房号   |
| ruzhushijian | datetime     | 是   | NULL              | 入住时间 |
| jiage        | varchar(200) | 是   | NULL              | 价格     |
| tianshu      | int(11)      | 是   | NULL              | 天数     |
| zongjia      | varchar(200) | 是   | NULL              | 总价     |
| yuyueshijian | datetime     | 是   | NULL              | 预约时间 |
| zhanghao     | varchar(200) | 是   | NULL              | 账号     |
| xingming     | varchar(200) | 是   | NULL              | 姓名     |
| shouji       | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng | varchar(200) | 是   | NULL              | 身份证   |
| sfsh         | varchar(200) | 是   | 否                | 是否审核 |
| shhf         | longtext     | 是   | NULL              | 审核回复 |
| ispay        | varchar(200) | 是   | 未支付            | 是否支付 |

表4.7 客房信息

| 字段              | 类型         | 空   | 默认              | 注释         |
| ----------------- | ------------ | ---- | ----------------- | ------------ |
| id (主键)         | bigint(20)   | 否   |                   | 主键         |
| addtime           | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间     |
| kefanghao         | varchar(200) | 否   |                   | 客房号       |
| kefangleixing     | varchar(200) | 是   | NULL              | 客房类型     |
| chuangxing        | varchar(200) | 否   |                   | 床型         |
| kefangtupian      | varchar(200) | 是   | NULL              | 客房图片     |
| fangjianmianji    | varchar(200) | 是   | NULL              | 房间面积     |
| jiage             | int(11)      | 是   | NULL              | 价格         |
| kefangzhuangtai   | varchar(200) | 是   | NULL              | 客房状态     |
| keyueshijian      | varchar(200) | 是   | NULL              | 可约时间     |
| weishengqingkuang | varchar(200) | 是   | NULL              | 卫生情况     |
| kefanghuanjing    | varchar(200) | 是   | NULL              | 客房环境     |
| suoshujiudian     | varchar(200) | 是   | NULL              | 所属酒店     |
| kefangjieshao     | longtext     | 是   | NULL              | 客房介绍     |
| clicktime         | datetime     | 是   | NULL              | 最近点击时间 |
| clicknum          | int(11)      | 是   | 0                 | 点击次数     |

表4.8 留言板

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| userid    | bigint(20)   | 否   |                   | 留言人id |
| username  | varchar(200) | 是   | NULL              | 用户名   |
| content   | longtext     | 否   |                   | 留言内容 |
| reply     | longtext     | 是   | NULL              | 回复内容 |

表4.9 酒店资讯

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| title        | varchar(200) | 否   |                   | 标题     |
| introduction | longtext     | 是   | NULL              | 简介     |
| picture      | varchar(200) | 否   |                   | 图片     |
| content      | longtext     | 否   |                   | 内容     |

表4.10 清洁人员

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| qingjiezhanghao | varchar(200) | 否   |                   | 清洁账号 |
| mima            | varchar(200) | 否   |                   | 密码     |
| qingjiexingming | varchar(200) | 是   | NULL              | 清洁姓名 |
| nianling        | varchar(200) | 是   | NULL              | 年龄     |
| xingbie         | varchar(200) | 是   | NULL              | 性别     |
| shouji          | varchar(200) | 是   | NULL              | 手机     |
| zhaopian        | varchar(200) | 是   | NULL              | 照片     |

表4.11 清扫房间

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| kefanghao       | varchar(200) | 是   | NULL              | 客房号   |
| kefangleixing   | varchar(200) | 是   | NULL              | 客房类型 |
| suoshujiudian   | varchar(200) | 是   | NULL              | 所属酒店 |
| shifoudasao     | varchar(200) | 是   | NULL              | 是否打扫 |
| dasaoshijian    | datetime     | 是   | NULL              | 打扫时间 |
| qingjiezhanghao | varchar(200) | 是   | NULL              | 清洁账号 |
| qingjiexingming | varchar(200) | 是   | NULL              | 清洁姓名 |

表4.12 收藏表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| refid     | bigint(20)   | 是   | NULL              | 收藏id   |
| tablename | varchar(200) | 是   | NULL              | 表名     |
| name      | varchar(200) | 否   |                   | 收藏名称 |
| picture   | varchar(200) | 否   |                   | 收藏图片 |

表4.13 管理员表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| username  | varchar(100) | 否   |                   | 用户名   |
| password  | varchar(100) | 否   |                   | 密码     |
| role      | varchar(100) | 是   | 管理员            | 角色     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 新增时间 |

表4.14 用户

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| zhanghao     | varchar(200) | 否   |                   | 账号     |
| mima         | varchar(200) | 否   |                   | 密码     |
| xingming     | varchar(200) | 是   | NULL              | 姓名     |
| nianling     | varchar(200) | 是   | NULL              | 年龄     |
| xingbie      | varchar(200) | 是   | NULL              | 性别     |
| shouji       | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng | varchar(200) | 是   | NULL              | 身份证   |
| zhaopian     | varchar(200) | 是   | NULL              | 照片     |

表4.15 用户取消

| 字段          | 类型         | 空   | 默认              | 注释     |
| ------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)     | bigint(20)   | 否   |                   | 主键     |
| addtime       | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yuyuebianhao  | varchar(200) | 是   | NULL              | 预约编号 |
| kefanghao     | varchar(200) | 是   | NULL              | 客房号   |
| shifouquxiao  | varchar(200) | 是   | NULL              | 是否取消 |
| jiage         | varchar(200) | 是   | NULL              | 价格     |
| tianshu       | int(11)      | 是   | NULL              | 天数     |
| zongjia       | varchar(200) | 是   | NULL              | 总价     |
| quxiaoyuanyin | longtext     | 是   | NULL              | 取消原因 |
| quxiaoshijian | datetime     | 是   | NULL              | 取消时间 |
| zhanghao      | varchar(200) | 是   | NULL              | 账号     |
| xingming      | varchar(200) | 是   | NULL              | 姓名     |
| shouji        | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng  | varchar(200) | 是   | NULL              | 身份证   |
| sfsh          | varchar(200) | 是   | 否                | 是否审核 |
| shhf          | longtext     | 是   | NULL              | 审核回复 |
| ispay         | varchar(200) | 是   | 未支付            | 是否支付 |

表4.16 用户入住

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| dingdanbianhao  | varchar(200) | 是   | NULL              | 订单编号 |
| kefanghao       | varchar(200) | 是   | NULL              | 客房号   |
| kefangleixing   | varchar(200) | 是   | NULL              | 客房类型 |
| suoshujiudian   | varchar(200) | 是   | NULL              | 所属酒店 |
| zhanghao        | varchar(200) | 是   | NULL              | 账号     |
| xingming        | varchar(200) | 是   | NULL              | 姓名     |
| shenfenzheng    | varchar(200) | 是   | NULL              | 身份证   |
| shouji          | varchar(200) | 是   | NULL              | 手机     |
| kefangzhuangtai | varchar(200) | 是   | NULL              | 客房状态 |
| ruzhuyajin      | float        | 是   | NULL              | 入住押金 |
| zhifufangshi    | varchar(200) | 是   | NULL              | 支付方式 |
| ruzhushijian    | datetime     | 是   | NULL              | 入住时间 |
| ispay           | varchar(200) | 是   | 未支付            | 是否支付 |

表4.17 用户退房

| 字段           | 类型         | 空   | 默认              | 注释     |
| -------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)      | bigint(20)   | 否   |                   | 主键     |
| addtime        | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| dingdanbianhao | varchar(200) | 是   | NULL              | 订单编号 |
| kefanghao      | varchar(200) | 是   | NULL              | 客房号   |
| kefangleixing  | varchar(200) | 是   | NULL              | 客房类型 |
| suoshujiudian  | varchar(200) | 是   | NULL              | 所属酒店 |
| zhanghao       | varchar(200) | 是   | NULL              | 账号     |
| xingming       | varchar(200) | 是   | NULL              | 姓名     |
| shenfenzheng   | varchar(200) | 是   | NULL              | 身份证   |
| shouji         | varchar(200) | 是   | NULL              | 手机     |
| ruzhuyajin     | varchar(200) | 是   | NULL              | 入住押金 |
| tuifangshijian | datetime     | 是   | NULL              | 退房时间 |
| ispay          | varchar(200) | 是   | 未支付            | 是否支付 |

表4.18 用户预约

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yuyuebianhao | varchar(200) | 是   | NULL              | 预约编号 |
| kefanghao    | varchar(200) | 是   | NULL              | 客房号   |
| ruzhushijian | datetime     | 是   | NULL              | 入住时间 |
| jiage        | varchar(200) | 是   | NULL              | 价格     |
| tianshu      | int(11)      | 是   | NULL              | 天数     |
| zongjia      | varchar(200) | 是   | NULL              | 总价     |
| yuyueshijian | datetime     | 是   | NULL              | 预约时间 |
| zhanghao     | varchar(200) | 是   | NULL              | 账号     |
| xingming     | varchar(200) | 是   | NULL              | 姓名     |
| shouji       | varchar(200) | 是   | NULL              | 手机     |
| shenfenzheng | varchar(200) | 是   | NULL              | 身份证   |
| sfsh         | varchar(200) | 是   | 否                | 是否审核 |
| shhf         | longtext     | 是   | NULL              | 审核回复 |
| ispay        | varchar(200) | 是   | 未支付            | 是否支付 |