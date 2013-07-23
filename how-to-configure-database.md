---
layout: default
title: How do I configure the database?
---

You shouldn’t normally need to do that, as Semaphore automatically inserts a working database.yml in your project, based on the database selected in your project’s settings. On top of that, project analysis usually inserts `rake db:setup` and `rake db:test:prepare` build commands, which is enough in most cases.

If you have or need to write a custom build script, you can use the database name and password specified by exported [environment variables](/available-environment-variables).
