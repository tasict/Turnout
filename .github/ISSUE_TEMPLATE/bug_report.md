---
name: Bug report
about: Something in Turnout does not work as it should
title: ""
labels: bug
---

<!--
Issues are public. Leave out private keys, preshared keys, server addresses
(endpoints) and whole config files. If a config matters, describe it or
replace those values with placeholders.
-->

**macOS version**
<!-- Apple menu › About This Mac, for example 15.6 -->

**Turnout version**
<!-- Turnout › About Turnout -->

**Mac**
<!-- Apple silicon or Intel -->

**What you did**

**What you expected**

**What happened instead**

**Background service log**
<!--
The lines from around the time it happened:
  tail -n 100 /Library/Logs/cc.ctsite.turnout.daemon.log
Where Turnout keeps its logs: https://turnout.ctsite.cc/how-it-works.html#logs
-->

```
```

**App log**
<!--
  /usr/bin/log show --predicate 'subsystem == "cc.ctsite.turnout"' --last 1h
-->

```
```
