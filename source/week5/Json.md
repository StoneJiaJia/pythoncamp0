##用Python解析Json
###JSON的格式
***
例子：https://api.douban.com/v2/book/user/ouyangzhiping/collections


#####1，对象：

{"count":20,"start":0,"total":1211,"collections":[{"status":"read","comment":"开智文库首本图书问世了！周日开智大会见！","updated":"2015-04-15 15:14:08","user_id":"2352991","tags":["开智文库","进化心理学","非言语"],"rating":{"max":5,"value":"5","min":0}

count对应的是20，start对应的是0，所以JSON的格式是：

{ 属性 : 值 , 属性 : 值 , 属性 : 值 }

#####2,数组是有顺序的值的集合。一个数组开始于"["，结束于"]"，值之间用","分隔。

[

{"status":"read","comment":"开智文库首本图书问世了！周日开智大会见！","updated":"2015-04-15 15:14:08","user_id":"2352991","tags":["开智文库","进化心理学","非言语"],"rating":{"max":5,"value":"5","min":0}


#####3, 值可以是字符串、数字、true、false、null，也可以是对象或数组。这些结构都能嵌套。

####4,Json示例：
1.打开例子的网页，怎么才能在python中打开呢

[问题解决源头](http://stackoverflow.com/questions/13921910/python-urllib2-receive-json-response-from-url)

         import urllib, json
         url = "https://api.douban.com/v2/book/user/ouyangzhiping/  collections"
         response = urllib.urlopen(url);
         data = json.loads(response.read())
         print data
         
2.有了Json数据结构，怎么解析出来呢？

首先，json基本上是key/value的，python中叫字典。既然是字典，那就应该按照字典的方式去读。将上面的data转为字典类型，这里用json模块的read方法。
