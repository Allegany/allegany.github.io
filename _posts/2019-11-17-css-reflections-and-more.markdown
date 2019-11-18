---
layout: post
title:  "CSS Preprocessor reflections and more"
categories: Reflections
excerpt_separator: <!--more-->
image: /assets/img/programming.jpg
---
### What do you think of pre-compiling your CSS?
I have used SASS and the scss syntax and I really like it. Even if vanilla css adding more and more features I think this syntax is really easy on the eye.
For example only the possibility to nest selector inside parent selectors makes it really easy to follow compared to regular CSS. And the possibily to use mixins
where you can easy reuse the same css setup on multiple selectors is also huge benefit over normal css. You can easier avoid repetitions and get less code in total.

I updated the minima themes sass files so much was already implemented. But I created new variables, a new mixin with variables for headings that of course could be solved with other solutions but 
was a fun try. I also used nesting of selectors and the lighten function that comes with sass.

The drawbacks of CSS preprocessors is that the generated css file is still the what is read by the browser and you lose control of it and it can become really big and hard to read. And when debugging
the line numbers will point to the generated css file and not the source file which means it will be harder to find. Another big drawback is there is no common pattern in the community if the generated files
should be saved to the source control or not and if someone else then comes and changing the normal css only to later get overwritten etc.

### What do you think of static site generators?
I think there can be really good advantages of using static site generators when the circumstances are the right ones. If you don't have a project that requires databases or
dynamic content where you dont need real time data and when you want a site that will be the same for everyone a SSG can be a really good alternative. I especially like the benefits
of creating for example a header, footer or menu in seperate file and then import this feutures where you want them. If you then have to change something you only need to change it one place
compared to normal HTML / CSS project where you need to change and update is all files where this feature excist. There are of course more benefits like good and free server support (atleast for Jekyll)
and better security and speed performance of the site.

### What is robots.txt and how have you configure it for your site?
Robots.txt is just a simple text file that should be located in root of your project. Web Robots that is used by for example search engines to index the web content
will then look after this file, where you can specify which pages or directories you want to block or allow to the web robot. There are many types of web robots
and you can give the block instructions for example only to specific ones if you want or to all of them.

I configured my robots.txt to block everything on my site for the robots, see below.
~~~~
User-agent: *
Disallow: /
~~~~

### What is humans.txt and how have you configure it for your site?
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
Standards: HTML5, CSS3, SASS, JavaScript  
Components: Jekyll              
Software: Visual Studio Code, Docker, Adobe Illustrator CC, Adobe Photoshop CC
~~~~

### How did you implements comments to blog posts
Since Jekylls standard theme Minima comes with some Disqus-configuration already made I decided to use Disqus. I created a new shortname at Disqus.com
and then added that shortname to the config.yml. I then changed the environment to production to show the Disqus comments on post sites.

### What is Open Graph and how do you make use of it?
The Open Graph Protocol was introduced by Facebook as a way for other websites to integrate with Facebook to become rich objects with the same functions 
as other objects. It is today used by all major social media platforms and is a way for the developer to decide what type of content that will show of up
if a page is linked to in social media. The developer can for example decide the title, an image a description and more.

Since Minima comes with a plugin called jekyll-seo-tag already predefined where you can either set this attributes in general in the config.yml or in the front matter
of each specific page or post I have defined at least the title, type, image and url in either the general config file or specific page file.
<!--more-->
