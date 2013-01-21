---
layout: default
title: Heroku add-on
---

[Semaphore](http://addons.heroku.com/semaphore) is an [add-on](http://addons.heroku.com) for providing Semaphore service to all Heroku users.

[Semaphore app](https://semaphoreapp.com) is a hosted continuous integration service for Ruby applications.

This document provides all the information you need in order to use Semaphore with your application hosted on Heroku.

## Activating the add-on

Semaphore add-on can be attached to a Heroku application on two ways:
  
<!-- <div class="callout" markdown="1">
A list of all plans available can be found [here](http://addons.heroku.com/semaphore).
</div> -->

- via Heroku web interface at [the add-on catalog](http://addons.heroku.com)

- via Heroku command-line interface with command `heroku addons:add`

```
  $ heroku addons:add semaphore
  -----> Adding semaphore to sharp-mountain-4005... done, v18 (free)
```

After installing Semaphore add-on the application should be configured to fully integrate with the application.
Next step is to access Semaphore through Heroku interface and run your first build.


## Using Semaphore with add-on

Using Semaphore is easy, just follow these steps:

- Connect with GitHub
- Select project
- Review build commands
- Build

After adding Semaphore add-on to your application you will be able to access Semaphore via Heroku interface, from your application resources page.

### - Connect with GitHub 

First thing you must do is to choose whether you'd like to build from a private or public repository on GitHub.


![GitHub authentication screen](/assets/images/heroku-addon-1.jpg)

Authorize Semaphore with your GitHub account.

![Authorize GitHub account](/assets/images/heroku-addon-2.jpg)

### - Select project

After authorizing GitHub account, you are able to select a project and branch that you want to build.

![Select project](/assets/images/heroku-addon-3.jpg)

### - Review build commands

Semaphore will analyze your project and present you a suggested configuration and build commands that will run every time you push to the selected repository. If necessary you can change the version of Ruby or build commands at this step.

![Build settings](/assets/images/heroku-addon-4.jpg)

### - Build

At this point, setup is complete and your build will begin. You can watch its' progress live or come back and view the logs later. Semaphore will automatically test your application every time you push to GitHub. New branches will be detected and built automatically.

![Build status](/assets/images/heroku-addon-5.jpg)

## Migrating between plans

Migrating between plans can be done:

- via Heroku interface at [add-on catalog](http://addons.heroku.com)

- via Heroku command-line interface with command `heroku addons:upgrade`

```
  $ heroku addons:upgrade semaphore:newplan
  -----> Upgrading semaphore:newplan to sharp-mountain-4005... done, v18 ($49/mo)
         Your plan has been updated to: semaphore:newplan
```

## Removing the add-on

<div class="warning" markdown="1">This will destroy all associated data and cannot be undone!</div>

Semaphore add-on can be removed:

- via Heroku interface at [add-on catalog](http://addons.heroku.com)
  
- via Heroku command-line interface with command `heroku addons:remove`

```
  $ heroku addons:remove semaphore
  -----> Removing semaphore from sharp-mountain-4005... done, v20 (free)
```

## Supported application stack

Semaphore can build programs based on Ruby and Bundler. To find out more about supported application stack please visit 
[Semaphore documentation](http://docs.semaphoreapp.com/supported-stack).

## Support

Semaphore support and runtime issues should be logged with Heroku Support at [Heroku Support channels](support.heroku.com). Any non-support related issues or product feedback is welcome at [semaphore@renderedtext.com](semaphore@renderedtext.com) or via Twitter [@SemaphoreApp](http://twitter.com/semaphoreapp)

For more information about Semaphore visit [SemaphoreApp.com](https://semaphoreapp.com/) and [Semaphore docs](http://docs.semaphoreapp.com/).