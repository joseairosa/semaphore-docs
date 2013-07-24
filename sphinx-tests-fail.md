---
layout: default
title: My Sphinx tests fail
---

If you are using Thinking Sphinx, make sure that that you run this command before your tests:

{% highlight bash %}
RAILS_ENV=test bundle exec rake ts:index
{% endhighlight %}

Than you can either run

{% highlight bash %}
RAILS_ENV=test bundle exec rake ts:start &
{% endhighlight %}

or use

{% highlight bash %}
ThinkingSphinx::Test.start
ThinkingSphinx::Test.stop
{% endhighlight %}

directly in the source code of your tests.
