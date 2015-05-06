##用Urllib抓取豆瓣API数据

###Urllib标准库
***
Urllib模块用来读取网上的数据
 
        import urllib2
        import json
        data = urllib2.urlopen(r'https://api.douban.com/v2/book/1220562')
        json = json.loads(dota.read())
        print json['rating']
        print json['images']['large']
        print json['summary']

###urlopen（）
urlopen主要用于打开url文件，然后就获得指定url的数据，接下来就如同在本地操作文件那样来操作。
