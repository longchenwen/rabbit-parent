# rabbitmq项目实战的封装


## 1.项目模块基本结构:
1. rabbit-parent:
  * 1.rabbit-api
  * 2.rabbit-common
  * 3.rabbit-core-producer
  * 4.rabbit-tast

## 简单封装rabbitmq 发送和消费消息,使用分布式定时器es-job做分布式定时任务

## [es-job官方网址](http://elasticjob.io/)

## 使用的工具:com.google.common.base.Preconditions
```
 Preconditions.checkNotNull(string); 检查是否为null
```
## 使用工具:com.google.common.base.Splitter
```
1.Splitter.on("#");切分的字符串
2.List<String> strings = splitter.splitToList("字符串")

```

## 序列化和反序列化

## 发送消息的确认消息完成

## 可靠性消息的投递
1. 消息信息储存在数据库,并设有消息储存的状态
  * 1.在insert消息成功的时候confirm方法在改变数据库里面的消息为成功的状态

2. 用定时任务查询状态的消息,并且改变状态

## 使用分布式定时器es-job做分布式定时任务-实现消息可靠性的投递做补偿,[es-job官方网址](http://elasticjob.io/)
1. es-job属于分布式定时任务
2. zookeeper做分布式锁

## ThreadeLocal的学习[参考博客](https://www.cnblogs.com/jiangxinlingdu/p/11055540.html)

## 延迟消息的发送

