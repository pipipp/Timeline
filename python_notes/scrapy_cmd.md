# Scrapy Commands

## 全局命令： 
* [ scrapy startproject {project_name} ]                  - 创建爬虫项目  
* [ scrapy genspider {-t template} spider_name domain ]   - 创建爬虫文件  
* [ scrapy runspider {spider_file.py} ]                   - 直接通过运行.py文件来启动爬虫  
* [ scrapy shell {url} ]                                  - 打开scrapy-shell交互器（可以使用Selector进行调试）  
* [ scrapy fetch {url} ]                                  - 该命令会通过scrapy-downloader将网页的源代码下载并显示出来  
* [ settings ]                                            - 查看项目设置  
* [ version ]                                             - 查看版本
* [ view ]                                                - 该命令会将网页document内容下载下来，并且在浏览器显示出来（可以判断是否是Ajax请求）       

## 项目命令（项目命令只能在项目目录下使用）：
* [ scrapy crawl {spider_name} ]    - 启动爬虫程序  
* [ scrapy list ]                   - 显示项目中所有的爬虫  
* [ check ]                         - 用于检查代码是否有错误  
* [ edit ]                          - 编辑  
* [ parse ]                         - 解析调试  
* [ bench ]                         - 速度测试    

## 使用示例（如果命令显示无效，在命令前面加上“python -m”）： 
* [ scrapy startproject example ]                       - 创建名字为example的项目  
* [ cd example ]                                        - 切换到该项目  
* [ scrapy genspider sample_spider www.sample.com ]     - 创建名字为sample_spider的爬虫文件，并且初始域名为www.sample.com  
* [ scrapy crawl sample ]                               - 执行sample爬虫程序  
* [ scrapy crawl sample -o sample.json ]                - 保存输出结果到json文件（还有csv，xml，pickle，marshal，ftp等格式可以存取）  

## Tips：
* [ scrapy crawl sample --nolog ]           - 不打印日志  
* [ scrapy crawl sample --headers ]         - 打印响应头信息  
* [ scrapy crawl sample --no-redirect ]     - 不做跳转（禁止重定向）  

## shell调试：
* [ python3 -m scrapy shell ]       - 开启shell调试
* [ response.selector.xpath('') ]   - 使用xpath定位 
* [ response.selector.css('') ]     - 使用css定位
