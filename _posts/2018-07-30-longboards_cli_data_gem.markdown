---
layout: post
title:      "Longboards CLI Data Gem "
date:       2018-07-30 06:41:57 +0000
permalink:  longboards_cli_data_gem
---


Nothing feels better than figuring out how to create something that you didn’t know how to do a few days earlier. It’s especially rewarding when you finally can grasp the concept of something that always seemed a bit fuzzy before. For instance, when I tried explaining to others what I had to do for my project, I stumbled through my words trying to explain what a CLI even is. *How could I create something that I didn’t even understand enough to explain to people?* Although a daunting task, this was a challenge that I accepted. Here’s how I figured out the mess of going from a blank screen, to writing fully executed code. 

I started with an idea—an idea that I was not quite sure could be feasible. So I messaged my instructor so we could figure out together if this was something I could do. The first idea was to scrape from a website, CreativeLive, and take data from the Top Trending Classes. I’d soon find out that there are just some websites that aren’t ideal to be scraped, and then I was back to square one. Through this process, I figured out two awesome and simple ways to figure out if a website can be scraped.

1. Drop into the IRB
    * `require ‘open-uri’` and `require ‘nokogiri’`. 
    * Set the `URL = “insert website URL here”`
    * Set the `doc = Nokogiri::HTML(open(“insert website URL here”)`
    * Enter `doc.css(“paste selector here”)`
    * This should give back some sort of an array or data. 
    * (My CreativeLive returned an empty array. Turns out Angular isn’t something you can scrape from.)
    * 
2. Download a Chrome extension named **Wappalyzer** 
    * This nifty gem (no pun intended) is a tool that can detect the framework for a website. Which means that when I saw that some websites used an Angular framework or React, I stayed away. 

I finally came up with an idea. I like longboards and long boarding, so I found a site that I could scrape (the framework was jQuery) with the idea that a person seeking information about a longboard could choose from a list of longboards and input a choice of which longboard they could see more information on, and then receive an output that would show the price and description of each longboard. 

When I found a website to use, things started to fall into place. Now I could start writing code!

*Now what should I call this gem? …Ah, Easy! Longboards*
Now was the time to create my gem.
`bundle gem longboards`

I looked through the folders and created an environment in my bin folder. In my library folder, I made sure to set up three different folders: *boards.rb*,* cli.rb*, and *scraper.rb*. 

**boards.rb** would contain all the information on the longboards and assign attributes to each video game that gets instantiated. Attributes included name, URL, price, and description.

**scraper.rb** would contain the scraper class that would scrape, or parse the HTML, from another website to extract and access data

**cli.rb** would require all of the classes built inside our gems directory. this is where the structure of the user interface would be.

I had no idea what my structure should be like. One instructor suggested to draft out what I want my program to do, but I was stuck. It’s like trying to figure out the structure of an essay before I actually write the words. The best thing I figured I could do was to just write code. All I knew is that I wanted to be able to have a menu, have a list of choices, have details displayed when a user chooses from the list, and have a solution for when a user enters an invalid input.

So I created theses instance methods:

`def main_menu`
`def list_boards`
`def display_details`
`def invalid`

Then I thought that the user should be greeted at the beginning, so I also defined a start method. And then I just kept coding. It was trial and error at this point, and once the code started working, I was able to tweak the program from here. 

By the end, I was no longer looking at a blank screen but instead, written code by me. I was amazed. The challenge of writing my own code proved to be rewarding in that, I was able to understand these concepts as I test out code by trial and error. And I'm not going to lie, this was frustrating, but it was pretty damn fun.

And guess what? I finally was able to explain what a CLI is.

*In the most basic terms, a CLI, or a command-line interface, is an interactive program that uses alternating lines of input and output, where a user enters instructions (or commands) by input, and in turn, will receive an output. 
*





