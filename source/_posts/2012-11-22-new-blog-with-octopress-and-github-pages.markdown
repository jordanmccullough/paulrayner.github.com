---
layout: post
title: "New blog with Octopress and Github pages"
date: 2012-11-22 12:26
comments: true
categories: 
---

## Inertia and Impetus - Chasing Zero Friction

_Inertia:_ The resistance of any physical object to a change in its state of motion or rest, or the tendency of an object to resist any change in its motion. [Wikipedia - "Inertia"][11] 

Inertia relates to an object's amount of resistance to change in velocity, whether it is moving or not. Either for an object getting started, or changing velocity when it is already moving:

The Wikipedia entry notes that "On the surface of the Earth inertia is often masked by the effects of friction and air resistance, both of which tend to decrease the speed of moving objects (commonly to the point of rest), and gravity."

So, inertia for moving objects is about their tendency to remain at the same velocity, but it's also about the tendency of resting objects not to move. According to the [Free Dictionary][12], inertia is "the tendency of a body at rest to remain at rest." This reluctance to move is how I typically think about inertia: resistance to movement. For me it's the inability to get started on something. Something that I know is important, but I'm feeling the drag created by friction.

The Wikipedia entry also points out that:

>Inertia comes from the Latin word, __iners__, meaning idle, or lazy.

which is perhaps why I attribute my reluctance to do things as laziness.

## _Goal: Zero Friction_

