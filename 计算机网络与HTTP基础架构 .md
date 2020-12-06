# Record
编程记录

##计算机网络与HTTP基础架构 

回顾数据类型 IP由四个byte组成  一个byte的区间在 -127 ~ 128 之间 所有ip单个byte不会超过255

DNS 为域名解析 使得访问域名能找到ip地址

端口号是每个应用程序在电脑上定位的标识

HTTP协议默认端口为80 HTTPS协议默认端口为443

TCP协协议规定了字节发送与解析的规范

## response 常用方法

getHeaderNames() 获取响应头信息 K,V

/**
@param {String} HeaderName 响应头KEY
@return 信息
*/
getHeader(HeaderName) 获取指定响应头信息  


## request 常用方法与属性

属性
Referer 存放请求来源于哪个网站 得到 IP地址 || 域名

content-Typpe 获取响应类型


