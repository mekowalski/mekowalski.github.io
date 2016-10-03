---
layout: post
title:  "If you work hard and dig deep, eventually you will discover gems."
date:   2016-10-03 13:28:21 -0400
---


This gem I obtained, I worked incredibly long days for.  It is a very simple gem but is precious to me nonetheless.

I live in the San Juan Mountains in southwest Colorado.  If you are adventurous and willing enough, you are able to discover all there is the mountains have to offer.  Here in the town of Durango, you simply cannot be bored.  There are mountains to hike, run, bike up.  Rivers and lakes to swim in.  History to be learned of.  Live music to dance and sing along with. Shopping, eating and drinking to do.  With drinking Durango offers a great variety of distilleries and breweries to choose from.  Your thirst will not go unquenched.

There were many ideas going through my mind when I brainstormed what to create my gem for.  A devotee of fashion, I could have built a gem that users could engage with for building everyday outfits.  With my passion for design, I could have built a gem that users could engage with to gain ideas for home decor and furnishings.  My mind was all over the place and excited to begin building a gem.

Since there are so many breweries for the small mountain town I reside in, I decided on building a gem that users could engage with to learn about Durango breweries.  In order for users to interact with the gem, I needed to build a working CLI, (command line interface.)  And I needed to return real information to the users, therefore I scraped a live site to gain data.  A CLI and scraped data were the two main components I needed for a basic gem.

I built the base of my gem using `gem bundler`.  This helped me save on a headache that would have accrued if I decided to build my files, folders and informative articles one by one.  Using `gem bundler` made me feel confident in building my gem and I mainly had to go back, with given instructions to edit a few lines for my gem to work.

# CLI wants to play

This is where the fun begins.  I watched a [gem walkthrough video](http://youtu.be/_lDExWIhYKI) many times to fully understand how to begin building a gem.  I followed along for a few days to build a fake yet working command line interface. It was a process.  To build my CLI I wanted it to do a few things.

* I knew I wanted a list of breweries to show when the gem ran
* I also knew I wanted to go in depth and show details of each brewery
* I wanted to greet the user when they began to run the gem
* If the user was simply lost, I wanted to redirect them towards the list or exit out the gem
* I wanted the user to exit the gem on a simple, goodbye note

These simple requirements were how the gem would engage with the user.  I spent a few days building code that would just work.  Afterwards I refined what I wanted the CLI to do through interatction.  Though I had fake information that was available through the command line, I still had a working command line interface finally.  Now forward.

# Digging for real

Now that the CLI part was working I needed to present real information regarding the breweries.  I had much frustration and fun on scraping data from [Durango.org](http://www.durango.org/listings/category/microbreweries).  Frustration because scraping is very meticulous and time consuming.  Fun because once I had the data scraped I was able to play around in the console make my code work.  While begining the scraping method I had a few requirements.

* I wanted to grab all the microbreweries listed on the site
* I then wanted the basic details on the microbreweries
* This simply consisted of the brewery name, address, a description and telephone
* And I wanted this information to be returned for the user's interest.

Scraping was a long and detailed task.  I know I spent the majority of my days scraping.  Once I had my scraping information ready to go I had to build my scraping method that would also converse with my CLI.  This was included in the majority of days I spent with scraping.  *(I tell you, I thought I was a meticulous yet detailed person but with scraping you kind of just wish it were simpler and easier to do.)*

There was a lot of tricky business in making the CLI and the Scraper talk smoothly.  Here I learned a great amount of `require`, `require_relative` and `dependencies`.  I definitely gained a headache a few times.

While I played around, broke down and built up my code over and over, I began to realize that my gem was slowly working more effeciently.  I was overjoyed when I would run the command `./bin/micro-breweries` and see my gem play in the terminal.  Returning a greeting, a list of breweries and a set of options.  From those options, selecting more information on the breweries and seeing the real data being returned on the terminal made my eyes bright and wide.  This definitely is so basic but very cool to know!

Once I had a legitimate, working gem I was able to install my gem and run the command `micro_breweries` and see the greeting, the list and the options.  

# The final stretch

This was a huge learning curve for me.  I learned that I can build a gem.  I learned that my peers are beyond helpful.  I learned that I wanted to give up many times only to get back at it.  I tested my gem many times with the help of others playing with it and giving feedback.  There were moments that I reworked my code and it broke.  There were moments when it was smooth sailing.  Now, I'm excited to learn what else I can build.

After over two weeks I now have a simple yet beautiful gem.  As mentioned a couple times, it is very simple, nonetheless all gems are precious and valuable.


<iframe width="560" height="315" src="https://www.youtube.com/embed/yS1fbJIle-s" frameborder="0" allowfullscreen></iframe>
