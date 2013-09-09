---
layout: default
title: How do I build a project with private gems?
---

Either use a hosted private gem repository such as [Gemfury](http://www.gemfury.com/), or follow this procedure:

## - Get an OAuth Token from  GitHub

First you will need to get an OAuth Token from GitHub using your own username and "note"

{% highlight bash %}
$ curl -u 'masonforest' -d '{"scopes":["repo"], "note":"Semaphore CI private gem"}' https://api.github.com/authorizations
{% endhighlight %}


## - Authenticate bundler to GitHub via OAuth Token

Add this line to your Gemfile replacing "your_token" with the token you got from first step.
In this example we are installing the 'ventana' gem:

{% highlight bash %}
gem 'ventana', git: "https://your_token:x-oauth-basic@github.com/renderedtext/ventana.git"
{% endhighlight %}


# More secure alternative:

## Storing the OAuth token in an environment variable

For additional security you can store your OAuth token in an environment variable. This way your token is not included in your codebase which is insecure.
However this technique require form you to export OAuth token in your development enviromet too (Best way is to export it in ~/.zshrc or ~/.bashrc).

Change the line in your Gemfile to

{% highlight bash %}
gem 'ventana', git: "https://#{ENV['GITHUB_TOKEN']}:x-oauth-basic@github.com/thoughtbot/ventana.git"
{% endhighlight %}

Then export token on Semaphore using the token you got from above:

{% highlight bash %}
$ export GITHUB_TOKEN=your_token
{% endhighlight %}

Now bundle localy and you are ready to build on Semaphore!
