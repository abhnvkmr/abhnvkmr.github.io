---
title: Fixing the Facebook and Twitter layout problems in Cocoon
layout: post
tags: [technology, facebook, twitter]
comments: true
share: true
categories: blogpost
---
All of my comrades who use Cocoon to evade campus firewalls are pretty content with the service except one thing: the ads. They usually block all the ads to get a web experience similar to the free open web. Let me be clear about ads&#8230;I&#8217;m not against them as they are part of the Cocoon&#8217;s business model and other free web services, but  their current implementation for the top-banner ads are too intrusive and have a major side-effect. They push the content far down so that the Facebook&#8217;s chat sidebar&#8217;s command palette is not visible at all. And if you&#8217;re blocking ads the top bar may be stuck floating in the middle  So here is a tiny CSS stylesheet to fix this. (I assume that you are using an advanced adblocker, preferably Firefox&#8217;s AdBlock Plus)

**Step 1:** First of all, you need to install <a title="Stylish" href="https://addons.mozilla.org/en-US/firefox/addon/stylish/" target="_blank">Stylish</a>. It&#8217;s an extension available for Firefox (and Pale Moon) which can modify a webpage&#8217;s look by altering its CSS (Cascading Style Sheet).

**Step 2:** Go to <a href="http://userstyles.org/styles/83583/cocoon-fixer-for-facebook-and-twitter" target="_blank">Cocoon Fixer for Facebook and Twitter &#8211; Userstyles.org</a> and click &#8220;Install with Stylish&#8221;. Don&#8217;t worry about the link, it&#8217;s just a tiny CSS snippet written by me.

**Step 3:** Now add these custom filters to your Ad-blocker.

<pre>###cocoon_ad_container
||ad-server.vworldc.com^
||api.vworldc.com/fp/*
||api.vworldc.com/video-ad.html?*</pre>

To add custom filters in AdBlock Plus, open its preferences either through status bar or Add-ons tab and go to &#8216;Custom filters&#8217; tab and add all these filters there in any of the groups.

Tada! You&#8217;re done. Cheers!!!

&nbsp;