---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# 简介 

欢迎使用Musicwow API, 本文档描述了所有的Musicwow音乐窝APP后台接口，提供于MusicWoW iOS及Android客户端所用RESTful API。由于历史原因，musicwow部分接口来源于原外包团队(fanwe)，本文档也一并记录。

# 认证类型

## 认证类型

```shell
curl "http://dev.conwaysmusic.com/mapi/index.php？ctl=user_center&act=authent&itype=edu"
```

> 返回结果示例:

```json
{
  "status": 1,
  "error": "",
  "title": "印客认证",
  "user": {
    "id": "167182",
    "user_id": "167182",
    "investor_send_info": "",
    "authentication_type": "",
    "authentication_name": "",
    "identify_number": "",
    "contact": "",
    "from_platform": "",
    "wiki": "",
    "identify_positive_image": "",
    "identify_nagative_image": "",
    "identify_hold_image": "",
    "is_authentication": "0"
  },
  "authent_list": [
    {
      "id": "1",
      "name": "教师"
    },
    {
      "id": "2",
      "name": "机构"
    }
  ],
  "investor_send_info": ""
}
```

获取认证信息。

### HTTP 请求

`POST http://dev.conwaysmusic.com/mapi/index.php？ctl=user_center&act=authent&itype=edu`

### 请求参数

| Parameter    | Default | Description                                                  |
| ------------ | ------- | ------------------------------------------------------------ |

<aside class="notice">
更多返回错误代码请看首页的错误代码描述
</aside>

## 教师认证

```shell
curl "http://dev.conwaysmusic.com/mapi/index.php?ctl=user_center&act=attestation&itype=edu"
```

> 返回结果示例:

```json
 {
    "status": 1, 
    "error": ""
}
```

查询教师认证状态.

<aside class="notice">更多返回错误代码请看首页的错误代码描述</aside>

### HTTP 请求

`POST http://dev.conwaysmusic.com/mapi/index.php?ctl=user_center&act=attestation&itype=edu`

###请求方式
POST

### URL 参数
<table>
<tr><td>参数</td><td>必选</td><td>类型</td><td>说明</td></tr>
<tr><td>authentication_type</td><td>是</td><td>string</td><td>认证类型</td></tr>
<tr><td>authentication_name</td><td>是</td><td>string</td><td>认证名称</td></tr>
<tr><td>contact</td><td>	是</td><td>	string</td><td>	联系方式</td><</tr>
<tr><td>teaching_certificate</td><td>	是</td><td>	string</td><td>	教师资格证</td></tr>
<tr><td>education_certificate</td><td>	是</td><td>	string</td><td>	学历证书</td></tr>
<tr><td>identify_number</td><td>	是</td><td>	string</td><td>	身份证号码</td></tr>
<tr><td>identify_hold_image</td><td>	是</td><td>	string</td><td>	手持身份证照片</td></tr>
<tr><td>identify_positive_image</td><td>	是</td><td>	string</td><td>	身份证正面</td></tr>
<tr><td>identify_negative_image</td><td>	是</td><td>	string</td><td>	身份证反面</td></tr>
</table>

## 机构认证

```shell
curl "http://dev.conwaysmusic.com/mapi/index.php?ctl=user_center&act=attestation&itype=edu"
```

> 返回结果示例:

```json
{
    "status": 1, 
    "error": ""
}
```

查询机构认证信息.

### HTTP 请求

`POST http://dev.conwaysmusic.com/mapi/index.php?ctl=user_center&act=attestation&itype=edu`

### URL 参数
<table>
<tr><td>参数</td><td>必选</td><td>类型</td><td>说明</td></tr>
<tr><td>authentication_type</td><td>是</td><td>string</td><td>认证类型</td></tr>
<tr><td>authentication_name</td><td>是</td><td>string</td><td>认证名称</td></tr>
<tr><td>contact</td><td>是</td><td>string</td><td>联系方式</td><</tr>
<tr><td>business_license</td><td>是</td><td>string</td><td>营业资格证</td></tr>
<tr><td>identify_number</td><td>是</td><td>string</td><td>身份证号码</td></tr>
<tr><td>identify_positive_image</td><td>是</td><td>string</td><td>身份证正面</td></tr>
<tr><td>identify_negative_image</td><td>是</td><td>string</td><td>身份证反面</td></tr>
</table>

