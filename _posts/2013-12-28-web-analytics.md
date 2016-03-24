---
layout: post
title : "FUNdamentals of Web Analytics"
tagline : 
category : blog
tags : [featured,learning,work,analytics,Google,web]
---
{% include JB/setup %}

Getting to understand your visitors is one of the crucial elements in web development. Just creating and putting up a website isn't enough to help you identify the needs of your users. Without identifying the issues, you cannot put up a proper solution. 

Analytics has been with us for a very long time. And yet, most web development projects focus on the design and the structure of the website. While these are also essential part of web dev't, **web analytics** should also be in line with them in terms of importance.


## Background

My first encounter with web analytics was around 2010 when I was maintaining a blog. I used Google Analytics. I've learned that you can actually track the number of your unique visitors, number of pageviews, their location, even the device and browser they where using while accessing your site.

After learning about a bit of search engine optimization or commonly known as SEO (both on-site and off-site) to increase my pageviews, I've learned about _bounce rates_ - the more time the visitor spends on your page, the lower the 'bounce' rate you have. 'Bounce' literally meant when your visitors bounce off from your site. The lower the bounce rate, the more interesting content you have.


## Introduction to Digital Analytics

Recently, I was tasked to do **Event Tracking** and manage leads using **Goals** and **Funnels** on a project with Google Analytics. I had no idea how that does work nor have I been aware that you can actually track events on your website! Cool beans. After some research I discovered that Google offers digital analytics lessons on what they call [Analytics Academy](https://analyticsacademy.withgoogle.com/course). Cooler beans.

## Google Analytics UI

I was always confused with the UI before and didn't know which is for which. The GA UI is divided into two: the *Reports* section and the *Admin* section. Self-explanatory, the Reports section contains reports and the Admin lets you set things up on your account. 

Under the Admins section, you are then given three options, the *Account*, *Property* and *View*.

### Account 
Lets you manage the websites you have.

### Property 
If your website has different languages and you want to track them separately, you can set different properties for them. Or, if you have a mobile version of you site, you can also set them as another Property.

### View
Views are typically set up with your enviroments. The Default View tracks everything. You can set a Master View for your live site, and a Test View for your development site.

## Event Tracking

With [Event Tracking](https://developers.google.com/analytics/devguides/collection/gajs/eventTrackerGuide), you can track almost all user interactions on your page - from a button clicked, to your embedded video being played. 

	<a href="#" onClick="_gaq.push(['_trackEvent', 'Category', 'Action', 'Label']);">Play</a>

This can also be used to record case studies on a call-to-action object, like a specific button where the users click and submit their information and there goes your leads. This can also be used to test if the red button attracts more clicks than a green button - the most common but the best example of [A/B Testing](http://www.smashingmagazine.com/2010/06/24/the-ultimate-guide-to-a-b-testing/).

## Pageview Tracking

The first time I heard [Pageview Tracking](https://developers.google.com/analytics/devguides/collection/gajs/methods/gaJSApiBasicConfiguration?csw=1#_gat.GA_Tracker_._trackPageview) I was a bit confused on how it differs from
the number of pageview reports. This is then I discovered that this is used to track *virtual pageviews* on your page. For example, you are linking to a domain outside yours or you are linking a downloadable content. 

	_gaq.push(['_trackPageview', 'virtual-pagename']);

**Be mindful because it is case sensitive!** I've used `_trackPageView` (capital V) instead of `_trackPageview` and it didn't work.

*Why bother with pageview tracking when you can just do event tracking on the Download button!?* 

Good point. You can track them with event tracking but you cannot use them on your Goals which is the next topic.

## Goals and Funnels

Goals are your actual goals for your website. For example, you have an ebook and requires your visitor to submit their email address or subscribe to your newsletter before they can download the ebook. You can set up that as your Goal.

Funnels are a series of pages or virtual pages which leads to your Goal. 

Home -> Subscription page -> Confirmation link -> Ebook download page

To further your understanding, you can check out this article: 
[The Geek Guide To Understanding Funnels in Google Analytics](http://www.seotakeaways.com/the-geek-guide-to-understanding-funnels-in-google-analytics/)

## Classic GA vs Universal Analytics

Another note to take, there are two types of Google Analytics tracking methods out there. I wasn't aware of this first and it lead to nothing good so let me at least inform whoever is reading this post if you're still not aware of it. *Most* Google Analytics tutorials in existence used the syntax for the Classic Analytics, which is the old one. And the current tracking code on your GA Admin (if you migrated to the new GA) is the new one, Universal analytics. You might not want to interchange the two because they both differ in syntax and functions.

This is what the **Classic Analytics** tracking code looks like:

	var _gaq = _gaq || [];
    	_gaq.push(['_setAccount', 'UA-XXXXXXXX-X' ]);
        _gaq.push(['_trackPageview']);

        (function() {
            var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
            ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
        })();

This is what the **Universal Analytics** tracking code looks like:

	(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	})(window,document,'script','//www.google-analytics.com/analytics.js','ga');

	ga('create', 'UA-XXXXXXXX-X', 'gianfaye.com');
 	ga('send', 'pageview');

**Be careful not to use both tracking codes!**

That's it. I think I summed up everything I need to note for anyone introducing themselves with Google Analytics. If you have additional comments or suggestions you can just hit up the comment box below.