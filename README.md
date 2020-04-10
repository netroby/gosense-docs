# GoSense

文档站点: https://gosense.netroby.com

Gosense 是一个用golang编写的 博客 软件, 示例站点 : https://www.netroby.com

用sqlite存储数据. [如果有需要，我们用 Amazon S3 存储文件上传.]

## 加入我们

### Telegram Channel (电报频道)


[https://t.me/gosensechan](https://t.me/gosensechan)

### Telegram Group (电报群组)


[https://t.me/gosenser](https://t.me/gosenser)




### 贡献文档


如果您想和我们一起，改善文档，可以订阅仓库

[https://github.com/netroby/gosense-docs](https://github.com/netroby/gosense-docs)

不需要掌握编程，只需要简单 文档写作知识，了解基础的Markdown 语法就可以加入进来。

## 需求

1. Linux，Windows，MacOSX x86或者x64


## Feature


1. AWS S3 file upload storage
2. RSS output
3. Powered by golang
4. Builtin groupcache, amazing fast
5. Less cpu, memory usage than (wordpress etc)

## Install

You need proxy to build golang programm. or you will failed to build your gosense.

just rename .env.dist to .env  and edit it ,change the http_proxy and https_proxy to your proxy server ip.

First clone this repository to you pc/mac/laptop.

```bash
git clone https://github.com/netroby/gosense.git
```

The vol directory contains templates, static resources(css, js), It will be mount by docker

Then rename `config.toml.dist` to `vol/config.toml`, and change admin password and aws sdk key, secret

You need golang and libc-dev, for ubuntu ,you may want install it via `apt-get install -y build-essential`


```
cd gosense
go get -u github.com/valyala/quicktemplate/qtc
go generate
cp config.toml.dist vol/config.toml
go run -v .
```


Once you docker up and running, you may access demo via http://127.0.0.1:18080

To login, you need visit http://127.0.0.1:18080/admin/login  (The password will be found in config.toml file)

To create blog , you can visit http://127.0.0.1:18080/admin/addblog

Remember change 127.0.0.1 to your docker hosting machine real ip address.


## License

We using MIT License, so feel free to change anything as you want.

## Donate me please

Your donate will help me improve the code quality. I need money to pay for food, water.

### Paypal donate

https://paypal.me/netroby

### Bitcoin donate

```
136MYemy5QmmBPLBLr1GHZfkES7CsoG4Qh
```
### Alipay donate

![Scan QRCode donate me via Alipay](https://www.netroby.com/assets/images/alipayme.jpg)

**Scan QRCode donate me via Alipay**


## News

### 2017-08-17

* We have a new document site https://gosense.netroby.com

### 2017-08-13

* Fix bugs in docker-compose, now you can start gosense via docker-compose up --build

### 2016-08-24

* Now you can run gosense using docker-compose

### 2015-10-31

* Add Cache for list and view page, now performance got better

### 2015-10-30

* Now gosense handle time better than before
* The search by keyword now working correct

### 2015-10-29

* The docker scripts now working perfect, you can easier deploy gosense 

### 2015-10-28

* Fix bug in add blog
* Now we can add, edit blog
* Fix SQL load


