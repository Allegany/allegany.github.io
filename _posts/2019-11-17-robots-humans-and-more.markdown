---
layout: post
title:  "Robots, Humans and more"
type: article
categories: Reflections
excerpt_separator: <!--more-->
image: /assets/img/robots.jpg
---
#### What is robots.txt and how have you configure it for your site?
Robots.txt is just a simple text file that should be located in root of your project. Web Robots that is used by for example search engines to index the web content
will then look after this file, where you can specify which pages or directories you want to block or allow to the web robot. There are many types of web robots
and you can give the block instructions for example only to specific ones if you want or to all of them.
<!--more-->

I configured my robots.txt to allow all robots on my site (for now at least), see my file below.
~~~~
User-agent: *
Disallow:
~~~~

#### What is humans.txt and how have you configure it for your site?
Humans.txt is a text file that also should be located in the root of the project. This is a file were you can store and share information for other humans about for example
the people that created the site, technical information about the site and which softwares that helped created the site. You can also credit other sites or persons that in some way 
contributed to the site.

I configured my humans.txt to have information about me and which tools that I have used for this site. I also credited Unsplash were i got my photos from. See my configuration below.
~~~~
/* TEAM */
Web designer: Christoffer Granstedt
Mail: cg222sp@student.lnu.se
Github: Allegany
Location: Örebro, Sweden

/* THANKS */
Photos: Unsplash (www.unsplash.com)

/* SITE */            
Last update: 2019-11-17
Language: English   
Standards: HTML5, CSS3, Sass, JavaScript  
Components: Jekyll              
Software: Visual Studio Code, Docker, Adobe Illustrator CC, Adobe Photoshop CC
~~~~

#### How did you implements comments to blog posts
Since Jekylls standard theme Minima comes with some Disqus-configuration already made I decided to use Disqus. I created a new shortname at Disqus.com
and then added that shortname to the config.yml. The environment changed to production when it was published to GitHub Pages and then it was possible to add comments to each post.

#### What is Open Graph and how do you make use of it?
The Open Graph Protocol was introduced by Facebook as a way for other websites to integrate with Facebook to become rich objects with the same functions 
as other objects. It is today used by all major social media platforms and is a way for the developer to decide what type of content that will show of up
if a page is linked to in social media. The developer can for example decide the title, an image a description and more.

Since Minima comes with a plugin called jekyll-seo-tag already predefined I used this tool. I added the plugin in the gemfile and config.tml.
It helps automatically with some tags but you can also set the attributes in general in the config.yml or in the front matter of each specific page or post 
I have defined at least the title, type, image and url in either the general config file or specific page file.