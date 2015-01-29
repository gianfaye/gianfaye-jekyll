---
layout: post
title : "Gmail's Send Mail As Option Changes"
tagline : 
category : blog
tags : [featured,Google,Gmail,changes,updates,email,settings,branding,premium]
---
{% include JB/setup %}

This post is about the not-so-popular yet powerful feature of Gmail's **Send Mail As** option, and how it recently changed its mechanics of using it from *free to proprietary*.

Many of you probably aren't aware of this but [I've been using this feature for awhile](http://the.loading-info.net/2011/12/gmail-free-replacement-for-paid-email.html) until recently. When you have a domain name and your domain registrar offers free mail forwarding, you can use your Gmail to send as your preferred email address using your domain name.

For example, I have this `coolwebsite.com` domain and I want an email address associated with that. Let's say `contact@coolwebsite.com`

When you go to Gmail's **Settings** > **Accounts and Import**, scroll down to **Send Mail As** and click **Add another email address you own** you should be able to add another email address as long as it could successfully forward emails to your Gmail address.

![Send Mail As](http://i.imgur.com/TnJBK3Q.jpg)

However, Gmail recently changed its mechanics and are now asking users to input SMTP settings (which is a total bummer). Before this update, you can just add it the forwarding address and they'll send a confirmation link to verify that you own that forwarding address and that's it! But that's not the case now...

![Add another email address you own](http://i.imgur.com/BVqgYpd.jpg)

After a little research, I then discovered that they recently introduced [Google Apps for Business](http://www.google.com.ph/intx/en_ph/enterprise/apps/business/) - one feature is that you can create email addresses via Gmail using your domain name. But I've been doing this for a while now using their old **Send Mail As** settings. 

![Google Apps for Business](http://i.imgur.com/okTzIfo.jpg)

With the new settings, the user is now required to add SMTP settings to move on with the **Send Mail As** option, they have to get and pay for email hosting - which throws away the reason why we can use basic mail forwarding for Gmail. It followed [Yahoo!'s Small Business](https://smallbusiness.yahoo.com/email) (previously Yahoo! Mail Plus) paid plan to customize the email you'll be using to reply to a forwarded email - which is supposedly your custom email, not your Yahoo! email or Gmail. 

Related discussion: [MISSING OPTION: Use Gmail's servers to send your mail](https://productforums.google.com/forum/#!msg/gmail/B0Lqlwmm8Bc/pgLAySuVURgJ)

The most disappointing thing here is, I was in a middle of a project and already told the client that we could use Gmail for free when they are using their own domain name for their employee's email addresses. 

##Workaround

There's a workaround here but it doesn't work as good as before. You can still use Gmail's SMTP settings but with a few security drawbacks.

	SMTP Server: smtp.gmail.com
	Port: 465
	Username: yourgmail@gmail.com
	Password: yourgmailpassword
	Secured connection using SSL

On my initial attempt, I got an error and it links to this support page: [My client isn't accepting my username and password](https://support.google.com/mail/answer/78754)

So it says, first you must visit [http://www.google.com/accounts/DisplayUnlockCaptcha](http://www.google.com/accounts/DisplayUnlockCaptcha) and click on **Continue**.

Second, you must [allow less secure apps access](https://support.google.com/accounts/answer/6010255) your account and click **Enable**. Meaning, you are now more risk to security vulnerabilities because enabling this will (well as it says) allow less secure apps access your account.

~~Also, you cannot receive more than one email every 10 minutes or else it will block the sender.~~ (This no longer applies and you can receive emails within seconds. Thank you, Ben Harrison for letting us know.) And if you enable the 2-Step verification process you might have to disable it.

	Tip: If you don't want to sacrifice the security of your account you can create/ use another Gmail account you own for this purpose. Just use that Gmail address and its password on the SMTP settings and it should work fine.

Google gave mercy to the email addresses you already added prior to the update so this will only affect new email addresses you'll be sending mail as.

It's quite frustrating, yeah. But what can we do? Google isn't satisfied with putting ads on your Gmail inbox, they're now charging you for using their free(?) Gmail because you'll make the @gmail.com less popular by using your own domain name. 

We can all see where this is going.

**UPDATE:** Someone from Google Enterprise called me. Here's the backstory: So while testing the workaround I included on this post, I signed up for the 30-day trial for Google Apps For Business. Turns out, since we already have mail forwarding on the DNS, we cannot set MX records which Google is asking for the process to continue for their Google Apps for Business. So I told the representative, who seems to be calling to assist me, that I found a workaround and will not be continuing with their trial. :)
