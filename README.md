# CARNEGIE MELLON SOUNDBYTES WEBSITE STUFF

Hey tech-savvy Soundbyte!! (or anyone else who wandered onto this page)
My name is Daniel and I (like you) got wrapped into creating the Soundbytes website.

This page may seem like a lot, so I'm gonna try and walk you through this.

# STARTING COMMENTS
The main things that you'll *probably* have to work with are the following folders (barring any tragedies, but don't let that stop you!):

- _config.yml
- _posts
- img
- css (if you want something specific to posts)

Those should probably be the MAIN ones, but if you have questions or anything, feel free to email me or contact me or something. Someone in the group will probably know how to do this (hopefully).

# TERMINAL/SERVER STUFF

## Before Anything (with comments)

(run these in terminal)
```shell
bundle install
./scripts/install
```
  - Hopefully you have no issues here, but if you do, it's probably due to:
    - You don't have Ruby on Rails on your device (come on, what are you doing...)
      - Solution: Go through this - http://67272a.cmuis.net/labs/1 - and then thank the Information Systems Department
    - You don't have the bundler gem
      - Solution: Run this 
      ```shell
      gem install bundler
      ```
      and hopefully that works.
    - You may need to use sudo in front of bundle install because... reasons. Just try it if it is error-ing.

```shell
./scripts/generate-categories
./scripts/generate-tags
```
  - If either of those have errors, I'm sorry. I can't help you. Try running bundle install again? Google?
  
  
## Before Anything

```shell
bundle install
./scripts/install
./scripts/generate-categories
./scripts/generate-tags
```

## Running the Site Locally

```shell
./scripts/serve
```
NOTES:
- If you aren't seeing changes, go back and make sure that you saved everything. That'll be it 100% of the time when you forget to check. So just be smart and save your work.
- If you changed anything in the _config.yml file, you have to relaunch the server. So hit CTRL+C and restart that baby.
- Terminal is your friend. It will tell you if it can't find stuff.
- Google Chrome Inspector is also your friend when messing with CSS. Sean is smarter than me with that and will provide you with actual ideas. I will tell you to just Google things.

## Updating the Site

- Git stuff (you should really know how to use this, seeing as you probably downloaded it)
```shell
git add .
git commit -m "*USEFUL COMMIT MESSAGE PLEASE*"
git push
```
- And that's it. That's the beauty of using Github Pages. Whatever is in the directory will show on the website! Easy right?

- IMPORTANT NOTE: Using git push is terrible etiquette and you should go through the process of making pull requests but we're lazy. Please please PLEASE only push if you are 100% sure things work. Otherwise we'll have to roll the version back and you will be forever shamed.

# ACTUAL EDITS

## Member Editing

- All of this will happen in your _config.yml file. If you scroll down, you'll see a layout similar to this:
```shell
daniel: 
    name: 'Daniel Graf'
    section: 'Bass'
    pic: "/img/members/basses/daniel/daniel2-test.jpg"
```
If you follow this layout for anyone, everything should be fine. It's all organized by section, so try and keep it that way.
- The beautiful pics in the img/members section are also organized this way, so keep it that way.
- IMPORTANT NOTE: Please edit the pictures in Photoshop or something similar and make them smaller. Otherwise the site loads REALLY slowly and no one wants that at all. Don't even save them in this directory because those will upload to git, and make life miserable. Edited versions only please. Trust me. This goes for all pictures actually. BE WEB CONSCIOUS. NO ONE WANTS TO WAIT TO DOWNLOAD WHATEVER AWESOME PHOTOS WE HAVE. THEY WANT THEM AND THEY WANT THEM ASAP!!!!
- The criteria I made for each picture (using Photoshop) is as follows:
  - 1000w by 667h
  - Save as JPEG
  - When it brings up JPEG Options, set Quality to 7: (should make the size around 70K on the side. Adjust accordingly)
  
## Post Making

- This one is pretty straightforward.
  - You can use their script (look in scripts and learn) but I tend to just copy&paste an old one and edit things
  - IMPORTANT NOTE: The name of the file must be 'YYYY-MM-DD-post_name.md' because things break otherwise and it's sad.

