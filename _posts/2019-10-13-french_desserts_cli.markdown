---
layout: post
title:      "French Desserts CLI"
date:       2019-10-13 22:59:39 -0400
permalink:  french_desserts_cli
---

The path to creating something great (or in this instance, just a working CLI) contains a lot of trial and error. While learning to code, you're often told that you'll hit bumps in the road. 

![](https://personalexcellence.co/files/infographic-emotional-journey-of-creating-anything-great.png) 

This image has been presented to me a few times already during my coding journey, and since the beginning, I feel like I've been doing okay so far. You go through lessons and you're given a bunch of tests. Then, you solve the errors. Easy enough, right? I didn't want to experience that moment of panic just yet, because building a CLI meant that you weren't relying on a series of tests to check if you were correct. It was up to me to build working code and "testing" it by running the code to see if a user could enter an input and receive a specific output. 

At first, everything was going smoothly. I started with finding a page to scrape. When trying to find a good page, the main thing I looked for was whether or not the website had HTML in the code. Next, I decided that websites with lists could make it easier to create a CLI as well. In addition, my favorite show currently is *The Great British Bake Off*, so I already knew that the kind of CLI I wanted to build should be centered arround desserts. Once I decided that, I found a website that listed French desserts. It was perfect! It:

* Contained HTML in the code
* Contained a list of items 
* Contained a description of each item

Next, was building the bare bones of the structure of my project. I entered `bundle gem french-desserts-cli` and that created the basic file structure of the program. The issues didn't start until I had to actually start writing out the code.

**Here are the issues I faced:**

* I didn't know how to check if I had scraped the data correctly to create a hash that would return a hash of desserts with the name and description of each dessert item.

* I didn't know how to create a new instance of a dessert to be saved into an array.

* I didn't have a control flow where I could easily operate between the files **dessert.rb**, **scraper.rb**, and **cli.rb**

**Here's how I solved it:**
* I figured out that the reason why I couldn't properly check to see  if my code would return the hash of scraped elements was because my `binding.pry` was still in the method `self.scrape_desserts` in  **dessert.rb**. I created a `self.test` method so that I could pop in a `binding.pry` inside that method and outside of the `self.scrape_desserts` method. I made sure that I placed `Desserts::Dessert.test` in the **cli.rb** file so that before the CLI actually ran, it would hit the binding.pry first. Once I ran `ruby bin/french-desserts`, I received this output:

```
[{:name=>"Chocolate-Filled Croissants (Pains au Chocolat)",
  :description=>
   "It's worth the effort to order the special chocolate batons, which make the difference between an excellent pain au chocolat and an ordinary one."},
 {:name=>"Lemon Curd Tart with Olive Oil",
  :description=>
   "Olive oil in the crust gives this Provençal tart a rich, crumbly texture, and the zing of the lemon filling really steals the show."},
 {:name=>"Daniel Boulud's Madeleines",
  :description=>
   "These delicate mini shell-shaped cakes are flavored with honey and orange zest."}]
```

Success! I did it.

* Next was trying to figure out how to create a new dessert object to be saved into an array. I needed to take the key-value pairs from the hash which contained a name and description of each dessert and save it into the @@all array. I was able to create it with this code:
```
def self.all 
    @@all = self.scrape_desserts.collect do |dessert| 
      self.new(dessert)
    end
  end
```

Pseudo-coding was key to figuring out the code for this one. I just needed to create an method that would return an array of all the dessert objects in the dessert class. And to do that, I would have to iterate through each dessert within my hash and create a new object.

* Lastly was my control flow. I had started with three files within `lib/desserts` : **dessert.rb**, **scraper.rb**, and **cli.rb** I had figured out that if I just put in my scraper methods and dessert attributes within my dessert class, it would be easier to look at all the dessert objects being created and saved into an array. Conciseness was key. So, I removed **scraper.rb** and kept the other two files. 


Finally-- working code! I was able to test out my code by implementing binding.pry inside a different method and before the CLI code starts running. I also was able to create a new object and saving it by using pseudo-code to get me there. Lastly, great control flow simply meant making it easier to look through the code and creating a concise structure. 

The journey to getting there meant that I had one day of no progress at all. I spent hours in front of a screen trying to test something and realizing that I had not even written any new code at all. Sometimes, just taking a break and starting again the next day helps. Even more so is being able to talk through the code with someone else. 






