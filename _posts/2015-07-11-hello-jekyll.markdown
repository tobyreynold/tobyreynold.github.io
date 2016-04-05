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
{% highlight shell %}
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

<div>
	<a href="https://www.baidu.com">百度</a>
	<button id='btn'>
		test
	</button>
</div>

<script type="text/javascript">
	var btn = document.getElementById("btn");
	btn.onclick = function() {
		alert(1);
	};
</script>


Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
