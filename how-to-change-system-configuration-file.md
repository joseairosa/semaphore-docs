---
layout: default
title: How can I change /etc/hosts or another system configuration file?
---

If it’s short, this will do:

{% highlight bash %}
sudo sh -c "echo 'yourchange' >> /etc/hosts"
{% endhighlight %}

If it’s longer, we recommend saving your content in a private gist and then downloading via raw URL:

{% highlight bash %}
sudo sh -c "curl https://raw.github.com/gist/raw_url >> /etc/hosts"
{% endhighlight %}
