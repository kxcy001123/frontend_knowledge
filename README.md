# 前端知识

#### 项目介绍
工作学习中遇到的一些知识，问题，记录
 
    1. mobx 数组越界， js数组不存在越界，js的数组是hash表，如果找不到会返回undefined
    2. csrf 跨站请求伪造，防御:http请求头 referer
    3. vue商城  https://github.com/willemwei/goods
    4. 阿里云部署node  https://help.aliyun.com/document_detail/50775.html
    5. 阿里云 nginx服务器   https://blog.csdn.net/chichengit/article/details/80807354（失败）
        缺少openssl文件关联，  https://blog.csdn.net/qq_30507287/article/details/69389982（解决办法）
         the "ssl" parameter requires ngx_http_ssl_module in /usr/local/nginx/conf/nginx.conf:35    解决办法  https://www.cnblogs.com/ghjbk/p/6744131.html
       (https://www.cnblogs.com/123cn/p/5752141.html)  成功
    6. [h5 与原生 app 交互的原理](https://mp.weixin.qq.com/s/oMTqMqZHAP3OSeysb1Efcg)
##### Nginx  相关
    1. nginx -t  检测配置文件语法错误，同时会显示主配置文件路径
       .default 这是备份文件，不起作用，很多项目都是这样
    2. nginx.conf  配置详细解释  (https://www.cnblogs.com/liang-wei/p/5849771.html)
##### Liunx命令
    ```
        ldd 查看动态库依赖关系

        ln 它的功能是为某一个文件或目录在另外一个位置建立一个同步的链接，类似Windows下的超级链接。
    ```
##### 前端工程化
    1. [babel相关](https://www.cnblogs.com/lsgxeva/p/7758184.html)
##### 
    Vue生命周期   https://mp.weixin.qq.com/s/4ukhHAcMQN07y0ssYqUeuA
    React 16+生命周期   https://mp.weixin.qq.com/s/Lp-pXHdg48d-TV0QsJOcwA
##### rem布局解析
 (https://juejin.im/post/5b90e07ce51d450e6a2dd140?utm_medium=fe&utm_source=weixinqun)
##### 前端面试知识点
   （https://juejin.im/post/5b94d8965188255c5a0cdc02）
##### 短连接
    (https://www.cnblogs.com/nullllun/p/6637844.html)
##### webpack
    (https://www.cnblogs.com/hezihao/p/8027843.html)