Frictionless tools. An inertia-free process. I have left my blog lie fallow for over a year because of the friction of writing and publishing to it. Every time I came up with an idea to write about, I thought about the hassle of getting it online using my tools of choice, and instead of making it happen I did nothing. Thinking about the benefits of sharing did not help. Telling myself that I needed to be writing didn't help. Trying different HTML editors didn't help. Reading posts [about why I should be blogging didn't help.][22] [Well, maybe a little][23].

Friction in our tooling is the death of a thousand cuts.

It doesn't have to be blogging. Friction is found in many places. A commitment to eliminating friction wherever we find it should be paramount. At the heart of Lean is the idea of getting ideas from concept to cash as soon as possible, and friction is what gets in the way of that ideal. 

TDD assists us with reducing friction in creating maintainable, loosely-coupled code. CI is about reducing friction around technical teamwork. Continuous deployment is about eliminating friction from the deployment pipeline.

As Ayende said in his post [Reducing friction as a standard operating method][10]:

>One of the things that I am really sensitive for is friction. And anytime that I run into that, I am doing an evaluation about how much it is going to cost to remove that.

>The problem is ignoring the opportunities lost angle. One of the things that most people do not usually consider is that we tend to avoid things that are painful.

and [here][20]:

>Zero Friction approach is very important for the overall success of a project, because it means that the right thing is the easy thing, so that is what will get done.

And again in [Zero Friction & Maintainability][21] :

>Creating a zero friction environment will produce a system where there is no incentive to corrupt the design, the easiest thing to do is the right thing to do.

>By reducing the friction in the environment, you increase the system maintainability

What kind of friction? I can't work without source control now. 


Contrast inertia with impetus, which is [defined as][21]:

>An impelling force; an impulse.

It's also defined as a driving force, or the force or energy associated with a moving body. Friction is what makes inertia so hard to overcome, but once it is overcome that movement is what can give impetus to other things to move.

![Notebooks of Leonardo Da Vinci](notebooks-of-leonardo-da-vinci.jpg)

From Leonardo Da Vinci: 

![Leonardo Da Vinci](http://upload.wikimedia.org/wikipedia/commons/f/f9/Leonardo_da_Vinci_-_Self-Portrait_-_WGA12798.jpg)

I've been reading the [Notebooks of Leonardo Da Vinci][13] this week, and it was reading Da Vinci's notes on impetus that got me thinking about how reducing friction to overcome inertia is so key. Da Vinci defines Impetus as:

>...a power created by movement and transmitted from the mover to the movable thing; and this movable thing has as much movement as the impetus has life. - p. 73



### Why Octopress?

Here are [4 good reasons][0] from AlBlue's blog: 

* Jekyll-based
* Markdown content - I hate writing raw HTML, and have loved the switch to Markdown, using Byword as my primary editor.
* Stylish
* Plugins

Have been using BlogEngine.NET. Liked it, but found the authoring experience tedious, and wanted to move to tools I am now either more comfortable with or interested in learning: Ruby, Jekyll, Markdown, Sublime Text 2, Byword, Marked, Git. As Joel Hooks says on his ["Fresh Start"][1] blog post:

>It falls well into the [breakable toy][5] category of things, and that is something I can use right now as I learn new tools. I’m looking forward to improving this space with quality content about modern standards-based web development with open source tools.

Some [possible disadvantages of Octopress][2], also from AlBlue's blog. Part of what he mentions is the lack of separation between content and plumbing, in that there’s really five sets of things to manage:

1. The source posts (in Markdown format)
1. The layout and supporting scaffolding (in HTML/Liquid templates)
1. The plugins for Jekyll to know how to process the Liquid templates)
1. The Octopress supporting management code
1. The published HTML

His point is that the first two items (the source posts, layout and templates) should be in source control, but the:

>plugins and octopress management code really need to live in a different Git repository, though, so that they can be upgraded independently.

This makes a lot of sense, but I don't feel bothered by this at the moment, and fully expect the gap here to be addressed sometime in the near future.

http://mattgemmell.com/2011/09/12/blogging-with-octopress/

I had trouble getting ruby-1.9.3p??? with rbenv, so I tried rvm (again, after giving up on it earlier this year) and surprise, surprise, it worked!

Thanks to the following blog posts for help with getting this set up:

http://www.tomordonez.com/blog/2012/06/04/creating-a-github-blog-using-octopress/

![Twitter Conversation with @matthewmccull](github-pages-user-versus-project-pages.png)


In the process of researching Octopress, I stumbled across some other helpful resources, so if you are [switching Wordpress to Octopress][3] then be warmed and filled.

This same blog post about  talks about:

>Another cool tool that works well with Octopress is Pow. Octopress is a rack app, and once to point Pow at your Octopress folder, it serves the page up locally at http://foldername.dev. Then it’s just a matter of running rake watch and going to town.

### Cool Octopress Resources

http://stackoverflow.com/questions/12328828/directory-structure-of-octopress

Github pages aren't the only game in town, as @aeroplane soft pointed out:

![Hosting Octopress on Amazon S3](hosting-octopress-s3.png)

If you're using rbenv, as I was, then start with http://kvz.io/blog/2012/09/25/blog-with-octopress/

This started out as a post about installing Octopress, and became something more.

As Scott Hanselman said in [Your Blog is the Engine of Community][23]:

>**I would encourage you _all_ to blog more. Tweet less.** Blogs are owned by you. They are easily found, easily linked to, and great conversations happen with great blog posts. The river of social media rushes on and those conversations are long forgotten. A great blog post is forever. Today's real-time social media is quickly forgotten.

>Don't be a meme, but a movement.



[0]: http://alblue.bandlem.com/2012/02/advantages-of-octopress.html
[1]: http://joelhooks.com/blog/2012/07/25/fresh-start-migrating-wordpress-octopress/
[2]: http://alblue.bandlem.com/2012/02/disadvantages-of-octopress.html
[3]: http://adampreble.net/blog/2012/09/another-octopress-blog/
[5]: http://redsquirrel.com/dave/work/a2j/patterns/BreakableToys.html
[10]: http://ayende.com/blog/4298/reducing-friction-as-a-standard-operating-method
[11]: http://en.wikipedia.org/wiki/Inertia
[12]: http://www.thefreedictionary.com/inertia
[13]: http://www.amazon.com/Notebooks-Leonardo-Vinci-Worlds-Classics/dp/0192815385
[20]: http://ayende.com/blog/3131/setting-up-zero-friction-projects-data-access
[21]: http://www.thefreedictionary.com/impetus
[22]: http://www.hanselman.com/blog/YourWordsAreWasted.aspx
[23]: http://www.hanselman.com/blog/YourBlogIsTheEngineOfCommunity.aspx