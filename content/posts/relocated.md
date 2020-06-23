---
title: "Moving into a New Home"
date: 2020-06-20T19:42:11+10:00
draft: false
author: Tom
featuredImage: "/assets/images/sea.jpg"
lightgallery: true
---
I wasn't happy with the technical setup of my blog anymore, so I decided it was time for an overhaul. Instead of using Wordpress, I wanted to use a static site generator such as Jekyll or Hugo. Instead of using a traditional hoster, I decided to go cloud-native.

## From a traditional Web Hoster to Microsoft Azure

When I set up my blog years ago with a Germany-based hoster, the cloud was just in its infancy. At that time, it was pretty common to let the hoster manage the webserver, PHP, and for example, a MySQL database for you. Nowadays, especially from a software engineer's perspective, who is mainly working with the cloud, this seems quite old-fashioned. I wanted to set up and control the building blocks required to run a blog by myself and that ideally with something like Hashicorp's Terraform or the Azure command-line tool az with support for idempotent operations. This setup would require a domain registration, hosting a DNS zone, setting up an Azure web container, the Azure CDN, and organizing an SSL certificate.

## From Wordpress to Hugo and Github Actions

Over the years, running my blog with Wordpress bothered me for several reasons (and [more](https://www.sitepoint.com/wordpress-vs-jekyll-might-want-make-switch)):
- **Spam comments**; There were times were Wordpress emailed me several times a day that I had article comments to review. Usually, almost all of them were spam.   
- **Security updates**; Wordpress emails you that it needs updating. I do not want to be required to update software that serves static content.   
- **PHP is slow and overkill for hosting static content**; Employing a server-side scripting language for static pages does not seem to be the right choice for me.     

But besides all these points, I also wanted to change the editing and publishing workflow. While it was undoubtedly a novum to have a web editor you can write your articles in, Markdown has taken over the world of technical writing. I do not want to fight an online text editor. I want to write 'source code' which then gets rendered into some output format. After all, working with a markup language such as Latex saved in a plain text file has been around for longer than Microsoft Word. You can edit a markup file in basically any text editor, and have versioning with, for instance, git for free. Even further, with GitHub Actions, it is very well possible to set up a workflow where you: Edit a file, commit and push it to Github, run a static site generator in Docker, and deploy the output to Azure web hosting. GitHub lets you choose whether you make your blog 'source code' repository public or private. The latter reassembles what you get when using Wordpress, while the 'public' option gives your readers the possibility to view and work directly with your source content.

## Up and Running

One question remains, though, how can anyone comment on this blog? For that, I took inspiration from Mark Seemann, and his blog, who gratefully accepts comments as GitHub pull requests directly editing the source code of a page. So, here it is my new home on the web powered by Hugo, GitHub, and Azure. It feels much better to work with than my previous Wordpress installation, and I am excited to add more content soon.

Cheers!