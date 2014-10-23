---
layout: post
title: "Create a Free Twitter Bot - hosted on Heroku"
published: true
tags: [Ruby, Twitter, Heroku]
---

I decided to make a [Twitter Bot](https://twitter.com/damnnaturescary) hosted on Heroku. And I managed to do it really easily. Surprisingly.
The source code for this is [on Github](https://github.com/wmmc/Damn-Nature).

Here are the basic steps I took:

### 1. Think of something funny / useful for your bot to do. 
- This is the hard part...

### 2. Register a new Twitter Account

### 3. Create a new Twitter 'app' - go to http://dev.twitter.com/apps
- This will have the ability to control your twitter account on your behalf.
- Make a note of the API keys.

### 4. Enable Read / Write Permissions for this App
- Found under 'Permissions'. If you need an extra mobile number, try [this trick](http://wmmc.github.io/2014/10/22/twitter-apps-authentication--without-another-mobile-number/).

### 5. Write some code which interacts with the Twitter API.
- Sferik's [twitter gem](https://github.com/sferik/twitter) makes this very easy in Ruby.
- If you're looking for inspiration, browse my [code](https://github.com/wmmc/Damn-Nature/blob/master/twitter.rb). It's not very complicated... And the twitter gem is very well documented.
- Remember to use [Environmental Variables](https://devcenter.heroku.com/articles/config-vars) to hide your API keys.

### 6. Create a Gemfile / Rakefile for Heroku to latch onto.
- Again, examples of these can be found on my [Github profile](https://github.com/wmmc/Damn-Nature/blob/master/Rakefile).
- The rakefile basically defines an isolated process that can be run by heroku.
- The Gemfile lists all the Gems you'll need to install.
- You may need to run `bundle install` (as usual...)

### 7. Create a new [Heroku App](http://heroku.com).

### 8. Push this to Heroku.

### 9. Add your Environmental Variables to Heroku.

You should be ready to take Twitter by storm now!
