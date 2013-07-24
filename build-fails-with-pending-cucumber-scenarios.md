---
layout: default
title: My build fails if I have pending Cucumber scenarios
---

This is by design – Cucumber returns with an error code if you have pending scenarios.

If you’d like to avoid this, tag the work-in-progress scenarios and exclude them from your build via `--tags ~tag-to-exclude`.
