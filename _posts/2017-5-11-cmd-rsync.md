---
layout: post
title: rsync
date:   2017-05-11 09:54:01 +0800
categories: cmd rsync
---

# sync remote dir with local dir via ssh

```
rsync -e ssh --progress -r alertservcie/ alertservcie_server:/console/www
```
