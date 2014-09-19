所需环境
========

需要PHP版本不低于5.3，只需要安装PHP的Cli即可，无需安装PHP-FPM、nginx、apache
不能运行在Window平台

安装
=========

以ubuntu为例

安装PHP Cli
`sudo apt-get install php5-cli`

启动停止
=========

以ubuntu为例

启动
`sudo ./bin/workermand start`

重启启动
`sudo ./bin/workermand restart`

平滑重启/重新加载配置
`sudo ./bin/workermand reload`

查看服务状态
`sudo ./bin/workermand status`

停止
`sudo ./bin/workermand stop`


本人安装环境 PHP Version 5.3.6 NTS  FPM/FastCGI
依赖的扩展包:
posix 必须
pcntl 必须
proctitle 可选
sysvshm  可选
sysvsem  可选
sysvmsg  可选
libevent  可选


 [更多请访问www.workerman.net](http://www.workerman.net/workerman-statistics)
 压力测试
 测试环境：
系统：debian 6.0 64位
内存：64G
cpu：Intel(R) Xeon(R) CPU E5-2420 0 @ 1.90GHz （2颗物理cpu，6核心，2线程）
Workerman：开启200个Benchark进程
压测脚本：benchmark
业务：发送并返回hello字符串

 压测数据：
 短链接（每次请求完成后关闭链接，下次请求建立新的链接）:
    条件： 压测脚本开1000个并发线程模拟1000个并发用户，每个线程链接Workerman 10W次，每次链接发送1个请求
    结果： 吞吐量：3.5W/S ， cpu利用率：35% 

长链接（每次请求后不关闭链接，下次请求继续复用这个链接）:
    条件： 压测脚本开6000个并发线程模拟6000个并发用户，每个线程链接Workerman 1次，每个链接发送10W请求
    结果： 吞吐量：45W/S ， cpu利用率：67% 

内存：HHVM环境每个进程内存稳定在46M，无内存泄漏


 
 
 
