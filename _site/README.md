# 如何搭建一个github.io的页面
## 安装Ruby

```
$ sudo apt-get install ruby-full
```

or

[下载Linux版：Ruby 2.6.5](https://cache.ruby-lang.org/pub/ruby/2.6/ruby-2.6.5.tar.gz)

解压命令：
```
$ tar -xvf ruby-2.6.5.tar.gz 
```
进入ruby-2.6.5目录：
```
$ cd ruby-2.6.5/
$ ./configure
$ make
$ sudo make install
$ ruby -v
```
## 安装RubyGems

[下载Linux版：RubyGems v3.0.6 ](https://rubygems.org/rubygems/rubygems-3.0.6.tgz)

解压命令：
```
$ tar -xvf rubygems-3.0.6.tgz
```
进入rubygems-3.0.6目录：
```
$ cd rubygems-3.0.6/
$ sudo ruby setup.rb
```
## 安装NodeJS

[下载Linux版：nodejs](https://nodejs.org/dist/v12.13.1/node-v12.13.1-linux-x64.tar.xz)

解压命令：
```
$ tar -xvf node-v12.13.1-linux-x64.tar.xz
```
编辑配置环境变量
```
$ vim .bash_profile
```
往 .bash_profile 新增环境变量
```
export NODE_HOME=/node-v12.13.1-linux-x64.tar.xz
export PATH=$PATH:$NODE_HOME/bin 
export NODE_PATH=$NODE_HOME/lib/node_modules
```
:wq 退出保存
```
$ source .bash_profile
$ node -v
```
## 创建一个jekyll项目
创建一个jekyll项目my_blog
```
$ jekyll new my_blog
```
项目结构

进入my_blog目录，输入下面命令，开启jekyll服务
```
$ jekyll serve
```
浏览器进入：http://127.0.0.1:4000/

推送到github上

```
$ git init
$ git add .
$ git commit -m "first commit"
$ git remote add origin https://github.com/RedBlueAlliance/Jekyll_test.github.io.git
$ git push -u origin master
```