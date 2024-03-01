//# network-libary
# 基于Reactor模式的多线程网络库
muduo网络库是一个高性能的基于Reactor模式的多线程网络库，采用one loop per thread + thread pool
的架构实现，能够帮助开发者轻松实现高并发、低延迟的网络应用程序。


亮点： 1、底层使用Epoll + LT 模式的I/O复用模型，并结合非阻塞I/O实现主从Reactor模型。
       2、采用one loop per thread 线程模型，并封装成线程池避免线程创建和线程销毁带来的性能开销。
       3、通过双缓冲区实现异步日志，由后端线程负责定时向磁盘写入前端日志信息，避免数据落盘时阻塞网络服务。

       
技术关键词：Reactor模式、线程池、异步日志
