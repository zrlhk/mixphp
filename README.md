<br>

<p align="center">
<img src="https://box.kancloud.cn/90f9b3c1d667aefa77b09ea1b7ffb054_120x120.png" alt="MixPHP">
</p>

<p align="center">高性能 • 轻量级 • 命令行</p>

<p align="center">
<img src="https://img.shields.io/badge/downloads-3.8k-green.svg">
<img src="https://img.shields.io/badge/platform-linux%20%7C%20win%20-lightgrey.svg">
<img src="https://img.shields.io/badge/size-172%20KB-green.svg">
</p>

## MixPHP是什么

MixPHP 是秉承 **"普及 PHP 常驻内存型解决方案，促进 PHP 往更后端发展"** 的理念而创造，采用 Swoole 扩展作为底层引擎，围绕常驻内存的方式而设计，架构设计简洁而有扩展性，开发可以很灵活，提供了 Web 开发 / 命令行开发所需的众多组件，参考了 Yii2 框架的设计思想，如果你使用过 Yii2 基本上可以立即上手。

框架最新源代码行数：**5497 行**，因此可以很容易的改造它，成为你们公司的专属框架。

## 与其他框架的比较

MixPHP 与传统 PHP 的 Web 框架非常不同，MixPHP 可以不需要 Web 服务器(Apache/PHP-FPM)，框架自带 MixHttpd 高性能HTTP服务器，传统的 PHP 应用程序中脚本结束后，所有的对象在请求后都将销毁，而 MixHttpd 不同，框架组件对象常驻于内存，减少对象反复创建销毁的性能损失，具有传统框架无法比拟的性能优势。

MixPHP 也不同于其他基于 Swoole 的微服务框架，只聚焦于微服务治理，MixPHP 定位于 Web 开发的更多领域，覆盖从初创到亿元级体量的技术诉求。

MixPHP 更像是传统 Web 框架的 [次世代](https://baike.baidu.com/item/%E6%AC%A1%E4%B8%96%E4%BB%A3/536193) 版本，拥有更高的性能又保留了快速开发的能力，还能完成传统框架不能想象或者很难实现的功能。

[MixPHP 并发性能全面对比测试](http://www.jianshu.com/p/f769b6be1caf)

## 核心特征

* 高性能：极简架构 + Swoole引擎，超过 Phalcon 这类 C 扩展框架的性能；
* 长连接：按进程保持的长连接，支持 Mysql/Redis；
* 服务器：框架自带 MixHttpd 替代 Apache/PHP-FPM 作为高性能HTTP服务器；
* 组件：基于组件的框架结构，可通用的 Web 编程框架；
* 自动加载：完全使用 Composer，统一且高效；
* 路由：底层全正则实现，性能高，配置简单；
* 模型：模型集成了使用简单但功能强大的验证器，支持多场景控制；
* 查询构造器：独创的 SQL 构造方法，可灵活优雅的构造复杂语句；
* 视图：使用 PHP 做模板引擎，支持布局、属性；
* 命令行：封装了完整的命令行开发环境，可开发定时任务、守护进程；
* 多进程：简易的多进程开发方式，充分利用多核性能，可处理大量数据；
* WebSocket：具备长连接开发能力，扩展了 PHP 开发领域；

## 文档

MixPHP开发指南：http://doc.mixphp.cn

## 环境要求

* PHP >= 5.4
* Swoole >= 1.7.18

## 快速开始

一键下载

```
$> php -r "copy('https://raw.githubusercontent.com/mixstart/mixphp/master/download.php', 'download.php');include 'download.php';"
```

输出如下：

```
download mixphp zip ... ok
unzip ... ok
clean temp files ... ok
Successful download to "/data/mixphp-master"
```

入口文件安装至：`/usr/local/bin`。

```
$> cd /data/mixphp-master
$> chmod 777 install.sh
$> ./install.sh
```

接下来启动 mix-httpd 服务器

```
$> mix-httpd service/start -d
```

如果一切顺利，运行到最后你将看到如下的输出：

```
                           _____
_______ ___ _____ ___ _____  / /_  ____
__/ __ `__ \/ /\ \/ / / __ \/ __ \/ __ \
_/ / / / / / / /\ \/ / /_/ / / / / /_/ /
/_/ /_/ /_/_/ /_/\_\/ .___/_/ /_/ .___/
                   /_/         /_/

[2017-11-20 14:41:32] Server    Name: mix-httpd
[2017-11-20 14:41:32] PHP    Version: 5.4.45
[2017-11-20 14:41:32] Swoole Version: 1.9.21
[2017-11-20 14:41:32] Listen    Addr: 127.0.0.1
[2017-11-20 14:41:32] Listen    Port: 9501
```

访问测试：

```
$> curl http://127.0.0.1:9501/
Hello World
```

## 下载

[MixPHP 发行版本](https://github.com/mixstart/mixphp/releases)

## 技术交流

作者微博：http://weibo.com/onanying ，关注最新进展     
官方QQ群：284806582，敲门暗号：phper

## 授权

开源项目的可持续发展离不开资金，MixPHP 希望通过出售授权来获得维持项目运行的资金。      
授权详情：http://mixphp.cn/wiki/licence 。
