---
layout: default
title: Post-build webhooks
---

Semaphore allows you to set up webhooks that will receive payload about every finished build.  You can use them, for example, to implement alerts through [Hubot](http://hubot.github.com/), or keep track of your projects on a company dashboard.

To set up one or more webhooks for your project, follow these steps:

- Click on "settings" next to your project on the dashboard.

![Project settings](/assets/images/project-settings-link.png)

- Open the "Webhooks" tab on project settings page.

![Webhooks tab](/assets/images/webhooks-tab-link.png)

- Add a URL to receive the payload.

![Webhooks](/assets/images/webhooks.png)

- Click on "Test" to receive an example payload and verify that it all works.

- Save your settings.

### Payload format

Payload is JSON in the same structure as [build notification API](/branches-and-builds-api).

{% highlight javascript %}
{
  "branch_name": "gem_updates",
  "branch_url": "https://semaphoreapp.com/projects/44/branches/50",
  "project_name": "base-app",
  "build_url": "https://semaphoreapp.com/projects/44/branches/50/builds/15",
  "build_number": 15,
  "result": "passed",
  "started_at": "2012-07-09T15:23:53Z",
  "finished_at": "2012-07-09T15:30:16Z",
  "commit": {
    "id": "dc395381e650f3bac18457909880829fc20e34ba",
    "url": "https://github.com/renderedtext/base-app/commit/dc395381e650f3bac18457909880829fc20e34ba",
    "author_name": "Vladimir Saric",
    "author_email": "vladimir@renderedtext.com",
    "message": "Update 'shoulda' gem.",
    "timestamp": "2012-07-04T18:14:08Z"}
}
{% endhighlight %}

### Retry on failure

In case of a delivery failure, Semaphore will retry, twice, to send the webhook.
