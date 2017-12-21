# WangZheRongYao
Glory of Kings王者荣耀英雄信息资料的爬取

### 原创爬虫
>爬取以下内容         
    // 我最喜欢玩的英雄是诸葛亮，招牌英雄
   
   
- 保存英雄皮肤大图片 // 我感觉我写这个爬虫唯一好玩的就是爬取这个图片，我是不是好无聊:)
- 英雄技能分析　　　//目前只是提取了英雄
- 英雄出装
- 英雄属性说明等等等相关信息，多的信息自己提取.

### 目标网址
#### http://pvp.qq.com/web201605/herolist.shtml
- 分析页面　这一步最重要
- 1首先分析页面,发现页面response里面的数据和element页面的数据不一样，响应的数据是动态渲染的
- 2那我们不能直接提取详细英雄的url，然后找找有没有json数据的url　http://pvp.qq.com/web201605/js/herolist.json
- 3找到一个json数据的url,点开发现有英雄id相关的信息,　可以用英雄id构造英雄详细页面
- 4提取英雄详细页面的相关信息,大部分信息都可以直接xpath提取，少部分信息在json数据里面,比如铭文,所有装备等等
- 这三个json数据里面包含有所有的相关信息，可以从页面提取的id然后从里面找到对应的详细信息
       - http://pvp.qq.com/web201605/js/item.json
       - http://pvp.qq.com/web201605/js/summoner.json
       - http://pvp.qq.com/web201605/js/ming.json
- 5写代码,没啥技术含量,就是一些常规操作,OK
