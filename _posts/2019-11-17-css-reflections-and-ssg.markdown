---
layout: post
title:  "CSS Preprocessor reflections and SSG"
type: article
categories: Reflections
excerpt_separator: <!--more-->
image: /assets/img/programming.jpg
description: "What my views on CSS preprocessors and Static Site Generators are".
---
#### What do you think of pre-compiling your CSS?
Of the CSS preprocessors I have used Sass and the sCSS syntax and I really like it. Even if vanilla CSS adding more and more features I think this syntax is really easy on the eye.
For example only the possibility to nest selector inside parent selectors makes it really easy to follow compared to regular CSS. And the possibily to use mixins
where you easy can reuse the same CSS setup on multiple selectors is also huge benefit over normal CSS. You can easier avoid repetitions and get less code in total.
<!--more-->

I updated the Sass files in the Minima theme so much was already implemented there. But I created new variables, a new mixin with variables for headings that of course could be solved with other solutions but 
was a fun try. I also used nesting of selectors and the "lighten" function that comes with Sass.

The drawbacks of CSS preprocessors is that the generated CSS file is still what is read by the browser and you lose control of it and it can become really big and hard to read. And when debugging
the line numbers will point to the generated CSS file and not the source file which means it will be harder to find. Another big drawback is there is no common pattern in the community if the generated files
should be saved to the source control or not and if someone else then comes and changing the normal CSS only to later get overwritten etc.

#### What do you think of static site generators?
I think there can be really good advantages of using static site generators when the circumstances are the right ones. If you don't have a project that requires databases or
dynamic content where you dont need real time data and when you want a site that will be the same for everyone a SSG can be a really good alternative. I especially like the benefits
of creating for example a header, footer or menu in seperate file and then import this features where you want them. If you then have to change something you only need to change it one place
compared to normal HTML / CSS project where you need to change and update is all files where this feature excist. There are of course more benefits like good and free server support (atleast for Jekyll)
and better security and speed performance of the site.

