---
layout: post
title : "Windows 8 App Dev Boot Camp"
tagline : 
category : blog
tags : [featured,dev camp, coding, open source, software development, Microsoft, Windows 8, Azure, BizSpark]
---
{% include JB/setup %}

Last Thursday, we attended the **Windows 8 App Dev Boot Camp** at the Microsoft Philippines office. The event basically answered some questions floating around my head about Windows 8 application development. On the other hand, these answers brought up new questions.

The boot camp was attended by a few people, most of them are students, and some from the open-source community which mostly are from the Philippine Drupal group.

The speaker explained some of the basic steps on how to develop a simple Windows 8 app. From a web developer's view point, it is pretty easy to follow. And I could actually follow them if I have the copy of the tutorial he used. The first 30 minutes of the event basically shows how to use Windows 8, which I've already familiarized myself by watching Windows 8 demo in preparation to the dev boot camp and hackathon.

In the event, I have confirmed that we could use Node.js for our Windows 8 application. WinJS and how to access the native functions of a Windows 8 machine are some of the things I needed to know, since I'll be building a web based app. I've also learned about Windows Azure mobile services and how we could use this to add more complex features to our app.

I've also seen a Trello Windows 8 app and I installed it on my partner's machine. The UI is simple but the interesting part is what we did next...

We opened Trello on a web browser on a Mac, and we opened the Trello Windows 8 app on my partner's Windows 8 machine.

We then opened an existing board on both machines, created a card on the web app Trello, and a notification popped up on the Windows 8 Trello app and updated the interface adding the card exactly as I added it on the web app Trello.

This is when we realized that the Trello Windows 8 app is real-time. And this is the type of application we are planning to do. I've gathered some resources that we could use to make this happen.

######Here's a list of the related articles:
- [Real World Windows 8 Apps in JavaScript](http://www.slideshare.net/domenicdenicola/real-world-windows-8-apps-in-javascript)
- [Want To Build Win8/WinJS Apps? You Need To Understand Promises.](http://lostechies.com/derickbailey/2012/07/19/want-to-build-win8winjs-apps-you-need-to-understand-promises/)
- [Using Backbone.js in Windows 8 RT apps](https://blog.stackmob.com/2013/08/using-backbone-js-in-windows-8-rt-apps/)
- [Using AngularJS/BackboneJS in Windows 8 JavaScript app](http://blog.jonathanchannon.com/2013/01/24/using-angularjsbackbonejs-in-windows-8-javascript-app/)
- [Using backbone.js with Win8 Metro & WinJS](http://jrtipton.tumblr.com/post/28131822076/using-backbone-js-with-win8-metro-winjs)

I've also applied for [Microsoft BizSpark](http://bizspark.com/), got access to [Windows Azure](http://www.windowsazure.com/), and was invited to a new dev camp: **[Azure Camp](https://msevents.microsoft.com/CUI/EventDetail.aspx?EventID=1032567443&Culture=en-PH&community=0)** which will be held on October 25.

*"Learn to build, deploy and manage applications across a global network of Microsoft-managed datacenters using any operating system, language or tool."*

*"Azure Camps are free, fun, no-fluff events for developers, by developers. You learn from experts in a low-key, interactive way and then get hands-on time to apply what you've learned."*

*"In this foundation session we will demonstrate how to quickly build and deploy applications using Windows Azure features and services including Windows Azure Web Sites, Virtual Machines, Mobile Services, Cloud Services, and new developer tools and SDKs."*

Since the [Openness Night: 24-Hour Hackathon](/blog/openness-night-24-hour-hackathon) got postponed and was moved to October 26 due to bad weather last weekend, we'll have more time to prepare.

In regards to our project, I'll be sharing it as soon as I purchased the domain name so we don't encounter any reservation problems. :) I have created a Facebook page so if you are quite the stalker you might have already seen the project name. (I've unpublished it, though.) Otherwise, I'll be sharing the idea as soon as possible.

This week I'll be exploring MongoDB and deploying a sample web app to Heroku. Then, I'll be deploying a simple Windows 8 app on Windows Azure (maybe next week) in preparation to the Azure camp. If you'll be attending, please let me know. :)