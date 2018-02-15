## mainroad-cn

mainroad-cn 是一个简单的响应式[Hugo](https://gohugo.io)主题，基于[Mainroad](https://github.com/Vimux/Mainroad)（其基于[MH Themes](https://www.mhthemes.com/)的[MH Magazine](https://wordpress.org/themes/mh-magazine-lite/) - WordPress主题）

具体的修改包括了更改默认字体，调整字号以适合中文显示（主要做的就是放大和调细字重来保证中文字看得清楚），把默认的Google自定义搜索换成了百度的，社交媒体换成了Github，Linkedin，新浪微博和知乎。评论系统选用了[gitalk](https://gitalk.github.io) 1.2.2，在其基础上添加了一个md5库来解决[长链接问题](https://github.com/gitalk/gitalk/issues/102)。

实际效果可以参考[我的博客](https://www.noobear.com)。

参考配置(yaml同理)：

~~~toml

baseurl = "/"
title = "站名"
languageCode = "zh-CN"
paginate = "10" # 列表页文章数
theme = "mainroad-cn"
hasCJKLanguage = true # 超级重要中文网站一定要开！！！

[Author] # 作者
    name = "张三"
    bio = "你好，我是张三。"
    copyright = "转载请著名出处"
    avatar = "img/avatar.png"

[Params]
    subtitle = "我的博客" # 大标题下的介绍
    description = "我的博客是一个技术博客" # meta标签中的介绍
    opengraph = true # Enable OpenGraph if true
    readmore = false # 显示阅读更多的按钮
    leftsidebar = false # 将右侧栏移动到左边
    authorbox = true # 显示作者窗口
    post_navigation = true # 导航栏（上一篇下一篇）
    postSections = ["post"] # 哪些分区显示在主页上
    #postSections = ["blog", "news"] # 多分区的情况
    dateformat = "2006-01-02" # 显示日期的格式

[Params.widgets]
    search = true # 是否显示“搜索”框
    recent_articles = true # 是否显示“最近文章”框
    recent_articles_num = 5 # 最近文章数
    categories = false # 是否显示“目录”框
    tags = true # 是否显示标签云
    tags_counter = false # 标签的出现频率统计

    # 当被设置的时候会显示“社交”框
    social_github = "username" # Github github.com/username
    social_linkedin = "username" # linkdin linkedin.com/in/username
    social_weibo = "username" # weibo.com/你的个性域名
    social_zhihu = "username" # zhihu.com/people/你的个性域名
    social_email = "example@example.com"

[Params.gitalk]
    clintID = "your_client_id"
    clientSecret = "your_client_secret"
    repo = "your_repo"
    owner = "your_github_id"
    admin = "your_github_id"

~~~
