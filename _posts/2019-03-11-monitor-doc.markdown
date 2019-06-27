---
layout:     post
title:      "监控管理接口文档"
subtitle:   " \"\""
date:       2019-03-11 10:20:00 UTC+8
author:     "王先虎"
header-img: "img/post-bg-2015.jpg"
tags:
    - 项目
---

<p align="center"><font size='7'><b><a name='ml'>监控管理接口文档</a></b></font></p>

## <a>目录</a>

1. [设备](#aa1)      
2. [状态-开启](#aa2)
3. [状态-关闭](#aa3)
4. [状态-在线](#aa4)
5. [状态-离线](#aa5)
6. [状态-报警、故障、正常](#aa6)

---

## **<a href='#ml' name='aa1' >1\. 设备</a>**

### 接口功能

查询分类相关设备（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/sBShow](http://39.106.198.108:8140/cover-web/sBShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|entity|no|string|树一次分类|
|lx|yes|string|点选二次分类|
|street|no|string|搜索关键字|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/sBShow](http://39.106.198.108:8140/cover-web/sBShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1529,
		"coverId": null,
		"terminalId": 1363,
		"equipmentId": 2,
		"lockId": null,
		"street": "中国福建省福州市晋安区东浦路66号",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1552033218000,
		"installNum": null,
		"repairNum": null,
		"longitude": "119.320568",
		"latitude": "26.120483",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 5,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "IT01-YT12",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

## **<a href='#ml' name='aa2' >2\. 状态-开启</a>**

### 接口功能

查询带锁且锁是开启的设备（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/kQShow](http://39.106.198.108:8140/cover-web/kQShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|street|no|string|搜索关键字|
|entity|no|string|分类模糊字串|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/kQShow](http://39.106.198.108:8140/cover-web/kQShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1456,
		"coverId": null,
		"terminalId": null,
		"equipmentId": 3,
		"lockId": 209,
		"street": "中国北京市海淀区创业路8",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1551415382000,
		"installNum": null,
		"repairNum": null,
		"longitude": "116.316446",
		"latitude": "40.047213",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 16,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "LK01-YT04",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

## **<a href='#ml' name='aa3' >3\. 状态-关闭</a>**

### 接口功能

查询带锁且锁是关闭的设备（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/gBShow](http://39.106.198.108:8140/cover-web/gBShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|street|no|string|搜索关键字|
|entity|no|string|分类模糊字串|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/gBShow](http://39.106.198.108:8140/cover-web/gBShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1456,
		"coverId": null,
		"terminalId": null,
		"equipmentId": 3,
		"lockId": 209,
		"street": "中国北京市海淀区创业路8",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1551415382000,
		"installNum": null,
		"repairNum": null,
		"longitude": "116.316446",
		"latitude": "40.047213",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 16,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "LK01-YT04",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

## **<a href='#ml' name='aa4' >4\. 状态-在线</a>**

### 接口功能

查询带终端且终端状态是在线的设备（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/zXShow](http://39.106.198.108:8140/cover-web/zXShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|street|no|string|搜索关键字|
|entity|no|string|分类模糊字串|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/zXShow](http://39.106.198.108:8140/cover-web/zXShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1456,
		"coverId": null,
		"terminalId": null,
		"equipmentId": 3,
		"lockId": 209,
		"street": "中国北京市海淀区创业路8",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1551415382000,
		"installNum": null,
		"repairNum": null,
		"longitude": "116.316446",
		"latitude": "40.047213",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 16,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "LK01-YT04",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

## **<a href='#ml' name='aa5' >5\. 状态-离线</a>**

### 接口功能

查询带终端且终端状态是离线的设备（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/lXShow](http://39.106.198.108:8140/cover-web/lXShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|street|no|string|搜索关键字|
|entity|no|string|分类模糊字串|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/lXShow](http://39.106.198.108:8140/cover-web/lXShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1456,
		"coverId": null,
		"terminalId": null,
		"equipmentId": 3,
		"lockId": 209,
		"street": "中国北京市海淀区创业路8",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1551415382000,
		"installNum": null,
		"repairNum": null,
		"longitude": "116.316446",
		"latitude": "40.047213",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 16,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "LK01-YT04",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

## **<a href='#ml' name='aa6' >6\. 状态-报警、故障、正常</a>**

### 接口功能

查询设备状态（有权限筛选，有搜索优先级）

### URL

[http://39.106.198.108:8140/cover-web/cKShow](http://39.106.198.108:8140/cover-web/cKShow)

### 支持格式

json

### HTTP请求方式

post

### 请求参数

|参数|必选|类型|说明|
|:-----  |:-------|:-----|-----|
|street|no|string|搜索关键字|
|entity|no|string|分类模糊字串|
|lx|yes|string|所要查询设备状态的种类,其对应值zc(正常),bj（报警）,gz（故障）|

### 返回字段

|返回字段|字段类型|说明|
|:-----   |:------|:-----|
|coverterId|int|设备id|
|coverId|int|井盖id|
|terminalId|int|终端id|
|lockId|int|锁id|
|street|string|街道|
|longitude|string|经度|
|latitude|string|纬度|

### 接口示例

地址：[http://39.106.198.108:8140/cover-web/cKShow](http://39.106.198.108:8140/cover-web/cKShow)

``` javascript
{
	"coverTerminalList": [{
		"coverterId": 1529,
		"coverId": null,
		"terminalId": 1363,
		"equipmentId": 2,
		"lockId": null,
		"street": "中国福建省福州市晋安区东浦路66号",
		"technicalP": null,
		"stockNum": null,
		"coverState": "1",
		"enclosureId": null,
		"installDate": 1552033218000,
		"installNum": null,
		"repairNum": null,
		"longitude": "119.320568",
		"latitude": "26.120483",
		"repairDate": null,
		"photo": null,
		"guaraNum": null,
		"guaraDate": null,
		"userId": null,
		"companyId": 5,
		"mainNum": null,
		"warrantyDate": null,
		"entitysId": "IT01-YT11",
		"num1": null,
		"num2": null,
		"num3": null,
		"num4": null
	}]
}
```

注：

1. 权限筛选：是指根据不同权限查询用户名下或公司名下
2. 优先级：是指给设备上挂载的产品分级（有优先级就意味着忽略其他产品）
3. 锁状态转换：是指把设备上的状态放弃替换为相关联锁产品的状态
4. 搜索优先级：是指给相同关键字匹配表字段的先后顺序（先用户，再公司，最后街道）