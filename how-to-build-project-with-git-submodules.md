---
layout: default
title: How do I build a project with git submodules?
---

In you build commands you should add following lines as setup commands:

```
git submodule init
git submodule update
```

and as post-thread command add:

```
  git submodule deinit .
```

__Tip:__
Make sure that Semaphroe have premissions to clone your submodules repo. Please check docs about [private gems](http://docs.semaphoreapp.com/how-to-build-project-with-private-gems) where you can find more info about setting premisions for private repos.
