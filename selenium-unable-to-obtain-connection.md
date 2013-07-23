---
layout: default
title: Selenium tests are unable to obtain connection to Firefox
---

Make sure selenium-webdriver gem is at latest available version specified on rubygems.org.

Use

{% highlight bash %}
bundle update selenium-webdriver capybara
{% endhighlight %}

commit and push the resulting changes to `Gemfile.lock`.
