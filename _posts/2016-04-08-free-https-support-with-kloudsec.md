---
layout: post
title : "Free HTTPS support for Github Pages"
tagline : 
category : blog
tags : [free, devtools, SSL, Github, web, tools, InfoSec, Security, Cybersecurity]
---
{% include JB/setup %}

**UPDATE: Kloudsec shut down last August 1. <sup>[[Details here]](https://www.reddit.com/r/webdev/comments/4s3kmf/got_an_email_saying_that_kloudsec_will_be/)</sup> Too bad the service was good, way too good to survive. I'll be checking out [Let's Encrypt](https://letsencrypt.org/getting-started/) in the near future. If you have some tutorials on implementing this to a Github Page, feel free to share them on the comments section below.**

If you are using [Github Pages](https://pages.github.com/) for your site similar to what I have here at [gianfaye.com](/colophon), you may want to grab this neat tool by Kloudsec. As some of us may know, [Github does not currently support HTTPS on Github Pages with custom domains](https://gist.github.com/coolaj86/e07d42f5961c68fc1fc8). 
<hr>
<small>[Kloudsec](https://kloudsec.com/), in general, is an open Content Delivery Network (CDN) platform for programmers. They have servers at Singapore, US, and London, and are planning to expand to several locations. For the non-techies, visitors on your site will access the nearest server to them, serving your site faster as compared to just being served from one location. To know more about Kloudsec, [visit their docs here](https://docs.kloudsec.com/).</small>
<hr>
[Kloudsec for Github Pages](https://kloudsec.com/github-pages/new) provides HTTPS support for your Github custom domain page with a [LetsEncrypt](https://letsencrypt.org/) certificate over TLS 1.2, and a CDN for free. I received an email from Steven Goh, their CEO, about this tool. I'm not sure how they got my email address and knew that I have a custom domain for my Github Page but I think there are others who also got this email. I'm pretty sure they're spreading the news out to everyone, I'm also doing my part as they religiously replied to my emails for my questions.

The process was swift, and I got all the configuration set up in just a few minutes and the site live with HTTPS in a few days. 

## Pics or it didn't happen

![Kloudsec email](https://i.imgur.com/QLeV8rO.png)

![Kloudsec dashboard overview](https://i.imgur.com/9y0miic.png)

![Kloudsec dashboard reliability](https://i.imgur.com/4mEmwOm.png)

![My site's certificate](https://i.imgur.com/eg2hw6f.png)

## Take Note

1. You should remove your old A records.
2. You should wait for 48-72 hours for the propagation.
3. Well, if you're using Github, I would expect most of you already know 1 & 2. Just an FYI for those who don't.
4. You may [redirect all your http traffic to your new https domain](https://docs.kloudsec.com/v1/discuss/56e90d37dae96a0e00de0a5d). How awesome is that?
5. If you are using Disqus (or other commenting system) for your site, make sure to update the URL with the https - both on Disqus admin and your code.
6. If you turned the redirect on, make sure all your resources are also loaded via https to prevent the Mixed Content warning on Google Chrome, or its counterpart on other browsers. 
7. When your site is offline, they will serve a cached copy of your site to your visitors.
8. Enjoy your site being served over https.

<hr>
Here's my site report from Qualys SSL Labs:

![My site's Qualys SSL report](https://i.imgur.com/aYgppeW.png)

Yay, an A+! **Your turn.**

##### Check out:

* [Encrypt All the Things](https://encryptallthethings.net/) - a movement to encourage all online users: companies, organizations, individuals, to follow strict precautions and best practices for securing their data and transactions.
* [Marking HTTP As Non-Secure](https://www.chromium.org/Home/chromium-security/marking-http-as-non-secure) - a proposal by the Chrome Security to mark sites served over http as not secure

