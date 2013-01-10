---
layout: post
title: Blogging On GitHub
tags:
- github
- jekyll
---

GitHub Pages is a great example of **it just works**. Internally it uses a parsing engine called [Jekyll](http://jekyllrb.com/), which creates static pages from your dynamic components.<br/>

Why Jekyll with GitHub Pages ?

- Minimalistic - It comes with no content, you create the components.

- Convention over configuration - It expects a certain [structure](https://github.com/mojombo/jekyll/wiki/Usage) for your website, reducing the configuration files.

- [Markdown](http://daringfireball.net/projects/markdown/) - don't need any fancy editors to write posts.

- Test your blog on [Windows locally](http://blog.ntotten.com/2012/03/02/github-pages-with-jekyll-local-development-on-windows/).

- No fuss deployment - Just use git to push out your changes.

- Setting up a custom domain is as easy as spelling [CNAME](https://help.github.com/articles/setting-up-a-custom-domain-with-pages).



To get started you need a GitHub account, if your account name is ***username*** just create a repository called ***username.github.com*** and push your content to the master branch.<br/>

Since the content is static (GitHub does not support Jekyll plugins) implementing tags and search can get tricky, luckly this too has been solved.

- [Charlie Park](http://charliepark.org/jekyll-with-plugins/) on tags.
- [Young Hahn](http://developmentseed.org/blog/2011/09/09/jekyll-github-pages/) on seaching.

