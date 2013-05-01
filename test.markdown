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

Tilde with postfix lang class
=============================

~~~
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
~~~
{.matlab}

Tilde with postfix lang spec
============================

~~~
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
~~~
{: .language-matlab}

Tilde with plain lang
=====================

~~~ ruby
def what?
42
end
~~~

Tilde with plain lang
=====================

~~~
def what?
42
end
~~~
{:lang="ruby"}


Tilde with postfix ruby spec
============================

~~~
def what?
  42
end
~~~
{: .language-ruby}

Indented code block with class
==============================

{.c}
    int main(void) {
      printf("Hello world!");
      return 0; 
    }

Indented code block lang spec
=============================

{: .language-c}
    int main(void) {
      printf("Hello world!");
      return 0; 
    }

prefix lang=c
=============================

{:lang="c"}
    int main(void) {
      printf("Hello world!");
      return 0; 
    }

postfix lang=c
=============================

    int main(void) {
      printf("Hello world!");
      return 0; 
    }
{:lang="c"}

postfix tilde lang=c
=============================

~~~
int main(void) {
  printf("Hello world!");
  return 0; 
}
  ~~~
{:lang="c"}

Indented code with postfix lang
===============================

    int main(void) {
      printf("Hello world!");
      return 0; 
    }
{: .language-c}

Liquid tag
==========

{% highlight matlab %}
% asd jasöd jaskadlfhds flahfalkjds hfalkds hasld hadlkfhdsflkjahfalkjfds halkds halkdsf
[a, b, c] = rot90('abc', 1, 2, [1, 2, 3])
{% endhighlight %}
