---
title: How I created my blog using SvelteKit
author: Thibaut Wittevrongel
date: 2022-10-12
cover: /images/SvelteKitPicture.png
coverDescription: How I created my blog.
description: In this blog post, I explain how I created my blog using SvelteKit.
tags: development
---

<script>
    import Image from '$lib/components/Image.svelte';
    import Link from '$lib/components/Link.svelte';
</script>

<Image imgUrl="/images/SvelteKitPicture.png" altText="SvelteKit" size="large" />

## How I created my blog using SvelteKit

Hello and welcome to my first blog post. In this blog post, I will explain how I created my blog using SvelteKit and all the other technologies I used to create it.

<hr />

## 🤔 Why did I choose SvelteKit?

I chose SvelteKit because I wanted to try out a new framework and I wanted to learn something new. I also wanted to try out SvelteKit because I heard a lot of good things about it.

As a software engineering student, I am always looking for new technologies to try out and learn. Since we have an assignment to create a personal blog, I thought it would be the perfect opportunity to try out SvelteKit.

## 🚀 How did I start?

Firstly, I followed the <Link url="https://svelte.dev/tutorial/basics">Svelte tutorial</Link> on the <Link url="https://svelte.dev/">Svelte</Link> website to get a general understanding of how Svelte works. After that, I looked at the <Link url="https://kit.svelte.dev/">SvelteKit</Link> documentation to get a general understanding of how SvelteKit works.

Now, the important question was: "How do I start creating my blog?". So that's why I did the first thing every developer does when he/she starts on creating a new project. GOOGLING!

It didn't take very long until I actually found a very good tutorial on how to create a blog using SvelteKit. The tutorial I found was the following: <Link url="https://joshcollinsworth.com/blog/build-static-sveltekit-markdown-blog#approach-2-dynamic-routes">Let's learn SvelteKit by building a static Markdown blog from scratch</Link> by Josh Collinsworth.

The guide linked above explains everything you need to know to create a blog using SvelteKit. I followed this guide and created my blog using SvelteKit. The technologies that are used in this guide are the following:

- SvelteKit
- mdsvex
- Sass
- Markdown

After following the guide, the only thing that is left is just to style your blog and to add all the content you want to add.

## 📝 How do I add content to my blog?

Since this blog makes use of Markdown, it is very easy to add content to the blog. All I have to do is create a new Markdown file in the `src/routes/blog` folder and add the following code to it:

```markdown
---
title: How I created my blog using SvelteKit
author: Thibaut Wittevrongel
date: 2022-10-12
cover: /images/SvelteKitPicture.png
coverDescription: CollabDays 2022 In Brussels
description: In this blogpost I explain how i created my blog using SvelteKit.
tags: development
---

<script>
    import Image from '$lib/components/Image.svelte';
</script>

CONTENT I WANT TO ADD TO MY BLOG
```

## 🪚 Setting up the blog

Now that I have the code for my blog, I of course needed a place where I can host it. I chose to go for a Virtual Private Server (VPS) from <Link url="https://hosthatch.com">HostHatch</Link>. I decided to go for a VPS because I wanted to have full control over my blog and I wanted to learn how to set up a server.

Now that the server was obtained, I installed Debian 11 on it and NGINX as a web server. After that, I installed Node.js and PM2 to run my blog. PM2 is a process manager for Node.js that allows you to run your Node.js application in the background and to keep it running.

After that, I cloned my blog from GitHub and installed all the dependencies. Now that everything was installed, I could start my blog using PM2. I also configured NGINX to proxy all the requests to my blog.

## 📝 acquiring a domain name

Now that my blog was up and running, I wanted to have a domain name for it. It is not so nice to search for an IP address every time you want to visit my blog. So I went to <Link url="https://namecheap.com">Namecheap</Link> and bought the domain name <Link url="https://thibautwittevrongel.com">thibautwittevrongel.com</Link>.

After that, I configured the DNS records of my domain name to point to my server and I used Cloudfare as a DNS provider. Cloudflare is a DNS provider that offers a lot of features for free. I used Cloudflare to add an SSL certificate to my blog.

## 😄 Conclusion

I am very happy with the result of my blog, and I am very happy that I chose to use SvelteKit. SvelteKit is a very nice framework and I will definitely use it again in the future.

Setting up the server was also a very nice experience and I learned a lot from it.

Also, all the code is available in this <Link url="https://github.com/wittevrongelthibaut/personal-website">GitHub repository</Link>.



