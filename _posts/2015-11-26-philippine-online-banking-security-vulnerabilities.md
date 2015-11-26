---
layout: post
title : "Philippine Online Banking Vulnerabilities"
tagline : 
category : blog
tags : [InfoSec, Philippines, Security, Cybersecurity, Online Banking, featured]
---
{% include JB/setup %}

This post is a collation of articles and other references backing up a personal research of the current state of security of Philippine online banking portals. The purpose of this research is mainly educational and encouraging awareness of our online activities — one of which is online banking.

<hr>

<small>_Disclaimer: I am no expert in Information Security or Cybersecurity and I have minimal technical knowledge of the aforementioned fields as of this typing._</small>

<hr>

The main goal for this research is to answer this question: 

> Is your online banking secure enough?

**Cybersecurity**, or security in general, is a *cat-and-mouse* chase. Each day, software vulnerabilities and security holes are found, reported, and patched. But sometimes, [a mouse can outsmart the cat](https://en.wikipedia.org/wiki/Zero-day_(computing)). Attackers can find and exploit these vulnerabilities before they could be known and fixed by a patch. The victims will always be the users of the system.

There are techniques and technologies that help secure a system. The crucial part to keeping a system secure is to always use the latest release of these technologies as most likely the reason for the release would be a security patch to fix a known vulnerability.

What happens when the system you are using does not follow this practice? Well, it is like sending [an open invite to attackers](http://www.rappler.com/life-and-style/technology/42792-anonymous-hacks-ombudsman-government-websites).

For this research I will make examples of banks I can think of while writing this. I will use Google Chrome for checking the details of my connection to the following banks online and Qualys SSL Labs scanner for a deeper review. Technologies such as encryption, cryptography, online certificates will be the main basis.

##UnionBank

The main portal for personal banking is under this domain: _ebanking.unionbank.ph_

![UnionBank Connection Details](/assets/images/posts/2015/online-banking-unionbank.jpg)

**"This site uses a weak security configuration (SHA-1 signatures), so <span style='color:red'>your connection may not be private</span>."**

**"The certificate chain for this website contains at least one certificate that was signed <span style='color:red'>using a deprecated signature algorithm based on SHA-1</span>."**

SHA-1 has been vulnerable [since 2005](https://www.schneier.com/blog/archives/2005/02/sha1_broken.html)! More info [here](https://en.wikipedia.org/wiki/SHA-1#Attacks) and the full report on [this document](http://eprint.iacr.org/2005/010.pdf). Security experts recommend SHA-2 or SHA-3.

From [this article](https://sites.google.com/site/itstheshappening/): _"Microsoft, Google and Mozilla have all announced that their respective browsers will stop accepting SHA-1 based SSL certificates by 2017 (and that SHA-1-based certificates should not be issued after 2015). In conclusion, our estimates imply SHA-1 collisions to be now (Fall 2015) within the resources of criminal syndicates, two years earlier than previously expected and one year before SHA-1 will be marked as unsafe in modern Internet browsers. This motivates our recommendations for industry standard SHA-1 to be retracted as soon as possible."_

**"The connection uses <span style='color:red'>TLS 1.0</span>."**

TLS 1.0? Is there an acceptable reason why an online banking portal uses an older protocol? TLS 1.0 has been introduced in ...wait for it... 1999! The newer protocols are TLS 1.1 (released 2003) and TLS 1.2 (released 2008). And browsers started supporting TLS 1.2 since 2013. Why so behind? **Just why?**

**"Your connection to ebanking.unionbankph.com is <span style='color:red'>encrypted using an obsolete cipher suite</span>."**

I planned to save negative remarks to myself but **dear lord** -- UnionBank's server suports 512-bit export suites -- RSA. To put it bluntly, this is undoubtedly <span style='color:red'>A VERY UNSECURED SITE</span>. This obsolete cipher suite is obsolete for many reasons: one of them is that this is very susceptible to the **FREAK attack**. [It allows an attacker to intercept HTTPS connections between vulnerable clients and servers and force them to use weakened encryption, which the attacker can break to steal or manipulate sensitive data.](https://freakattack.com/) Meaning, if an attacker knows you do online banking at UnionBank they act as a middleman between you and the website, who can do whatever they want with your data. 


![UnionBank Security Scan Results](/assets/images/posts/2015/online-banking-unionbank-scan.jpg)

Scan result: <span style='color:red'>FAILED</span>. More info [here](https://www.ssllabs.com/ssltest/analyze.html?d=ebanking.unionbankph.com&s=203.82.36.182). 

(I thought I can do this in one seating. To be continued...)
