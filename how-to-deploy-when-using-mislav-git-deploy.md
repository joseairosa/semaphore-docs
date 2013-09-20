---
layout: default
title: How to deploy when using mislav/git-deploy?
---

If you are using [mislav/git-deploy](https://github.com/mislav/git-deploy) for your deployment needs, when adding a new server on Semaphore, select deployment option “Using a deploy script” and adapt the following deploy commands:

{% highlight bash %}
echo {SERVER_PUBLIC_KEY} >> ~/.ssh/known_hosts # Add server's public key as to not get prompted to authorize the authenticity of the server.
git remote add production "user@example.com:/apps/myapp" # Add a remote to where you push your code on the server.
git push production master # Push to the branch that is currently checked out on the remote.
{% endhighlight %}
