---
layout:     post
title:      "WebService的使用"
subtitle:   " \"所学知识的简单记录\""
date:       2019-03-25 14:49:00 UTC+8
author:     "王先虎"
header-img: "img/about-markdown/bg.jpg"
tags:
    - WebService
    - 学习
    - 笔记
---


webservice是分布式服务的一种，

## 1、为什么使用webservice

1. 跨平台调用 即不限操作系统可以互相调用
2. 跨语言调用 即可以不限语言互相调用
3. 可以远程调用 即可以不限区域远距离调用

## 2、java webservice服务端代码编写

服务端是服务的发布方

**代码**

``` java
import javax.jws.WebMethod;  
import javax.jws.WebService;  
import javax.xml.ws.Endpoint;  
@WebService  
public class WebServiceServer {  
	public String HelloWord(String name){  
		return "Hello: "+name;  
	}  
	@WebMethod(exclude=true)  
	public String HelloWord2(String name){  
		return"Hello: "+name;  
	}  
	public static void main(String[] args) {  
		Endpoint.publish("http://localhost:8080/helloWord",new HelloWebService());  
		System.out.println("serve ok");
	}  
}
```

**关于**

1. @WebService 注解用于定义webservice服务类
2. Endpoint 端点服务类，方法publish用于将webservice对象绑定到一个IP和端口上
3. @WebMethod(exclude=true) 用于注解webservice方法 ,exclude=true 表示不此方法不被发布
4. 代码可以随便写在任何类型的工程中

## 3、java webservice客户端代码的编写

客户端就是服务的调用方

客户端代码可以用eclipse自动生成不用怎样编写，只用调用就行

**自动生成操作**

1. 新建项目，任何类型项目均可（或者用之前写好的项目也可以）
2. 右键new->other->Web Service Client,点击next,Service definition内填写webservice地址(本例是http://localhost:8080/helloWord?wsdl)，点next,finish完成，代码会自动生成在工程中

**调用示例代码**

``` java
import java.rmi.RemoteException;
import javax.xml.rpc.ServiceException;
public class Test {
	public static void main(String[] args) {
		try {
			HelloWebService h = new HelloWebServiceServiceLocator().getHelloWebServicePort();
			String hw = h.helloWord("王先");
			System.out.println(hw);
		} catch (ServiceException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (RemoteException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}
}
```