## CSS Editing

- You can make sass files and it's great. All of these files (if you make new ones) must be started with:
```shell
---
---
```
otherwise it won't work. Trust me, I've tried debugging that for an hour or two.


# USEFUL LINKS

- Jekyll: https://jekyllrb.com/
- Jekyll Themes Used:
  - { Personal } Theme: https://github.com/PanosSakkos/personal-jekyll-theme
    - (Made mainly from the Grayscale Theme: https://github.com/jeromelachaud/grayscale-theme) and other stuff, look at the { Personal } documentation.
- Emoji Cheat Sheet (because we can support that :smile: ): http://www.webpagefx.com/tools/emoji-cheat-sheet/



# { Personal } Jekyll Theme
![Build Status](https://travis-ci.org/PanosSakkos/personal-jekyll-theme.svg?branch=master)
![license](https://img.shields.io/badge/license-MIT-blue.svg?link=https://github.com/dono-app/ios/blob/master/LICENSE)
[![Join the chat at https://gitter.im/PanosSakkos/personal-jekyll-theme](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/PanosSakkos/personal-jekyll-theme?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

{ Personal } is a free responsive Jekyll theme, about you :wink:

You can watch it in action [here](https://panossakkos.github.io/personal-jekyll-theme/)!

<img src="https://github.com/panossakkos/personal-jekyll-theme/raw/master/.github/personal-mobile.mov.gif" height="480">

<img src="https://github.com/panossakkos/personal-jekyll-theme/raw/master/.github/personal-desktop.mov.gif" height="600" width="960">

## What value does { Personal } add

* Fork of [Timeline](https://github.com/kirbyt/timeline-jekyll-theme) (mashup of [Grayscale by Start Bootstrap](https://github.com/IronSummitMedia/startbootstrap-grayscale) and [Agency Jekyll Theme](https://github.com/y7kim/agency-jekyll-theme))
  * Modern and minimal design
    * Responsive templates for home page, blog archive and posts. Looks great on mobile, tablet, and desktop devices
    * Sweet animations
    * Gracefully degrades in older browsers. Compatible with Internet Explorer 8+ and all modern browsers
  * Timeline
    * Tell your story so far with a sleek timeline of dates, pictures and descriptions
  * White on black text, making the reading experience tireless
  * Google analytics  
* Customization and full control of your website and blog through the site config
* Customization of the website's coloring
* Blogging functionality
  * Preview of the latest post in the home page
  * Archive page
  * Syntax highlighting
  * Emojis
  * Gesture navigation in archive and post pages by swiping
  * Hashtags
  * Categories
  * Disqus comments
  * Bootstrap share buttons
  * RSS feed
* Author blurb under the posts
* 404 page
* iOS and Android Web App mode
* Enforcing of https protocol
* Protection from email harvesting
* Sitemap
* Travis CI integration with [html-proofer](https://github.com/gjtorikian/html-proofer)

## Documentation

The theme contains documentation in the form of [blog posts](https://panossakkos.github.io/personal-jekyll-theme/blog/index.html).

## How to run locally

First, you need to install jekyll and the dependencies of { Personal } by running:

```shell
./scripts/install
```

Then, you can build and serve your website by simply running:

```shell
./scripts/serve-production
```

To serve across lan (requires su to forward the port 4000 over lan):

```shell
./scripts/serve-lan-production
```

## OSS used in { Personal }

One of the reasons { Personal } is real is the following OSS projects:

  1. [Grayscale](http://startbootstrap.com/template-overviews/grayscale/)
  2. [hammer.js](https://hammerjs.github.io/)
  3. [highlightjs](https://highlightjs.org/)
  4. [RRSSB](https://github.com/kni-labs/rrssb)
  5. [Timeline](https://github.com/kirbyt/timeline-jekyll-theme)
  6. [typed.js](https://github.com/mattboldt/typed.js/)

<div style="font-size:16px;margin:0 auto;width:300px">
    <a href="https://blockchain.info/address/1LHuKC9Em3KA5yoZaf7nngnNdf9K7s2gSi">
        <img src="https://blockchain.info/Resources/buttons/donate_64.png"/>
    </a>
</div>
