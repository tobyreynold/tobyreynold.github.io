---
layout: post
title:  "CentOS 7.0 Install nodejs environment"
date:   2016-04-05 23:01:07
categories: nodejs
---

1.准备工作

  一台sever，配置自己定
  nodejs安装包，下载地址：http://nodejs.org/dist/v4.4.2/node-v4.4.2.tar.gz (暂时稳定版本)

2.安装步骤  
{% highlight ruby %}
	# cat /etc/system-release 
		CentOS release 6.1 (Final) 
	# locale 
		LANG=en_US.UTF-8 ...
	# wget http://nodejs.org/dist/v4.4.2/node-v4.4.2.tar.gz
	# tar zxvf node-v4.4.2.tar.gz 
	# cd node-v4.4.2.tar.gz 
	# ./configure --prefix=/usr 
	# make 
	# make install 
{% endhighlight %}

3.安装express
  #npm -g install express forever supervisor

  #sudo npm install -g express-generator

  #express app

  install dependencies:
  #cd app && npm install

  run the app:
  #DEBUG=app:* npm start OR npm start

4. sever端搭建git仓库

  在sever端安装好git之后，客户端往服务端push代码会报错，类似如下错误：
   remote: error: refusing to update checked out branch: refs/heads/master
   remote: error: By default, updating the current branch in a non-bare repository
   remote: error: is denied, because it will make the index and work tree inconsistent
   remote: error: with what you pushed, and will require 'git reset --hard' to match
   remote: error: the work tree to HEAD.
   remote: error: 
   remote: error: You can set 'receive.denyCurrentBranch' configuration variable to
   remote: error: 'ignore' or 'warn' in the remote repository to allow pushing into
   remote: error: its current branch; however, this is not recommended unless you
   remote: error: arranged to update its work tree to match what you pushed in some
   remote: error: other way.
   remote: error: 
   remote: error: To squelch this message and still keep the default behaviour, set
   remote: error: 'receive.denyCurrentBranch' configuration variable to 'refuse'.


   #git config receive.denyCurrentBranch ignore 解决该问题。
   以后客户端push代码之后，服务端同步更新只要在sever端执行 git pull 就可以更新成最新代码。

  

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
