---
layout: default
title: Heroku add-on
---

[Semaphore](http://addons.heroku.com/semaphore) is an [add-on](http://addons.heroku.com) for providing Semaphore service to all Heroku users.

[Semaphore app](https://semaphoreapp.com) is a hosted continuous integration service for Ruby applications.

We’re designing it to be very easy to use, but if you need any help, we hope this document will give you all information which you need to use Semaphore with Heroku add-on


## Activating add-on

Semaphore add-on can be attached to a Heroku application on two ways:
  
<div class="callout" markdown="1">
A list of all plans available can be found [here](http://addons.heroku.com/semaphore).
</div>

- via Heroku interface at [add-on catalog](http://addons.heroku.com)

- via Heroku command-line interface with command `heroku addons:add`

```
  $ heroku addons:add semaphore
  -----> Adding semaphore to sharp-mountain-4005... done, v18 (free)
```

After installing Semaphore add-on the application should be configured to fully integrate with the application.
Next step is to access Semaphore through Heroku interface and run your first build.


## Using Semaphore with add-on

Using Semaphore is easy, just follow this simple steps:

- Authorize Github account
- Select project
- Select build commands
- Build

After adding Semaphore add-on to your application you are be able to access Semaphore via Heroku interface (Just click on add-on name on your application resources page).

### - Authorize Github account

First thing you must do is to chose would you like to build from private or public repository on github.

![Github authentication screen](/assets/images/heroku-addon-1.jpg)

After choosing repository, you will have to autorize your github account.

![Authorize github account](/assets/images/heroku-addon-2.jpg)

### - Select project

After authorizing github account, you are able to select which project and which branch you want to build.

![Select project](/assets/images/heroku-addon-3.jpg)

### - Select build commands

Semaphore will analyze your project and after that you are ready to build, select build commands for your project and Semaphore will run your builds every time you push to selected repository. If you add any branches later to your repository, we will detect that and you will be able to run tests for that branches too.

![Build settings](/assets/images/heroku-addon-4.jpg)

### - Build

When setup is done, you have simple interface for viewing status of your build. Here you can see current status, or find more about successful/failed build when build process completes.

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

Semaphore can build programs based on Ruby and Bundler. At the moment it fully supports the following:

__Database engines__

- PostgreSQL
- MySQL
- SQLite
- Redis
- MongoDB

__Test frameworks and backends__

- test/unit
- RSpec
- Cucumber
- Steak
- Capybara with Selenium
- Capybara Webkit
- Poltergeist and PhantomJS

You can also use any other, provided it’s configured in your bundle and you __add a custom build command__, including:

- Jasmine
- Minitest

To find more about supported application stack please visit [Semaphore Docs](http://docs.semaphoreapp.com/supported-stack).

## Support

Semaphore support and runtime issues should be logged with Heroku Support at [Heroku Support channels](support.heroku.com). Any non-support related issues or product feedback is welcome at [semaphore@renderedtext.com](semaphore@renderedtext.com) or via Twitter [@SemaphoreApp](http://twitter.com/semaphoreapp)

For more information about Semaphore visit [SemaphoreApp.com](https://semaphoreapp.com/) and [Semaphorore docs](http://docs.semaphoreapp.com/).