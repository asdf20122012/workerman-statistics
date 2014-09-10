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
proctitle
sysvshm
sysvsem
sysvmsg
libevent

 [更多请访问www.workerman.net](http://www.workerman.net/workerman-statistics)