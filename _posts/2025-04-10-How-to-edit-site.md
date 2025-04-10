---
layout: post
title: "How to edit the blog"
date: 2017-01-31
desc: "Describes how to edit the blog using docker containers"
keywords: "Jekyll,gh-pages,website,blog"
categories: [Misc]
tags: [Jekyll]
icon: icon-html
---

1. How to setup the docker container
- `docker pull jekyll/builder`

2. Have repo cloned and navigate to the folder

3. Run the container pointing to the
- `docker container run --rm -p 4000:4000 -v .:/srv/jekyll -it jekyll/builder bash`
- this will create the container mount the volume of the current directory to the container and open up a bash terminal to the container


4. Now we can run our site in the container and be able to navigate to the site using the mapped port
  - `Jekyll serve`
  - http://localhost:4000/MainSite