---
layout: post
title:  "Change local maven repository when building with gradle"
date:   2015-08-10 11:00:10
categories: gradle maven tips
---
It was quite hard to find that a simple system property can change what is the default local maven repository to push to.
Simply use the system property
{% highlight bash %}
-Dmaven.repo.local=path_to_the_local_m2_repository
{% endhighlight %}

It is useful when using this on CI servers without modifying the build.gradle and it works without any customizations.
