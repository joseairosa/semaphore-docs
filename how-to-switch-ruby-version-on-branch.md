---
layout: default
title: How to switch Ruby version in a specific branch
---

As with [running branch-specific commands](/how-to-override-build-commands.md):

    if [ "$BRANCH_NAME" = "ruby-2" ]; then rbenv local 2.0.0-p247 ; fi 

You can find the list of available Ruby versions on our [version information](/version-information.textile) page.
