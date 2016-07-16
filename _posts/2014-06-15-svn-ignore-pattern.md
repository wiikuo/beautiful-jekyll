---
layout: post
subtitle: ".Net 開發者適用的 svn 設定 - ignore pattern"
description: ".Net 開發者適用的 svn 設定 - ignore pattern"
tags: [how-to, svn]
---

.Net 的開發者在使用 SVN 的時候，可以加入以下的字串做為 ignore pattern

~~~
*.o *.lo *.la *.al .libs *.so *.so.[0-9]* *.a *.pyc *.pyo *.rej *~ #*# .#* .*.swp .DS_Store obj *.suo *.user debug release bin TestResults packages Bin
~~~

這樣子就能夠把不需要被版本控管的檔案自動的排除在送交清單上啦