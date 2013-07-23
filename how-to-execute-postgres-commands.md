---
layout: default
title: How can I execute Postgres commands?
---

Add a build command which looks something like:

{% highlight bash %}
psql -c "anything" -d $DATABASE_NAME_TEST -P pager
{% endhighlight %}
