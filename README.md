# coin_spider
# 数据平台设计

爬虫和数据库
pyspider+mysql
数据源：
主要是coingecko，其他辅助（coinmarketcap,feixiaohao,tokenclub）

## 1 项目基础表coin_info
https://www.coingecko.com/en
抓取所有币种的基本信息，包括名称，价格，24小时涨跌幅，市值，流动性，，开发人员，社区活跃度，公众关注度，总得分等。

## 2项目详情表coin_detail
项目的详细信息
例如：
访问页面https://www.coingecko.com/en/coins/bitcoin/developer#panel
从Code Repository标签获取项目的github地址
或者
访问页面http://www.tokenclub.com/#/coin/bitcoin
发送请求https://block.cc/api/v1/coin/get?coin=bitcoin
解析json获取github地址

## 3项目代码基础表coin_git
从https://github.com/bitcoin/bitcoin
获取git的基本信息，fork,star,watch,commit,release,contributors等数目


## 4项目代码commit表coin_commit
例如：
从https://github.com/bitcoin/bitcoin/commits/master
获取代码提交的历史记录信息
commitId，用户名，commit信息，时间
