---
title:  "The Future"
date:   2025-01-26 10:00:00 -0600
categories: examples
permalink: /hello-from-the-future/
---

TODO: Investigate difference between local env and prod.  The future flag in `_config.yml` doesn't seem to be working on prod.  
Ah, this seems to be the problem:  
https://github.com/actions/jekyll-build-pages/issues/9

What happens if I set the publish date in the future?

Oooh, it looks like Jekyll is smart enough to not display future-dated articles.  It seems to be based on the Front Matter date field, not the date in the file name.

Ah, but GH Pages sets the `future` flag by default, so you have to override it.  
https://github.com/github/pages-gem/blob/master/lib/github-pages/configuration.rb#L18

So we need to clear that flag in our `_config.yml`.

And we might need a cron:  
https://seankilleen.com/2020/02/how-to-deploy-github-pages-on-a-schedule-to-publish-future-posts/


