---
layout: post
title: Footnote on VirtualHost in Apache2
---
I recently had to reinstall my web server. I got a really big problem when the virtualhost started overriding the default documentroot. So localhost would point to mysite.locahost etc. A really annoying problem. It turns out that you need to add the original server name first before defining any virutalhost domains. Or as it said on the Apache <a href="http://httpd.apache.org/docs/2.2/vhosts/name-based.html">webpage</a> under "Main host goes away"(someone should really work on that semantic)
<blockquote>"If you are adding virtual hosts to an existing web server, you must also create a &lt;VirtualHost&gt; block for the existing host."</blockquote>
So basically this is what you need to have in your virutalhost conf file

&lt;VirtualHost *:80&gt;
DocumentRoot "/Users/myuser/www/"
ServerName localhost
&lt;/VirtualHost&gt;

&lt;VirtualHost *:80&gt;
DocumentRoot "/Users/myuser/www/mysite/"
ServerName mysite.localhost
&lt;/VirtualHost&gt;
