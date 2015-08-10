---
layout: post
title:  "Debug gradle build script in the IDE"
date:   2015-08-10 11:30:00
categories: gradle IDE tips
---
I did not find an easy way to debug gradle build script inside the IDE but the most convenient I found is to export GRADLE_OPTS before running the gradle build inside a terminal. Then use remote debug to connect the IDE to the JVM

Inside you terminal do
{% highlight bash %}
export GRADLE_OPTS="-Xdebug -Xrunjdwp:transport=dt_socket,server=y,suspend=y,address=5005"
{% endhighlight %}
Then run your build
{% highlight bash %}
gradle clean install
{% endhighlight %}
Finally put some breakpoints and launch the remote debug configuration inside your IDE on the port 5005 and you're good to go!
