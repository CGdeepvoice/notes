# celery
1. 什么是celery？
   
   异步框架。是一个简单的，灵活可靠的分布式系统。当我们的代码运行时候，遇到一些耗时操作，可能会被阻塞，用户的响应就会延迟，就需要把这些耗时的任务从主体任务中分离出来。

2. 生产者消费者模式

    生产者负责生成消息，缓存到消息队列，消费者读取消息队列的消息并且执行。

消息队列和任务队列的区别。
都是进行排队，celery和rabbitmq有什么不同呢，消息队列传递的是消息，接收到消息就开始执行任务，可以进行解耦，削峰，注重的消息的吞吐量。而任务队列重点是执行异步的任务，复杂的耗时的任务放在任务队列，不适合高吞吐量的场景。