---
layout: post
title: "Scheduling posts with Octopress"
date: 2012-11-22 19:40
comments: true
categories: 
---

A request for [deferred posting with Octopress][0]. A comprehensive posting on how to do [Synced and scheduled blogging with Octopress][1].

One thing I've discovered about my writing is that it is very sporadic. I will be inspired with an idea, write about it, go in a completely different direction. And end up with a long winding article that actually generates a bunch of blog posts. This is a consistent pattern. 

I want to be able to create draft posts. And then mark them as ready to publish. Once I do this then for the vast majority of them I want to have something that happens in the background that pushes all those blog posts onto a fire-and-forget queue, and then posts them on a consistent basis regardless of when the posts were written. I want to be able to override this from time to time, scheduling a post for a certain day, but that is the exception, not the rule.

Bascially, be able to write whenever the fancy strikes me, and then when they are ready, add them to a automated publishing pipeline. I want to be able to see the contents of the pipeline (which posts are scheduled and when), so I always can stay ahead of it, or tweak the order if I need to.

I have tried scheduling posts with Wordpress, but I need to make the decision on when to publish, rather 


[0]: http://tech.tulentsev.com/2012/10/deferred-posting-with-octopress/
[1]: http://instant-thinking.de/2012/08/03/synced-and-scheduled-blogging-with-octopress/
[2]: http://jarrettmeyer.com/blog/2012/05/24/automatically-publishing-drafts-with-octopress
[3]: http://ayende.com/blog/4837/and-now-raccoon-blog
[4]: https://github.com/ayende/RaccoonBlog/blob/master/RaccoonBlog.Web/Services/PostSchedulingStrategy.cs