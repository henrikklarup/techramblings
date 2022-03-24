---
setup: |
  import Layout from '../../layouts/BlogPost.astro'
title: Build-a-blog
publishDate: 24 Mar 2022
description: Why I created the blog, the techstack involved, and how it all came together
---

# Why?
I wanted to have a forum to share my thoughts, ideas, rants and ramblings. I'm a man of many opinions, and I like talking about them. This is a forum where I get to do that in a (potentially) broarder audience.

# Background story
I'm a developer at heart, but currently work as an engineering manager. This allow me to try out the role of managing other developers, and impact the company I work for on a higher level.

A lot of what I did as a developer involved helping my peers get better, moving the ball on bigger concepts, or trying to change the status quo. Since becoming an engineering manager, I've not slowed down on that front.

I think there are so many interesting topics out there, some of a technical nature, and some of a process nature, and I intend to write about some of them on this blog.

Whenever possible I will use real world examples, but I might leave out names, and other information to make sure I don't put anyone in the public spotlight who does not want to be there.

# Building a blog
The first thing I needed in order to share my ideas on a blog, was a blog.
I quickly decided that it should be low effort, to try out the format, and evaluate over time, before pouring all my energy into it.

I quickly decided on a name, and bought the domain [techramblings.dk](https://techramblings.dk/) from a vendor (I used simply.com, but you can use any vendor).


## Techstack
I've been following a project for some time called [Snowpack](https://www.snowpack.dev/) and while the project was cool, and I used it for some work related projects, it quickly turned out it was quite undermaintained.
The main reason is one of the most common ones for open source projects, the maintainers finds something better to do.

Snowpack was one of the first projects to provide a bundless developer experience, and it's honestly still a really cool project, but has not been updated for quite some time. If you are looking to try bundlesss development I would suggest heading towards [vite](https://vitejs.dev/) instead. Thats a topic for another blog post.

The reason for mentioning Snowpack, was because the project the maintainers moved onto was what I would be using for this blog, [astro](https://astro.build/).

Astro promises to deliver websites faster, and I really want my blog to be fast.
It's build for static sites, and my blog is mostly static.
I has a really cool idea of providing only the javascript required, and shipping the rest of the content as HTML. And I really like cool ideas.

So I settled on using astro to figure out what it can do, and how easy it is to work with.

### Create a blog template.
It was really easy to get started on using astro, as it comes with a lot of different templates one can use.

The only thing you need to do is to use the `create-astro` command, and it will guide you through it. Go [here](https://docs.astro.build/en/installation/) to see the details.


```bash
  # yarn
  yarn create astro
```

After the installation it's easy to adjust some of the files, and begin writing your first blog post.

## Hosting
Now that you have the technical stuff down, it's time to put it somewhere.

Again as I wanted to move quickly I wanted a reliable solution which was easy to use.
I decided on using [Cloudflare pages](https://pages.cloudflare.com/).
Not only do they officially support astro, they also handle all the complexities of deploying your application, putting SSL/TLS on top, and website analytics. And the best thing is, it's all free!

I'll not go into details about it, but follow their guide [here](https://developers.cloudflare.com/pages/framework-guides/astro/).
Note: you need to put you code into GitHub or GitLab, either one works, and it's easy to connect, and both are free. Your repository can either be public or private.

Once you've set everything up, which literally takes 5 minuts, then you will be presented with your deployed blog. mine was [techramblings.pages.dev](https://techramblings.pages.dev/).

## Custom domain.
If you use cloudflare as your DNS provider, it's easy to attach your new cloudflare pages blog. In the project you've just created you will see a tab named `custom domains` where you just setup your domain, easy!
If you are not already using cloudflare as your DNS provider, then you can follow the guide [here](https://developers.cloudflare.com/dns/manage-dns-records/how-to/create-dns-records/) to switch.

# Rounding up
That's it. You now have a fully working blog, which automatically deploys when you push to your production branch in git, it's protected, and hosted right at the edge, so no matter where you are located around the world the performance is going to be great. In addition most of the content is generated as HTML, so the size is super minimal, and load speeds are good.

Thanks for the reading the first blog post, one of many more to come.
