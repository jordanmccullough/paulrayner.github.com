---
layout: post
title: "Scheduling posts with Octopress"
date: 2012-11-22 19:40
published: false
comments: true
categories: Writing
sharing: true
footer: true
---

One thing I've discovered about my writing is that it is very sporadic. I will be inspired with an idea, write about it, go in a completely different direction. And end up with a long winding article that actually generates a bunch of blog posts. This is a consistent pattern for me. 

I want to be able to create draft posts. And then mark them as ready to publish. Once I do this then for the vast majority of them I want to have something that happens in the background that pushes all those blog posts onto a fire-and-forget queue, and then posts them on a consistent basis regardless of when the posts were written. I want to be able to override this from time to time, scheduling a post for a certain day, but that is the exception, not the rule.

Bascially, be able to write whenever the fancy strikes me, and then when they are ready, add them to a automated publishing pipeline. I want to be able to see the contents of the pipeline (which posts are scheduled and when), so I always can stay ahead of it, or tweak the order if I need to.

I have tried scheduling posts with Wordpress, but it forced me to make the decision on _when_ to publish, rather than taking care of that for me. I just want to be able to write, then have the tools get out of the way and handle the rest of the pipeline.

I remembered Ayende's post on RacoonBlog, and found the repo on Github, and then the relevant file: [PostSchedulingStrategy.cs][4].

<script src="http://gist-it.appspot.com/github/ayende/RaccoonBlog/raw/master/RaccoonBlog.Web/Services/PostSchedulingStrategy.cs"></script>

As Ayende says, the rules are simple:

* If there is no set date, schedule in at the end of the queue, but on a Monday - Friday 
* If there is a set date, move all the posts from that day one day forward
	* only to Monday - Friday
	* don't touch posts that are marked with SkipAutoReschedule = true
* If we are moving a current post, we need to:
	* trim all the holes in the schedule

And here we have the rules I want. Thanks Ayende!

Now, to see what others have done so far with Octopress...

A little research turned up a plea for [deferred posting with Octopress][0]. This led to finding a comprehensive posting on how to do [Synced and scheduled blogging with Octopress][1] which had some great ideas.

However, it was the [Automatically Publishing Drafts with Octopress][2] that proved to be most useful for me. I was able to incorporate the rules I wanted into the sample Rakefile and get it working the way I wanted. Here is my Rakefile:

 /// <summary>
 ///Rakefile here
 /// </summary>

If you like this, and especially if you want to productize it as a plugin so others can benefit, then feel free to fork my repo. 

[0]: http://tech.tulentsev.com/2012/10/deferred-posting-with-octopress/
[1]: http://instant-thinking.de/2012/08/03/synced-and-scheduled-blogging-with-octopress/
[2]: http://jarrettmeyer.com/blog/2012/05/24/automatically-publishing-drafts-with-octopress
[3]: http://ayende.com/blog/4837/and-now-raccoon-blog
[4]: https://github.com/ayende/RaccoonBlog/blob/master/RaccoonBlog.Web/Services/PostSchedulingStrategy.cs