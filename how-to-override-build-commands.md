---
layout: default
title: Is it possible to override build commands on some branches?
---

Yes. Since the environment variable BRANCH_NAME is [available](/available-environment-variables), you can add a new build command to your project settings such as:

{% highlight javascript %}
if [ "$BRANCH_NAME" = "acceptance-tests" ]; then bundle exec rake spec:acceptance ; fi
{% endhighlight %}
