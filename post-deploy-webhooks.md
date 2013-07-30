---
layout: default
title: Post-deploy webhooks
---

Semaphore allows you to set up webhooks that will receive payload about every finished deploy.  You can use them, for example, to implement alerts through [Hubot](http://hubot.github.com/), or keep track of your projects on a company dashboard.

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

Payload is JSON in the same structure as [deploy notification API](/servers-and-deploys-api).

{% highlight javascript %}
{
  "project_name": "heroku-deploy-test",
  "result": "passed",
  "server_name": "server-heroku-master-automatic-2",
  "number": 2,
  "created_at": "2013-07-30T13:52:33Z",
  "updated_at": "2013-07-30T13:53:21Z",
  "started_at": "2013-07-30T13:52:38Z",
  "finished_at": "2013-07-30T13:53:21Z",
  "html_url": "https://semaphoreapp.com/projects/2420/servers/81/deploys/2",
  "build_html_url": "https://semaphoreapp.com/projects/2420/branches/58394/builds/7",
  "commit": {
    "author_email": "rastasheep3@gmail.com",
    "author_name": "Aleksandar Diklic",
    "id": "43ddb7516ecc743f0563abd7418f0bd3617348c4",
    "message": "One more time",
    "timestamp": "2013-07-19T12:56:25Z",
    "url": "https://github.com/rastasheep/heroku-deploy-test/commit/43ddb7516ecc743f0563abd7418f0bd3617348c4"
  }
}
{% endhighlight %}

### Retry on failure

In case of a delivery failure, Semaphore will retry, twice, to send the webhook.
