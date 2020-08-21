# rocketMq-consumer

#背景
实现动态新增消费者的需求，并且能根据准备的模板，将rocketmq读取到的内容解析后，赋值给模板，在做后续业务需要的处理

#作用
1.界面事先录入消费者信息，通过接口启动消费者或关闭消费者，起到动态新增消费、下线消费者的效果
2.从消息队列里获取到msg消息后，取其值赋给数据库事先录制好的模板中，转换对象格式（目前只支持双一维，可以扩展根据配置读取多维）

#注意
demo实现采用的是rocketMq服务推的方式（无法消费服务启动之前的数据），如果需要实现拉的方式，对应修改实现对象