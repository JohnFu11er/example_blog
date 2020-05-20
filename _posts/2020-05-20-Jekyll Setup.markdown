---
layout: post
title:  "Jekyll Setup"
date:   2020-05-20 08:28:15 -0400
categories: jekyll update
---

This build guide will prepare you to run Jekyll on CentOS<br/><br/>

STEPS:<br/>
* Provision a VM (Virtual Box)<br/>
* Install CentOS on the VM<br/>
* Add <your user> to the sudo user (wheel) group

{% highlight common %}
[user@localhost ~]$ su
# enter the super user password that you setup
[root@localhost your_user]#  usermod -aG wheel your_user
{% endhighlight %}
<br/>

* Add your_user to the /etc/sudoers file

{% highlight common %}
[root@localhost your_user]# visudo
# Scroll down to the bottom of the file
# Press “i” to insert text into the file
# Type the following line on a new line at the very bottom of the file:
your_user ALL=(ALL:ALL) ALL
# Write and exit the file by pressing:
"ctrl+C" and then “:wq” and hit enter
# Exit the super user by typing “exit” and hit enter
{% endhighlight %}
<br/>

* Update CentOS
{% highlight common %}
[your_user@localhost ~]$ sudo dnf update -y
{% endhighlight %}
<br/>

* Install supporting programs/extensions
{% highlight common %}
[your_user@localhost ~]$ sudo dnf install ruby
[your_user@localhost ~]$ sudo dnf install ruby-devel
[your_user@localhost ~]$ sudo dnf install redhat-rpm-config
[your_user@localhost ~]$ sudo dnf install gcc-c++
[your_user@localhost ~]$ sudo dnf install make
[your_user@localhost ~]$ sudo dnf install git
{% endhighlight %}
<br/>

* Install Jekyll

{% highlight common %}
[user@localhost ~]$ gem install bundler
[user@localhost ~]$ gem install Jekyll
{% endhighlight %}

* Addtional steps for class:<br/>
  * A github account will be required to follow along. If you don't already have one, one may be created at [github.com][github].<br/>
  * A text editor is optional, but installing Visual Studio Code on the CentOS VM is highly recommended. 

[github]: https://github.com