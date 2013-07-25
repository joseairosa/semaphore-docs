---
layout: default
title: How do I build a project with private gems?
---

Either use a hosted private gem repository such as [Gemfury](http://www.gemfury.com/), or follow this procedure:

- Generate a new passwordless SSH key pair:

{% highlight bash %}
ssh-keygen -f /tmp/key -t dsa
{% endhighlight %}

- Put the content of `/tmp/key` into a secret gist on GitHub and name the file id_dsa.

- Put the content of `/tmp/key.pub` as a new deploy key in your [gem’s admin screen on GitHub](http://d.pr/i/qFcv).

- Go to your app’s project settings on Semaphore and add the following build commands before all:

{% highlight bash %}
mkdir -p ~/.ssh
cd ~/.ssh
wget https://raw.github.com/gist/.../id_dsa (this is the path you get through the "raw" link on gist's page)
chmod 600 id_dsa
cd -
{% endhighlight %}

Warning: GitHub secret gists offer security only through URL obscurity. We used GitHub gist simply to explain the process of using private gems.
