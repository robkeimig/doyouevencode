---
title: A Modern Workflow for Blogging
author: rob
date: 2013-02-09
template: article.jade
---

I figured I would start the first real post on doyouevencode.com with an overview of blog's workflow and some of the decisions I made along the way.

##The Typical Approach (DYEC?)

A typical hosted blog solution such as Wordpress utilizes server-side rendering of content for the end user. This means that you have a typical web server, database, operating system and server-side scripting language (commonly referred to as a WAMP/LAMP stack).

You get some nice advantages with this solution since you have a back-end database which can persist data between visits. This means you can have fun features like visit counters, comments on posts, etc. You are also able to log into your site from anywhere and create/edit pages, articles, themes, etc.

The downside is that PHP/MySQL can cause scaling issues when you have hundreds of thousands of visitors per day requesting your site.  Every time someone attempts to load your blog, an explosion of queries, log entries and PHP processes have to kick off in order to render the content. Some of this can be mitigated by using a caching service/plugin/appliance, but this ultimately adds to your overhead in cost and administration. Don't forget that you have to have a web server and database server (hosting fees).

##My Approach 

For this site I am using the Wintersmith static blog generator. This means that after I have completed changes to my blog, and run the proper build scripts, the entire site is available as static web content. When it is deployed in this form it can be hosted virtually anywhere. I use Amazon S3 for hosting my blog since they offer a static website mode for their buckets. I could even use a CDN (content delivery network) such as Amazon Cloudfront or Cloudflare to host the blog at edge locations for ultra-fast loading across the world.

These advantages sound really nice don't they?

The downsides should be obvious to most people reading this. No web server, database server or server-side rendering means that I am unable to utilize the advantages that are common to Wordpress. I can't have comments. I can't add articles or modify styles on the road. Lies.

By using the 3rd party service Disqus, I am able to have comments for each article I post. Their service is free and persists all of the data for me. They use their edge locations to rapidly service my users. They scale to service me. By loading their javascript asynchronously, I can maintain these ridiculously fast load times even if their service is slow or completely down.

The other major issue is how to modify the site on the go. Obviously I could carry my laptop with me and have the full development and build stack ready at all times. This is not an option. I will now describe the workflow used for modifying the site by utilizing cloud-based services exclusively.

##The Components and Workflow

In order to achieve the same effect of browser-only blogging, I needed to combine several technologies. My blog has the following components:

> **doyouevencode.com Blog Components:**
> - [Github]:https://github.com
> - [Wintersmith]:http://wintersmith.io
> - [Amazon S3]:http://aws.amazon.com/s3/
> - [Amazon Route 53]:http://aws.amazon.com/route53/
> - [Dillinger]:http://dillinger.io
> - [Travis-CI]:http://travis-ci.org
> - [Cloud9]:http://c9.io
> - Any domain registrar

[Workflow here]




