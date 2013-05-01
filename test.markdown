---
layout: post
title:  test dat shizz
author: towolf
category: site
---

* auto-gen TOC
{:toc #toc}


Code blocks
-----------

Backticks
=========

```
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
```

Backticks with lang
===================

```matlab
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
```

Bare tilde
==========

~~~
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
~~~

Tilde with bare lang
====================

~~~ matlab
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
~~~

Tilde with postfix lang
=======================

~~~
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
~~~
{.matlab}

Indented code block with class
==============================

{.c}
    int main(void) {
      printf("Hello world!");
      return 0; 
    }

Liquid tag
==========

{% highlight matlab %}
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
{% endhighlight %}
