# binance-quant-robot
数字货币，币安Binance,BTC ETH DOGE SHIB 量化交易系统 火币


## 简介
这是一个数字货币量化交易系统，使用的Binance币安的交易API.

本系统采用双均线交易策略，两条均线出现金叉则买入，出现死叉则卖出。

如果你还没有币安账号：[注册页面](https://accounts.binancezh.io/zh-CN/register?ref=FJO3SX0X)（通过链接注册，享受交易返现优惠政策）

这世上，没有百分百赚钱的方式，量化交易策略只是一个辅助工具。

生死有命，富贵在天！币圈有风险，入市需谨慎！！


## 为什么选择币安交易所
交易的手续费看起来很少，但是随着交易次数逐步增多，手续费也是一笔不小的开支。
所以我选择了币安，手续费低的大平台交易所
> 火币手续费 Maker 0.2% Taker 0.2%

> 币安手续费 Maker 0.1% Taker 0.1% （加上BNB家持手续费低至0.075%）


如果你还没有币安账号：[注册页面](https://accounts.binancezh.io/zh-CN/register?ref=FJO3SX0X)（通过链接注册，享受交易返现优惠政策）


## 运行环境
python3

由于交易所的api在大陆无法访问，需要科学上网(若无，可用[muncloud](https://www.muncloud.dog/aff.php?aff=2302))


## 快速使用

1、获取币安API的 api_key 和 api_secret

申请api_key地址:

[币安API管理页面](https://www.binance.com/cn/usercenter/settings/api-management)


2、注册钉钉自定义机器人Webhook，用于推送交易信息到指定的钉钉群

[钉钉自定义机器人注册方法](https://m.dingtalk.com/qidian/help-detail-20781541)


3、修改app目录下的authorization文件

```
api_key='你的币安key'
api_secret='你的币安secret'
dingding_token = '申请钉钉群助手的token'   # 强烈建议您使用
```


4、交易策略配置信息 strategyConfig.py
设置你的配置信息：

```
# 均线, ma_x 要大于 ma_y
ma_x = 5
ma_y = 60

# 币安
binance_market = "SPOT"#现货市场
binance_coinBase = "USDT"#使用USDT作为基础币种，用于购买其他货币；
binance_tradeCoin = "DOGE"#交易目标是 DOGE 币，
kLine_type = '5m' # 15分钟k线类型，你可以设置为5分钟K线：5m;1小时为：1h;1天为：1d
```
当 kline 5 向上穿过 kline 60， 则执行买入。

当 kline 5 向下穿过 kline 60， 则执行卖出。

你可根据自己的喜好，调整 ma_x 和 ma_y 的值。 

你也可以调整 kLine_type ，来选择 5分钟K线、15分钟K线、30分钟K线、1小时K线、1天K线等；

不同的K线，最终效果也是不一样的。



5、运行程序(记得先开科学上网)
```
python robot-run.py
```



## 服务器部署
购买服务器，建议是海外服务器，可以访问币安API

### 我的配置：
Linux, 1核CPU, 2G内存(1G也可)

我是在阿里云购买的日本东京服务器(传说币安服务器就在东京)

也可选择 新加坡、香港服务器

[阿里云，新人优惠](https://www.aliyun.com/activity?userCode=zs5is7pi)

[阿里云，最新活动](https://www.aliyun.com/1111/new?userCode=zs5is7pi)

## 钉钉信息截图
![image](https://user-images.githubusercontent.com/18456518/119217054-3cdb3c80-bb0a-11eb-9f66-60eb974bca46.png)




## 可加WX进交流群
![image](https://user-images.githubusercontent.com/18456518/119216880-e8838d00-bb08-11eb-81b5-0addc8c40f88.png)








