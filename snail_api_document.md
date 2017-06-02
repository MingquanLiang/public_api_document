# <center>Table of Contents</center>


[**介绍**](#0)  

[**API参考手册**](#1)  
&nbsp;&nbsp;&nbsp;&nbsp;[1、各家云产商的AKSK的管理操作](#1.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.1、添加某个云厂商的AKSK [AddAksk]](#1.1.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.2、删除某个AKSK [DeleteAksk]](#1.1.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.3、编辑/修改某个AKSK [EditAksk]](#1.1.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.4、查看已有的AKSK列表 [GetAkskList]](#1.1.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.5、获取某个AKSK的详细信息 [GetAksk]](#1.1.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[1.6、导入或重新覆盖某个AKSK下的云服务资源数据 [DumpAkskResourceData]](#1.1.6)  
&nbsp;&nbsp;&nbsp;[2、云服务器的管理操作](#1.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.1、购买云服务器 [AddCloudServer]](#1.2.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.2、批量删除云服务器 [BatchDeleteCloudServer]](#1.2.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.3、查看已有的云服务器列表 [GetCloudServerList]](#1.2.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.4、查看某台云服务器的详细信息 [GetCloudServer]](#1.2.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.5、开启一台/多台云服务器 [StartCloudServer]](#1.2.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.6、关闭一台/多台云服务器 [StopCloudServer]](#1.2.6)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.7、重启一台/多台云服务器 [RebootCloudServer]](#1.2.7)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.8、重装某台云服务器 [ReinstallCloudServer]](#1.2.8)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[2.9、获取某台云服务器可使用的系统镜像列表(用于重装系统) [GetCloudServerImageList]](#1.2.9)  
&nbsp;&nbsp;&nbsp;[3、弹性IP(EIP)的管理操作](#1.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.1、购买EIP [AddEip]](#1.3.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.2、批量删除一个/多个EIP [BatchDeleteEip]](#1.3.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.3、查看已有的EIP列表 [GetEipList]](#1.3.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.4、查看某个EIP的详细信息 [GetEip]](#1.3.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.5、绑定某个EIP到云服务 [EipBindCloudServer]](#1.3.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[3.6、解绑某个EIP [EipUnbindCloudServer]](#1.3.6)  
&nbsp;&nbsp;&nbsp;[4、共享带宽(BWS)的管理操作](#1.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.1、购买BWS [AddBws]](#1.4.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.2、批量删除一个/多个BWS [BatchDeleteBws]](#1.4.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.3、查看已有的BWS列表 [GetBwsList]](#1.4.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.4、查看某个BWS的详细信息 [GetBws]](#1.4.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.5、调整某个BWS的带宽 [EidtBws]](#1.4.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.6、将某个EIP绑定到BWS [BwsBindEip]](#1.4.6)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[4.7、将某个EIP从某个BWS中移除 [BwsUnbindEip]](#1.4.7)  
&nbsp;&nbsp;&nbsp;[5、业务线(产品线)对云服务资源的统一管理操作(以标签的形式)](#1.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.1、添加云服务器的业务线标签 [AddCloudServerLabel]](#1.5.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.2、添加EIP的业务线标签 [AddEipLabel]](#1.5.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.3、添加BWS的业务线标签 [AddBwsLabel]](#1.5.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.4、变更云服务器的业务线标签 [AlterCloudServerLabel]](#1.5.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.5、变更EIP的业务线标签 [AlterEipLabel]](#1.5.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.6、变更BWS的业务线标签 [AlterBwsLabel]](#1.5.6)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.7、查询业务线标签下的云服务器列表 [GetCloudServerListByLabel]](#1.5.7)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.8、查询业务线标签下的EIP列表 [GetEipListByLabel]](#1.5.8)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[5.9、查询业务线标签下的BWS列表 [GetBwsListByLabel]](#1.5.9)  
&nbsp;&nbsp;&nbsp;[6、其它辅助的管理操作](#1.6)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.1、查看已有的系统镜像(Image)列表 [GetImageList]](#1.6.1)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.2、查看已有的子网(Subnet)列表 [GetSubnetList]](#1.6.2)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.3、查看已有的链路(Line)列表 [GetLineList]](#1.6.3)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.4、查看已有的安全组(SecurityGroup)列表 [GetSecurityGroupList]](#1.6.4)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.5、查看已有的网卡(NetworkInterface)列表 [GetNetworkInterfaceList]](#1.6.5)  
&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;[6.6、查看各家云产商可用的地区(Region) [GetRegionList]](#1.6.6)  

[**附录**](#4)  
&nbsp;&nbsp;&nbsp;&nbsp;[附录A-错误信息](#4.1)
<br>
<br>

<h2 id='0'>介绍</h2>

&nbsp;&nbsp;&nbsp;&nbsp;**本文档主要提供云服务资源统一管理操作及其成本核算功能相关的API，接入的云服务资源包括云服务器，弹性IP和共享带宽三种。 其中，一期会接入ksyun(金山云)的云服务资源统一管理操作；二期将会实现接入qcloud(腾讯云)、aliyun(阿里云)的云服务资源，并提供资源的成本核算。**
 <br>
 <br>


<h2 id='1'>API参考手册</h2>

* **各家云产商的AKSK的管理操作** <br>
* **云服务器的管理操作** <br>
* **弹性IP(EIP)的管理操作** <br>
* **业务线(产品线)对云服务资源的统一管理操作(以标签的形式)** <br>
* **其它辅助的管理操作** <br>
  <br>
 <br>


<h2 id='1.1'> 1. 各家云产商的AKSK的管理操作</h2>

<h3 id='1.1.1'>1-1. 添加某个云厂商的AKSK [AddAksk]</h3>

* **Open API**
    
    Action=AddAksk&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/vendor/api/aksk/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| name      | string |  是 | AKSK的名称(描述) |
| access\_key\_id      | string |  是 | AKSK的access key |
| secret\_access\_key      | string |  是 | AKSK的secret key |
| vendor\_name      | string |  是 | AKSK属于的哪个云厂商 |

**注意：vendor_name的有效值暂时只包括ksyun(金山云)、qcloud(腾讯云)和aliyun(阿里云)**

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/vendor/api/aksk/
{
    "name": "张三的AKSK",
    "access_key_id": "AKsjaksjakjkwe3rifwrfjwf",
    "secret_access_key": "OEdjkhdjakdhjakfhjkwefhjkwehfjkwehfjkwebfdf3rjkh4k==",
    "vendor_name": "ksyun"
}


2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddAksk&Version=2017-03-28
{
    "name": "张三的AKSK",
    "access_key_id": "AKsjaksjakjkwe3rifwrfjwf",
    "secret_access_key": "OEdjkhdjakdhjakfhjkwefhjkwehfjkwehfjkwebfdf3rjkh4k==",
    "vendor_name": "ksyun"
}
```

```
Status： 201 Created

{
  "id": "1a6ab347-6a66-4dfe-a81f-770d6eff5789",
  "name": "张三的AKSK",
  "access_key_id": "AKsjaksjakjkwe3rifwrfjwf",
  "partial_secret_access_key": "OEd???k==",
  "vendor": "94cf1d90-c2ed-4d42-ab73-b2ffa91b8c8e",
  "vendor_name": "ksyun",
  "create_user": "e69200c3-82ff-4ab3-a4ce-3e787a56a9d9"
}
```

<br/>

<h3 id='1.1.2'>1-2. 删除某个AKSK [DeleteAksk]</h3>

注意：同时会删除由AKSK导入的资源数据

* **Open API**
    
    Action=DeleteAksk&Version=2017-03-28
    
* **API** 

    DELETE 127.0.0.1:8000/vendor/api/aksk/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(uuid) |  是 | AKSK的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
DELETE 127.0.0.1:8000/vendor/api/aksk/1a6ab347-6a66-4dfe-a81f-770d6eff5789/

2) Open API Request:
DELETE http://kog.api.ksyun.com?Action=DeleteAksk&Version=2017-03-28&id=1a6ab347-6a66-4dfe-a81f-770d6eff5789
```

```
Status： 204 No Content
```

<br/>

<h3 id='1.1.3'>1-3. 编辑/修改某个AKSK [EditAksk]</h3>

* **Open API**
    
    Action=EditAksk&Version=2017-03-28
    
* **API** 

    PATCH 127.0.0.1:8000/vendor/api/aksk/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(uuid) |  是 | AKSK的ID |
| name      | string |  否 | AKSK的名称(描述) |
| access\_key\_id      | string |  否 | AKSK的access key |
| secret\_access\_key      | string |  否 | AKSK的secret key |

* **Request/Response Example【请求/响应例子】**

```
1) API Request: 
PATCH 127.0.0.1:8000/vendor/api/aksk/1a6ab347-6a66-4dfe-a81f-770d6eff5789/
{
    "name": "张三修改的AKSK"
}

2) Open API Request:
PATCH http://kog.api.ksyun.com?Action=EditAksk&Version=2017-03-28
{
    "name": "张三修改的AKSK"
}
```

```
Status： 200 OK

{
  "id": "1a6ab347-6a66-4dfe-a81f-770d6eff5789",
  "name": "张三修改的AKSK",
  "access_key_id": "AKsjaksjakjkwe3rifwrfjwf",
  "partial_secret_access_key": "OEd???k==",
  "vendor": "94cf1d90-c2ed-4d42-ab73-b2ffa91b8c8e",
  "vendor_name": "ksyun",
  "create_user": "e69200c3-82ff-4ab3-a4ce-3e787a56a9d9"
}
```

<br/>

<h3 id='1.1.4'> 1-4. 查看已有的AKSK列表 [GetAkskList]</h3>

* **Open API**
    
    Action=GetAkskList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/vendor/api/aksk/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/vendor/api/aksk/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetAkskList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 2,
  "last_page": true,
  "data": [
    {
      "id": "73b13836-f5c5-42f7-b367-57843b07119e",
      "name": "王五的AKSK",
      "access_key_id": "AKsdnsacjdbfirr42dhkjdasdjwf",
      "partial_secret_access_key": "OEd???k==",
      "vendor": "94cf1d90-c2ed-4d42-ab73-b2ffa91b8c8e",
      "vendor_name": "ksyun",
      "create_user": "e69200c3-82ff-4ab3-a4ce-3e787a56a9d9"
    },
    {
      "id": "6fbd13fb-b1f6-4078-8066-55968d52dc63",
      "name": "李四的AKSK",
      "access_key_id": "AKsjaksjakjieudhkjdabfkadhasdjwf",
      "partial_secret_access_key": "OEd???k==",
      "vendor": "94cf1d90-c2ed-4d42-ab73-b2ffa91b8c8e",
      "vendor_name": "ksyun",
      "create_user": "e69200c3-82ff-4ab3-a4ce-3e787a56a9d9"
    }
  ]
}
```

<br/>

<h3 id='1.1.5'>1-5. 获取某个AKSK的详细信息 [GetAksk]</h3>

* **Open API**
    
    Action=GetAksk&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/vendor/api/aksk/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(uuid) |  是 | AKSK的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/vendor/api/aksk/1a6ab347-6a66-4dfe-a81f-770d6eff5789/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetAksk&Version=2017-03-28&id=1a6ab347-6a66-4dfe-a81f-770d6eff5789
```

```
Status： 200 OK

{
  "id": "1a6ab347-6a66-4dfe-a81f-770d6eff5789",
  "name": "张三修改的AKSK",
  "access_key_id": "AKsjaksjakjkwe3rifwrfjwf",
  "partial_secret_access_key": "OEd???k==",
  "vendor": "94cf1d90-c2ed-4d42-ab73-b2ffa91b8c8e",
  "vendor_name": "ksyun",
  "create_user": "e69200c3-82ff-4ab3-a4ce-3e787a56a9d9"
}
```

<br/>

<h3 id='1.1.6'>1-6. 导入或重新覆盖某个AKSK下的云服务资源数据 [DumpAkskResourceData]</h3>

* **Open API**
    
    Action=DumpAkskResourceData&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/vendor/api/aksk/{id}/dump\_resource\_data/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(uuid) |  是 | AKSK的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request: 
POST 127.0.0.1:8000/vendor/api/aksk/1da999df-3cfa-419c-98c8-363046a67055/dump_resource_data/

2) Open API Request:
POST http://kog.api.ksyun.com?Action=DumpAkskResourceData&Version=2017-03-28
{
    "id": "1da999df-3cfa-419c-98c8-363046a67055"
}
```

```
Status： 200 OK

{
  "dump_status": "done"
}
```

<br/>


<h2 id='1.2'> 2. 云服务器的管理操作</h2>

<h3 id='1.2.1'>2-1. 购买云服务器 [AddCloudServer]</h3>

* **Open API**
    
    Action=AddCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| aksk      | string(UUID) |  是 | AKSK的ID |
| region      | string |  是 | 各家云产商可用的地区名称 |
| image    | string(UUID) |  是 | 系统安装镜像(Image)的ID |
| subnet      | string(UUID) |  是 | 子网的ID |
| security_group      | string(UUID) |  是 | 安全组的ID |
| instance_password      | string(UUID) |  是 | 云服务器的开机密码，最短8个字符，最长32个字符，必须包含大小写英文字符和数字 |
| charge_type      | string |  是 | 收费方式，有效值为：Monthly(包年包月), Daily(按日月结) |
| instance_type      | string |  否 | 云服务器套餐类型, 对于是Ksyun的云服务器，默认是I1.1A |
| data\_disk_size      | interger |  否 | 数据盘的大小，单位为GB，如果没有指定则为相应套餐类型最小值 |
| max_count      | interger |  否 | 默认值为1 |
| min_count      | interger |  否 | 默认值为1 |
| purchase_time      | string |  否 | 只有charge_type为“Monthly”时有效，有效值范围为1~36，单位为月 |
| private\_ip_address      | string |  否 | 建议使用系统自动分配 |
| instance_name      | string |  否 | 新建的云服务器的名字 |
| instance\_name_suffix      | string |  否 | - |
| sriov\_net_support      | bool |  否 | 标识是否开启增强联网, 默认是false |

* **注意：由于各家云产商的云服务的套餐、计费方式等不尽相同，最好参照各家的云产商的云服务购买的API（目前只接入ksyun）**
* **ksyun（金山云）：https://docs.ksyun.com/read/latest/52/_book/oaRunInstances.html**


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/
{
    "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
    "region": "cn-shanghai-3",
    "image": "08af0966-8519-4dd6-9c86-299c7cd57d23",
    "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
    "security_group": "12d47bc2-8138-4e31-a7a4-b264c3ed08de",
    "instance_password": "Ksyun123456",
    "charge_type": "Monthly", 
    "instance_name": "my-centos6", 
    "purchase_time": 1, 
    "data_disk_size": 30
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddCloudServer&Version=2017-03-28
{
    "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
    "region": "cn-shanghai-3",
    "image": "08af0966-8519-4dd6-9c86-299c7cd57d23",
    "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
    "security_group": "12d47bc2-8138-4e31-a7a4-b264c3ed08de",
    "instance_password": "Ksyun123456",
    "charge_type": "Monthly", 
    "instance_name": "my-centos6", 
    "purchase_time": 1, 
    "data_disk_size": 30
}

```

```
Status： 201 Created

[
  {
    "instance_id": "70498b98-d704-4cc3-8d51-087bf47e9bf6",
    "name": "my-centos6"
  }
]
```

<br/>

<h3 id='1.2.2'>2-2. 批量删除云服务器 [BatchDeleteCloudServer]</h3>

* **Open API**
    
    Action=BatchDeleteCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/batch\_delete/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |

* **本接口支持批量操作，可以删除一台或者多台云服务器** 

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/batch_delete/
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b", 
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=BatchDeleteCloudServer&Version=2017-03-28
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b", 
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4",
    "success": true
  },
  {
    "reason": "OK",
    "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
    "success": true
  }
]
```

<br/>

<h3 id='1.2.3'>2-3. 查看已有的云服务器列表 [GetCloudServerList]</h3>

* **Open API**
    
    Action=GetCloudServerList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/cloud_server/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/cloud_server/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetCloudServerList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 18,
  "last_page": false,
  "data": [
    {
      "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
      "name": "test-abc",
      "instance_id": "ce562162-7916-4857-a3eb-8726cc29db02",
      "power_status": "active",
      "os": "centos-6.5",
      "cpu": 1,
      "memory": 1,
      "data_disk_size": 30,
      "data_disk_type": "SSD",
      "charge_type": "I1.1A",
      "private_ip": "172.31.32.6",
      "image": "f893edd7-dab8-4963-98c9-94ebf5b22a83",
      "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
      "eips": [],
      "associate_eips": [],
      "network_interfaces": [
        "cec7a695-9bd1-47e1-bd71-5c4a72fdffdf"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    ... 此处省略
   {
      "id": "53f7a4b1-a055-43e9-8bfc-92b35b31a45f",
      "name": "centos-67-a",
      "instance_id": "3bcbf46e-12b6-4bb4-ae10-5f942d3ca242",
      "power_status": "active",
      "os": "centos-6.7",
      "cpu": 2,
      "memory": 2,
      "data_disk_size": 50,
      "data_disk_type": "SSD",
      "charge_type": "I1.2A",
      "private_ip": "172.31.32.26",
      "image": "2990a197-8813-4291-809c-4a4f4836764b",
      "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
      "eips": [
        "d0e74d05-70a5-4905-b5bc-07577b39fddf"
      ],
      "associate_eips": [
        {
          "ip_address": "10.111.84.96",
          "id": "d0e74d05-70a5-4905-b5bc-07577b39fddf"
        }
      ],
      "network_interfaces": [
        "0e4365a0-9d02-43f0-ac12-174f29cd5b4b"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.2.4'>2-4. 查看某台云服务器的详细信息 [GetCloudServer]</h3>

* **Open API**
    
    Action=GetCloudServer&Version=2017-03-28&id={id}
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/cloud_server/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | 云服务器的ID |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/cloud_server/15a13159-e5cc-4e1a-8114-b42d1ab1174b/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetCloudServer&Version=2017-03-28
```

```
Status： 200 OK

{
  "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
  "name": "test-abc",
  "instance_id": "ce562162-7916-4857-a3eb-8726cc29db02",
  "power_status": "active",
  "os": "centos-6.5",
  "cpu": 1,
  "memory": 1,
  "data_disk_size": 30,
  "data_disk_type": "SSD",
  "charge_type": "I1.1A",
  "private_ip": "172.31.32.6",
  "image": "f893edd7-dab8-4963-98c9-94ebf5b22a83",
  "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
  "eips": [],
  "associate_eips": [],
  "network_interfaces": [
    "cec7a695-9bd1-47e1-bd71-5c4a72fdffdf"
  ],
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```


<h3 id='1.2.5'>2-5. 开启一台/多台云服务器 [StartCloudServer]</h3>

* **Open API**
    
    Action=StartCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/start/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/start/
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=StartCloudServer&Version=2017-03-28
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4",
    "success": true
  },
  {
    "reason": "OK",
    "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
    "success": true
  }
]
```


<h3 id='1.2.6'>2-6. 关闭一台/多台云服务器 [StopCloudServer]</h3>

* **Open API**
    
    Action=StopCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/stop/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/stop/
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=StopCloudServer&Version=2017-03-28
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4",
    "success": true
  },
  {
    "reason": "OK",
    "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
    "success": true
  }
]
```

<h3 id='1.2.7'>2-7. 重启一台/多台云服务器 [RebootCloudServer]</h3>

* **Open API**
    
    Action=RebootCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/reboot/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/reboot/
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=RebootCloudServer&Version=2017-03-28
{
    "id": [
            "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
            "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4"
        ]
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "a42609f2-5aad-4f68-bcb4-ffc1ead39fd4",
    "success": true
  },
  {
    "reason": "OK",
    "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
    "success": true
  }
]
```


<h3 id='1.2.8'>2-8. 重装某台云服务器 [ReinstallCloudServer]</h3>

* **Open API**
    
    Action=ReinstallCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/{id}/reinstall\_system/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | 云服务器的ID |
| image    | string(UUID) |  是 | 系统安装镜像(Image)的ID |
| instance_password      | string(UUID) |  是 | 云服务器的开机密码，最短8个字符，最长32个字符，必须包含大小写英文字符和数字 |

* **注意: 重装系统前，当前的云服务器必须关闭**

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/15a13159-e5cc-4e1a-8114-b42d1ab1174b/reinstall_system/
{
    "image": "080da356-f800-455f-ac18-ec1519998a86",
    "instance_password": "Ksyun111111"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=ReinstallCloudServer&Version=2017-03-28
{
    "image": "080da356-f800-455f-ac18-ec1519998a86",
    "instance_password": "Ksyun111111"
}
```

```
Status： 200 OK

{
  "instance_id": "ce562162-7916-4857-a3eb-8726cc29db02",
  "id": "15a13159-e5cc-4e1a-8114-b42d1ab1174b",
  "success": true
}
```

<h3 id='1.2.9'>2-9. 获取某台云服务器可使用的系统镜像列表(用于重装系统) [GetCloudServerImageList]</h3>

* **Open API**
    
    Action=GetCloudServerImageList&Version=2017-03-28&id={id}
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/cloud_server/{id}/image\_list/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | 云服务器的ID |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/cloud_server/15a13159-e5cc-4e1a-8114-b42d1ab1174b/image_list/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetCloudServerImageList&Version=2017-03-28&id= 15a13159-e5cc-4e1a-8114-b42d1ab1174b
```

```
Status： 200 OK

{
  "total_count": 70,
  "last_page": false,
  "data": [
    {
      "id": "066cdf09-1924-4aec-8f0b-372316b3ab05",
      "instance_id": "89b883de-70eb-4045-aab2-0784f7758c94",
      "name": "jumei_debian_7.11",
      "platform": "debian-7.11",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
        ... 此处省略
    {
      "id": "21a32e1f-0a39-4938-9d37-c1bd319d8b71",
      "instance_id": "a07a42d1-5ecf-450a-b997-294b7e219827",
      "name": "windows-2008_x86_en_20160726",
      "platform": "windows-2008",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h2 id='1.3'> 3. 弹性IP(EIP)的管理操作</h2>

<h3 id='1.3.1'>3-1. 购买EIP [AddEip]</h3>

* **Open API**
    
    Action=AddEip&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| aksk      | string(UUID) |  是 | AKSK的ID |
| region      | string |  是 | 各家云产商可用的地区名称 |
| line    | string(UUID) |  是 | 链路(Line)的ID |
| band_width      | interger |  是 | 带宽 |
| charge_type      | string |  是 | 计费方式，有效值为：Monthly(包年包月), Daily(按日月结), Peak(按峰值月结) |
| purchase_time      | interger |  否 | 购买时间 |

**注意：  
1） 对于ksyun的EIP，计费方式：包年包月Monthly，有到期时间，只能升带宽。按峰值月结Peak，无到期时间，可升降带宽。按日月结Daily，无到期时间，可升降带宽。  
2）对于ksyun的EIP，当charge_type为“Monthly”时，purchase_time为必要参数，单位为月**

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/
{
	"aksk": "1da999df-3cfa-419c-98c8-363046a67055",
	"line": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
	"region": "cn-shanghai-3",
	"band_width": 1,
	"charge_type": "Daily"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddEip&Version=2017-03-28
{
	"aksk": "1da999df-3cfa-419c-98c8-363046a67055",
	"line": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
	"region": "cn-shanghai-3",
	"band_width": 1,
	"charge_type": "Daily"
}
```

```
Status： 201 Created

{
  "id": "a3729998-d87e-4c86-b586-5d4da190f401",
  "instance_id": "d25538d7-deee-464d-8c31-c43b3cb1b769",
  "ip_address": "3.4.5.152",
  "band_width": 1,
  "line": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```

<br/>


<h3 id='1.3.2'>3-2. 批量删除一个/多个EIP [BatchDeleteEip]</h3>

* **注意 对于ksyun的EIP，如果EIP是绑定状态需要在删除之前进行解绑**


* **Open API**
    
    Action=BatchDeleteEip&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/batch\_delete/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | EIP的ID列表 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/batch_delete/
{
    "id": ["a3729998-d87e-4c86-b586-5d4da190f401"]	
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=BatchDeleteEip&Version=2017-03-28
{
    "id": ["a3729998-d87e-4c86-b586-5d4da190f401"]	
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "a3729998-d87e-4c86-b586-5d4da190f401",
    "success": true
  }
]
```

<br/>

<h3 id='1.3.3'>3-3. 查看已有的EIP列表 [GetEipList]</h3>

* **Open API**
    
    Action=GetEipList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/eip/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/eip/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetEipList&Version=2017-03-28

```

```
Status： 200 OK

{
  "total_count": 12,
  "last_page": false,
  "data": [
    {
      "id": "a3729998-d87e-4c86-b586-5d4da190f401",
      "instance_id": "d25538d7-deee-464d-8c31-c43b3cb1b769",
      "ip_address": "3.4.5.152",
      "band_width": 1,
      "line": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    ...此处省略
    {
      "id": "489a1f03-17ec-4a57-9e2e-dc379d070305",
      "instance_id": "7bc0dea3-e225-4499-9af4-0885ec8e799d",
      "ip_address": "10.111.85.67",
      "band_width": 2,
      "line": "c6588382-706d-4a87-9a50-64bc26e6872e",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.3.4'>3-4. 查看某个EIP的详细信息 [GetEip]</h3>

* **Open API**
    
    Action=GetEip&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/eip/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | EIP的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/eip/a3729998-d87e-4c86-b586-5d4da190f401/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetEip&Version=2017-03-28&id=a3729998-d87e-4c86-b586-5d4da190f401

```

```
Status： 200 OK

{
  "id": "a3729998-d87e-4c86-b586-5d4da190f401",
  "instance_id": "d25538d7-deee-464d-8c31-c43b3cb1b769",
  "ip_address": "3.4.5.152",
  "band_width": 1,
  "line": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```

<br/>

<h3 id='1.3.5'>3-5. 绑定某个EIP到云服务 [EipBindCloudServer]</h3>

* **Open API**
    
    Action=EipBindCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/{id}/associate\_cloud\_server/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | EIP的ID |
| cloud_server      | string(UUID) |  是 |  云服务器的ID |
| network_interface      | string(UUID) |  是 | 网卡的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/a3729998-d87e-4c86-b586-5d4da190f401/associate_cloud_server/
{
	"cloud_server": "f2620604-81b8-4d25-9c70-e8bac9de5582", 
	"network_interface": "3add1793-32bd-404a-b765-64af95e598cf"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=EipBindCloudServer&Version=2017-03-28
{
	"cloud_server": "f2620604-81b8-4d25-9c70-e8bac9de5582", 
	"network_interface": "3add1793-32bd-404a-b765-64af95e598cf"
}
```

```
Status： 200 OK

{
  "id": "a3729998-d87e-4c86-b586-5d4da190f401",
  "success": true,
  "reason: "OK"
}
```

<br>

<h3 id='1.3.6'>3-6. 解绑某个EIP [EipUnbindCloudServer]</h3>

* **Open API**
    
    Action=EipUnbindCloudServer&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/{id}/disassociate\_cloud\_server/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | EIP的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/a3729998-d87e-4c86-b586-5d4da190f401/disassociate_cloud_server/

2) Open API Request:
POST http://kog.api.ksyun.com?Action=EipUnbindCloudServer&Version=2017-03-28
{
    "id": "a3729998-d87e-4c86-b586-5d4da190f401"
}

```

```
Status： 200 OK

{
  "reason": "OK",
  "id": "a3729998-d87e-4c86-b586-5d4da190f401",
  "success": true
}
```

<br>

<h2 id='1.4'> 4. 共享带宽(BWS)的管理操作</h2>

<h3 id='1.4.1'>4-1. 购买BWS [AddBws]</h3>

* **Open API**
    
    Action=AddBws&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| aksk      | string(UUID) |  是 | AKSK的ID |
| region      | string |  是 | 各家云产商可用的地区名称 |
| line    | string(UUID) |  是 | 链路(Line)的ID |
| name      | string |  是 | BWS的名称 |
| band_width      | interger |  是 | 带宽 |
| charge_type      | string |  是 | 计费方式，有效值为：Daily(按日月结), Peak(按峰值月结) |

**注意：  
1） 对于ksyun的BWS，计费方式：共享带宽的计费类型，按峰值月结Peak，无到期时间，可以升配，可以降配（带宽）按日月结Daily，无到期时间，可以升配，可以降配。'
2）对于ksyun的BWS，其带宽的值为1-15000**

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/
{
	"aksk": "1da999df-3cfa-419c-98c8-363046a67055", 
	"line": "183426b4-385d-4b5e-8561-e04e527a1b96", 
	"region": "cn-shanghai-3",
	"name": "new-add-bws",
	"band_width": 2,
	"charge_type": "Daily"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddBws&Version=2017-03-28
{
	"aksk": "1da999df-3cfa-419c-98c8-363046a67055", 
	"line": "183426b4-385d-4b5e-8561-e04e527a1b96", 
	"region": "cn-shanghai-3",
	"name": "new-add-bws",
	"band_width": 2,
	"charge_type": "Daily"
}
```

```
Status： 201 Created

{
  "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
  "instance_id": "99038405-653a-4980-a011-9ad875b05c3c",
  "band_width": 2,
  "associate_eips": [],
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```

<br/>


<h3 id='1.4.2'>4-2. 批量删除一个/多个BWS [BatchDeleteBws]</h3>

* **注意：对于ksyun的BWS，在删除之前，需要确保当前的BWS没有绑定EIP，否则需要先解绑**

* **Open API**
    
    Action=BatchDeleteBws&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/batch\_delete/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | BWS的ID列表 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/batch_delete/
{
    "id": ["6c7ca940-8c69-441d-9550-1215ef29512f"]
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=BatchDeleteBws&Version=2017-03-28
{
    "id": ["6c7ca940-8c69-441d-9550-1215ef29512f"]
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
    "success": true
  }
]
```

<br/>

<h3 id='1.4.3'>4-3. 查看已有的BWS列表 [GetBwsList]</h3>

* **Open API**
    
    Action=GetBwsList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/bws/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/bws/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetBwsList&Version=2017-03-28

```

```
Status： 200 OK

{
  "total_count": 4,
  "last_page": true,
  "data": [
    {
      "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
      "name": "new-add-bws",
      "instance_id": "99038405-653a-4980-a011-9ad875b05c3c",
      "band_width": 2,
      "associate_eips": [],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    {
      "id": "41c96b21-5185-4dc4-8329-1fd2bd957932",
      "name": "qqqq",
      "instance_id": "3845a830-fa8d-4e3a-8cd0-61188af97dce",
      "band_width": 1,
      "associate_eips": [],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    {
      "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
      "name": "bws_test_2",
      "instance_id": "ccabad02-3460-48e8-ab65-c802b4d2483b",
      "band_width": 1,
      "associate_eips": [
        {
          "ip_address": "10.144.254.193",
          "id": "9f22bcfa-c379-4231-bf54-7fc8510953b4"
        }
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    {
      "id": "861bff92-f744-493e-aa7c-5d2e8ae8c1f1",
      "name": "bws_test",
      "instance_id": "28efa16e-eaae-401a-94dc-db058e34d982",
      "band_width": 3,
      "associate_eips": [],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.4.4'>4-4. 查看某个BWS的详细信息 [GetBws]</h3>

* **Open API**
    
    Action=GetBws&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/bws/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | BWS的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/bws/bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetBws&Version=2017-03-28&id=bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26

```

```
Status： 200 OK

{
  "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
  "name": "new-add-bws",
  "instance_id": "99038405-653a-4980-a011-9ad875b05c3c",
  "band_width": 2,
  "associate_eips": [],
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```

<br/>


<h3 id='1.4.5'>4-5. 调整某个BWS的带宽 [EditBws]</h3>

* **Open API**
    
    Action=EditBws&Version=2017-03-28
    
* **API** 

    PATCH 127.0.0.1:8000/cmdb/api/bws/{id}/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | EIP的ID |
| band_width      | interger |  是 |  带宽 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
PATCH 127.0.0.1:8000/cmdb/api/eip/a3729998-d87e-4c86-b586-5d4da190f401/
{
    "band_width": 3
}

2) Open API Request:
PATCH http://kog.api.ksyun.com?Action=EditBws&Version=2017-03-28
{
    "band_width": 3
}
```

```
Status： 200 OK

{
  "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
  "name": "new-add-bws",
  "instance_id": "99038405-653a-4980-a011-9ad875b05c3c",
  "band_width": 3,
  "associate_eips": [],
  "region": "cn-shanghai-3",
  "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
  "vendor_name": "ksyun"
}
```

<br>


<h3 id='1.4.6'>4-6. 将某个EIP绑定到BWS [BwsBindEip]</h3>

* **Open API**
    
    Action=BwsBindEip&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/{id}/add\_eip/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | BWS的ID |
| eip      | string(UUID) |  是 |  EIP的ID |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/6c7ca940-8c69-441d-9550-1215ef29512f/add_eip/
{
    "eip": "9f22bcfa-c379-4231-bf54-7fc8510953b4"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=BwsBindEip&Version=2017-03-28
{
    "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
    "eip": "9f22bcfa-c379-4231-bf54-7fc8510953b4"
}
```

```
Status： 200 OK

{
  "reason": "OK",
  "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
  "success": true
}
```

<br>

<h3 id='1.4.7'>4-7. 将某个EIP从某个BWS中移除 [BwsUnbindEip]</h3>

* **Open API**
    
    Action=BwsUnbindEip&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/{id}/delete\_eip/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | string(UUID) |  是 | BWS的ID |
| eip      | string(UUID) |  是 | EIP的ID |


* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/6c7ca940-8c69-441d-9550-1215ef29512f/delete_eip/
{
	"eip": "9f22bcfa-c379-4231-bf54-7fc8510953b4"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=BwsUnbindEip&Version=2017-03-28
{
    "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
    "eip": "9f22bcfa-c379-4231-bf54-7fc8510953b4"
}

```

```
Status： 200 OK

{
  "reason": "OK",
  "id": "6c7ca940-8c69-441d-9550-1215ef29512f",
  "success": true
}
```

<br>


<h2 id='1.5'> 5. 业务线(产品线)对云服务资源的统一管理操作(以标签的形式)</h2>

<h3 id='1.5.1'>5-1. 添加云服务器的业务线标签 [AddCloudServerLabel]</h3>

* **Open API**
    
    Action=AddCloudServerLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/add\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/add_entity_label/
{
	"id": [
		"2042c6d2-b905-449b-ba9e-a7f021171c4c", 
		"f2620604-81b8-4d25-9c70-e8bac9de5582"
		],
	"name": "projcet_name"
	
}


2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddCloudServerLabel&Version=2017-03-28
{
	"id": [
		"2042c6d2-b905-449b-ba9e-a7f021171c4c", 
		"f2620604-81b8-4d25-9c70-e8bac9de5582"
		],
	"name": "projcet_name"
	
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "2042c6d2-b905-449b-ba9e-a7f021171c4c",
    "success": true
  },
  {
    "reason": "OK",
    "id": "f2620604-81b8-4d25-9c70-e8bac9de5582",
    "success": true
  }
]
```

<br/>

<h3 id='1.5.2'>5-2. 添加EIP的业务线标签 [AddEipLabel]</h3>

* **Open API**
    
    Action=AddEipLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/add\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | EIP的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/add_entity_label/
{
	"id": [
		"3226bac8-3e8d-464a-a953-d7168f3e598d",
		"46bc7904-4e86-4d29-8a40-eb4d5b05725b", 
		"489a1f03-17ec-4a57-9e2e-dc379d070305", 
		"8450b1cc-d6eb-4149-ae0c-2f8da68e8353", 
		"975c54de-027b-4316-b593-aaa755451dc0", 
		"9f22bcfa-c379-4231-bf54-7fc8510953b4", 
		"bc5c275d-742b-4849-8f84-3923049dc15c", 
		"d0e74d05-70a5-4905-b5bc-07577b39fddf", 
		"d248ad08-2c44-4269-aa4a-5a1a6f7ae7af", 
		"d5be54ed-d4ea-42e5-b319-60b5d52061bb", 
		"d8619d4e-5da8-43a8-b474-d312cf9e9a59", 
		"f420fe09-9201-4449-b26c-802cfda1405b"
	],
	"name": "project-A"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddEipLabel&Version=2017-03-28
{
	"id": [
		"3226bac8-3e8d-464a-a953-d7168f3e598d",
		"46bc7904-4e86-4d29-8a40-eb4d5b05725b", 
		"489a1f03-17ec-4a57-9e2e-dc379d070305", 
		"8450b1cc-d6eb-4149-ae0c-2f8da68e8353", 
		"975c54de-027b-4316-b593-aaa755451dc0", 
		"9f22bcfa-c379-4231-bf54-7fc8510953b4", 
		"bc5c275d-742b-4849-8f84-3923049dc15c", 
		"d0e74d05-70a5-4905-b5bc-07577b39fddf", 
		"d248ad08-2c44-4269-aa4a-5a1a6f7ae7af", 
		"d5be54ed-d4ea-42e5-b319-60b5d52061bb", 
		"d8619d4e-5da8-43a8-b474-d312cf9e9a59", 
		"f420fe09-9201-4449-b26c-802cfda1405b"
	],
	"name": "project-A"
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "9f22bcfa-c379-4231-bf54-7fc8510953b4",
    "success": true
  },
  ... 此处省略
  {
    "reason": "OK",
    "id": "f420fe09-9201-4449-b26c-802cfda1405b",
    "success": true
  }
]
```

<br/>


<h3 id='1.5.3'>5-3. 添加BWS的业务线标签 [AddBwsLabel]</h3>

* **Open API**
    
    Action=AddBwsLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/add\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | BWS的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/add_entity_label/
{
	"id": ["bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26"],
	"name": "project abc"
}


2) Open API Request:
POST http://kog.api.ksyun.com?Action=AddBwsLabel&Version=2017-03-28
{
	"id": ["bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26"],
	"name": "project abc"
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
    "success": true
  }
]
```

<br/>



<h3 id='1.5.4'>5-4. 变更云服务器的业务线标签 [AlterCloudServerLabel]</h3>

* **Open API**
    
    Action=AlterCloudServerLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/cloud_server/alter\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | 云服务器的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/cloud_server/alter_entity_label/
{
	"id": [
		"2042c6d2-b905-449b-ba9e-a7f021171c4c", 
		"f2620604-81b8-4d25-9c70-e8bac9de5582"
		],
	"name": "projcet_xxx"
}


2) Open API Request:
POST http://kog.api.ksyun.com?Action=AlterCloudServerLabel&Version=2017-03-28
{
	"id": [
		"2042c6d2-b905-449b-ba9e-a7f021171c4c", 
		"f2620604-81b8-4d25-9c70-e8bac9de5582"
		],
	"name": "projcet_xxx"
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "2042c6d2-b905-449b-ba9e-a7f021171c4c",
    "success": true
  },
  {
    "reason": "OK",
    "id": "f2620604-81b8-4d25-9c70-e8bac9de5582",
    "success": true
  }
]
```

<br/>

<h3 id='1.5.5'>5-5. 变更EIP的业务线标签 [AlterEipLabel]</h3>

* **Open API**
    
    Action=AlterEipLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/eip/alter\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | EIP的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/eip/alter_entity_label/
{
	"id": [
		"3226bac8-3e8d-464a-a953-d7168f3e598d"],
	"name": "project-haha"
}

2) Open API Request:
POST http://kog.api.ksyun.com?Action=AlterEipLabel&Version=2017-03-28
{
	"id": [
		"3226bac8-3e8d-464a-a953-d7168f3e598d"],
	"name": "project-haha"
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "3226bac8-3e8d-464a-a953-d7168f3e598d",
    "success": true
  }
]
```

<br/>


<h3 id='1.5.6'>5-6. 变更BWS的业务线标签 [AlterBwsLabel]</h3>

* **Open API**
    
    Action=AlterBwsLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/alter\_entity\_label/

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| id      | list |  是 | BWS的ID列表 |
| name      | string |  是 | 业务线标识 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
POST 127.0.0.1:8000/cmdb/api/bws/alter_entity_label/
{
	"id": ["bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26"],
	"name": "new project name"
}


2) Open API Request:
POST http://kog.api.ksyun.com?Action=AlterBwsLabel&Version=2017-03-28
{
	"id": ["bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26"],
	"name": "new project name"
}
```

```
Status： 200 OK

[
  {
    "reason": "OK",
    "id": "bbdd3cfc-f85a-40cf-8ce9-9d595fc51e26",
    "success": true
  }
]
```

<br/>


<h3 id='1.5.7'>5-7. 查询业务线标签下的云服务器列表 [GetCloudServerListByLabel]</h3>

* **Open API**
    
    Action=GetCloudServerListByLabel&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/eip/get\_entity\_list\_by\_label/?name={name}

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| name      | string |  是 | 业务线标识 |
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/cloud_server/get_entity_list_by_label/?name=projcet_xxx

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetCloudServerListByLabel&Version=2017-03-28&name=projcet_xxx
```

```
Status： 200 OK

{
  "total_count": 2,
  "last_page": true,
  "data": [
    {
      "id": "2042c6d2-b905-449b-ba9e-a7f021171c4c",
      "name": "my-centos",
      "instance_id": "c964da91-1ebc-4888-85d9-68e7be676c4b",
      "power_status": "active",
      "os": "centos-6.5",
      "cpu": 1,
      "memory": 1,
      "data_disk_size": 0,
      "data_disk_type": "SSD",
      "charge_type": "I1.1A",
      "private_ip": "172.31.32.12",
      "image": "08af0966-8519-4dd6-9c86-299c7cd57d23",
      "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
      "eips": [],
      "associate_eips": [],
      "network_interfaces": [
        "6090b0ac-5551-4154-80a9-73ed7f2557cf"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    {
      "id": "f2620604-81b8-4d25-9c70-e8bac9de5582",
      "name": "my-centos6",
      "instance_id": "70498b98-d704-4cc3-8d51-087bf47e9bf6",
      "power_status": "active",
      "os": "centos-6.5",
      "cpu": 1,
      "memory": 1,
      "data_disk_size": 0,
      "data_disk_type": "SSD",
      "charge_type": "I1.1A",
      "private_ip": "172.31.32.37",
      "image": "08af0966-8519-4dd6-9c86-299c7cd57d23",
      "subnet": "5f4fd4ff-9be1-4561-918d-c79a1d5e7a76",
      "eips": [
        "a3729998-d87e-4c86-b586-5d4da190f401"
      ],
      "associate_eips": [],
      "network_interfaces": [
        "3add1793-32bd-404a-b765-64af95e598cf"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.5.8'>5-8. 查询业务线标签下的EIP列表 [GetEipListByLabel]</h3>

* **Open API**
    
    Action=GetEipListByLabel&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/eip/get\_entity\_list\_by\_label/?name={name}

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| name      | string |  是 | 业务线标识 |
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/eip/get_entity_list_by_label/?name=project-A

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetEipListByLabel&Version=2017-03-28&name=project-A

```

```
Status： 200 OK

{
  "total_count": 11,
  "last_page": false,
  "data": [
    {
      "id": "46bc7904-4e86-4d29-8a40-eb4d5b05725b",
      "instance_id": "3a5de9d1-c5a4-4459-8cff-96879cea8c53",
      "ip_address": "10.111.84.124",
      "band_width": 2,
      "line": "c6588382-706d-4a87-9a50-64bc26e6872e",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    ...此处省略
    {
      "id": "d8619d4e-5da8-43a8-b474-d312cf9e9a59",
      "instance_id": "5b897054-2f1c-47c1-a45a-ba07ea94bd4c",
      "ip_address": "10.111.84.67",
      "band_width": 2,
      "line": "c6588382-706d-4a87-9a50-64bc26e6872e",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>


<h3 id='1.5.6'>5-9. 查询业务线标签下的BWS列表 [GetBwsListByLabel]</h3>

* **Open API**
    
    Action=GetBwsListByLabel&Version=2017-03-28
    
* **API** 

    POST 127.0.0.1:8000/cmdb/api/bws/get\_entity\_list\_by\_label/?name={name}

* **Parameters【参数列表】**

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| name      | string |  是 | 业务线标识 |
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/bws/get_entity_list_by_label/?name=sasa

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetBwsListByLabel&Version=2017-03-28&name=sasa

```

```
Status： 200 OK

{
  "total_count": 0,
  "last_page": true,
  "data": []
}
```

<br/>




<h2 id='1.6'> 6. 其它辅助的管理操作</h2>

<h3 id='1.6.1'> 6-1. 查看已有的镜像列表 [GetImageList]</h3>

* **Open API**
    
    Action=GetImageList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/image/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/image/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetImageList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 70,
  "last_page": false,
  "data": [
    {
      "id": "066cdf09-1924-4aec-8f0b-372316b3ab05",
      "instance_id": "89b883de-70eb-4045-aab2-0784f7758c94",
      "name": "jumei_debian_7.11",
      "platform": "debian-7.11",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
          ... 此处省略
    {
      "id": "21a32e1f-0a39-4938-9d37-c1bd319d8b71",
      "instance_id": "a07a42d1-5ecf-450a-b997-294b7e219827",
      "name": "windows-2008_x86_en_20160726",
      "platform": "windows-2008",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.6.2'> 6-2. 查看已有的子网(Subnet)列表 [GetSubnetList]</h3>

* **Open API**
    
    Action=GetSubnetList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/subnet/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/subnet/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetSubnetList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 5,
  "last_page": true,
  "data": [
    {
      "id": "1969d95b-fc87-4c3c-8a74-4a3058804110",
      "instance_id": "98053d59-1326-4bde-904e-6505d091e5ae",
      "name": "Subnet2",
      "subnet_type": "Normal",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
        ... 此处省略
    {
      "id": "e9e47bf3-61d3-47fc-aa5d-7dad62d13f2a",
      "instance_id": "c28eb0af-f5e5-43cd-8b32-16073fcd54b1",
      "name": "终端子网",
      "subnet_type": "Reserve",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.6.3'> 6-3. 查看已有的链路(Line)列表 [GetLineList]</h3>

* **Open API**
    
    Action=GetLineList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/line/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/line/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetLineList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 9,
  "last_page": true,
  "data": [
    {
      "id": "149e5b28-e708-4b59-9203-e813e8a6d2c6",
      "instance_id": "8bb4238b-209e-4d62-9af3-36fb1fb8e9ca",
      "name": "BGP",
      "line_type": "Public",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
        ... 此处省略
    {
      "id": "c7a03f57-57fb-4045-b922-535ce9cea549",
      "instance_id": "1e4ac9e7-6c0c-4ff7-93cd-c736be6969f2",
      "name": "tmp-test-xie-0308",
      "line_type": "Public",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.6.4'> 6-4. 查看已有的安全组(SecurityGroup)列表 [GetSecurityGroupList]</h3>

* **Open API**
    
    Action=GetSecurityGroupList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/security_group/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/security_group/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetSecurityGroupList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 2,
  "last_page": true,
  "data": [
    {
      "id": "12d47bc2-8138-4e31-a7a4-b264c3ed08de",
      "instance_id": "ae40962e-96b3-4307-85c3-0451104e7267",
      "name": "金山",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
    {
      "id": "6b72cfae-d5e1-4995-9ea9-acc51279278a",
      "instance_id": "3366ef91-81d4-411d-aac9-d8fbdb2edf76",
      "name": "DefaultSG",
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.6.5'> 6-5. 查看已有的网卡(NetworkInterface)列表 [GetNetworkInterfaceList]</h3>

* **Open API**
    
    Action=GetNetworkInterfaceList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/cmdb/api/network_interface/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
| page_size      | int |  否 | 每页显示多少条数据，默认是10，最大值是100 |
| page      | int |  否 | 查询第几页，默认值为1。当page为0时则返回全部的数据 |

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/cmdb/api/network_interface/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetNetworkInterfaceList&Version=2017-03-28
```

```
Status： 200 OK

{
  "total_count": 21,
  "last_page": false,
  "data": [
    {
      "id": "0283ce0a-2fa5-4d88-9b71-e89f9d0ccd73",
      "instance_id": "81bfdb28-ece9-4c01-a8c6-37e6b12c7c98",
      "network_interface_type": "primary",
      "mac_address": "fa:16:3e:3d:ca:4d",
      "security_groups": [
        "12d47bc2-8138-4e31-a7a4-b264c3ed08de"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    },
       ... 此处省略
    {
      "id": "b16774e9-dddd-4c69-8b62-62ce81289d51",
      "instance_id": "521e21ee-60aa-4270-a618-b2737594a17c",
      "network_interface_type": "primary",
      "mac_address": "fa:16:3e:05:a8:b8",
      "security_groups": [
        "12d47bc2-8138-4e31-a7a4-b264c3ed08de"
      ],
      "region": "cn-shanghai-3",
      "aksk": "1da999df-3cfa-419c-98c8-363046a67055",
      "vendor_name": "ksyun"
    }
  ]
}
```

<br/>

<h3 id='1.6.6'> 6-6. 查看各家云产商可用的地区(Region) [GetRegionList]</h3>

* **Open API**
    
    Action=GetRegionList&Version=2017-03-28
    
* **API** 

    GET 127.0.0.1:8000/vendor/api/region/

* **Parameters【参数列表】** 

| 参数名称  | 参数类型  | 是否必要 | 参数说明
|:-------------:|:---------------:| :-------------:|:-------------:|
暂无

* **Request/Response Example【请求/响应例子】**

```
1) API Request:
GET 127.0.0.1:8000/vendor/api/region/

2) Open API Request:
GET http://kog.api.ksyun.com?Action=GetRegionList&Version=2017-03-28
```

```
Status： 200 OK

{
  "ksyun": [
    "cn-beijing-6",
    "cn-beijing-2"
  ],
  "aliyun": [],
  "qcloud": []
}
```

<br/>

---
---

<h2 id='4'>附录</h2>
<h3 id='4.1'>附录A-错误信息</h3>

调用接口失败，不会返回结果数据；HTTP请求返回一个4xx或5xx的HTTP状态码，返回的HTTP消息体中包含具体的错误代码(code)及错误信息(message)等信息。

错误信息会以json格式进行返回，eg：

``` 
{
  "RequestId": "36fa40a1-b983-4bef-8f19-34c30530e9b7",
  "Error": {
    "Data": null,
    "Message": "Lack of Required Parameter: '\"u'vendor_name'\"'",
    "Code": "LackRequiredParameterError",
    "Type": "Response"
  }
}
```

**公共错误**

| 错误代码(Code)  | 错误消息(Message)  | HTTP状态码 | 中文描述(语义)
|:-------------:|:---------------:| :-------------:|:-------------:|
| LackRequiredParameterError      | Lack of Required Parameter: %s |  400 | 请求缺少必要的参数 |
| InputParameterTypeError      | An invalid or out-of-range value for parameter: %s |  400 | 输入的参数类型错误或不是有效值 |
| ServiceAccessNotImplementedError      | Target access service is still in progress: %s |  503 | 标识访问的云厂商服务还没接入完成 |
| InvalidQueryParameter      | Query instance does not exist: %s |  400 | 没有找到相应的实例 |
| KscoreClientError      | Call Kscore Client Error |  400 | 调用ksyun服务出错 |
| Exception      | %s |  500 | 未知的异常 |

