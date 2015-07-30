---
layout: post
title: "Git commits - change Author Name"
categories: bits
share: true
comments: true
tag: [http]
---

This is a simple command which changes author name of all commits for a specific email

{% highlight bash %}
git filter-branch --env-filter 'if [ "$GIT_AUTHOR_EMAIL" = "youremailaddress@gmail.com" ]; then
     GIT_AUTHOR_EMAIL=youremailaddress@gmail.com;
     GIT_AUTHOR_NAME="Your Name";
     GIT_COMMITTER_EMAIL=$GIT_AUTHOR_EMAIL;
     GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"; fi' -- --all
{% endhighlight %}
