---
layout: post
title:  "Enable hidden Developer options for Chromecast"
date:   2016-03-22 22:07:49
categories: Developer
banner_image: ""
featured: false
comments: true
---

So this evening I was having a problem with my Chromecast which was intermitantly causing audio to stutter. There didn't seem to be any logical reason for this happening and I was having problems narrowing down the cause. I decided to do a bit of Googling to see if I could find any useful information. That is why I discovered the Hidden Chromecast Developer Options which I didn't realise existed so I thought id share in case others didn't know either. 

<!--more-->

- Open Google Chrome
- Click the Chromecast icon
- Click Options
- Right click anywhere in the options tab
- Click Inspect element
- At the bottom of the screen, expand the body text
- Select the line that says showDevSettings
- On the right hand side, hover the mouse over the style that says:

`.ng-hide {
display: none !important;
}`

This will cause a tickbox to appear next to the display: none !important; code. Untick the tickbox.

> ❗ Please Note: the exact code may change from version to version and the detail of this will undoubtedly change with future versions. Look for any HTML or CSS code that hides web elements and remove or disable it to view the hidden options.

*Close the Inspect element interface with the little x on the top right hand side of the code window
The hidden developer options will now appear and you can change a selection of features ranging from:

- Tab casting mode
- Fullscreen zoom
- Automatically send Cast extension usage statistics to Google
- Minimum bitrate
- Maximum bitrate
- Maximum capture frame rate
- Enable Mirroring Link Protection
- Enable Cloud Features
- Pair with cloud device
- Delete cloud device
