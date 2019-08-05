---
layout: post
# portfolio tile config
title: NameChangr
description: A website that helps people change their legal names.
img: namechangr.png
open_source: true

# portfolio page post config
meta: NameChangr is a full stack web application I built from scratch that helps generate documents for legal name changes.
date: 2017-06-26
link: https://www.namechangr.com
repo_link: https://github.com/Darunada/namechangr
repo_icon: fa-github
tags: [portfolio, web, php, laravel, postgres, redis, heroku, s3]
---

<img class="col three" src="/img/portfolio/namechangr/screen-shot.png" alt="NameChangr Pick a Court Location Page" 
            title="NameChangr Pick a Court Location Page"/>

<div class="col three caption">
	The Court Location selection page.
</div>

[NameChangr](https://www.namechangr.com) is a social activism project I created in my spare time. It helps people who are trans 
or gender-non-conforming generate the paperwork required to legally change their name and gender in Utah. 
I run a google ad for the project and the system welcomes 70-80 users per month (as of July, 2019). In the same month, there were 6 
user registrations.

While not super impressive numbers in the grand scheme of things, it is a surprising amount considering the target market
is trans folks early in their transition who are interested in changing their legal names.
  
<div class="col one">
    Admittedly, I am not much of a designer, and creating beautiful front end UX from scratch is difficult for everyone.  
    Still, I wanted to challenge myself and create something uplifting as a surprise for the user.
</div>
<img class="col two right" src="/img/portfolio/namechangr/lovely-name.gif" alt="Your name is lovely." title="Your name is lovely."/>
<div class="col two right caption">
	When the user's name is entered, the system "checks" if the name is lovely.  <br/>Hint: all names are lovely.
</div> 
<div class="clearfix"></div>

<br/>
The site has an instructions page where I have written about the steps in the name change process, and if a user registers 
they gain access to the application generator which generates the packet.  To generate the documents, 
I took the court documents in docx format and added ${tokens} to it.  I am then able to replace the tokens with the 
user-entered values using the excellent [PHPWord](https://github.com/PHPOffice/PHPWord) library.  I built a framework 
around the process, and if someone implements another state it should be as easy as providing a template and inheriting some traits.

At the time I was evaluating [Heroku](https://heroku.com) for another project, and NameChangr needed a home.  Heroku appealed to me
because of the ephemeral nature of its containers and the free account has enough time to host NameChangr for free.  The idea 
that a site could be turned off and only turned on as needed is extremely interesting to me, and dynamic scaling is something
I had not had the pleasure of experimenting with at the time.  I enjoyed using it, and having a all the Heroku features available 
allowed me to configure other components like the database, emails, and NewRelic monitoring extremely quickly. 
If the time comes, scaling up should be incredibly easy, and I'm looking forward to it!

NameChangr is a an ongoing project, and I'd be delighted for other socially conscious individuals to participate
in expanding its reach into other states, or with help maintaining it.  I have made a bit of a framework that should make
it easy to add another state &mdash; I think the hardest part is data collection and formatting the document packet.

NameChangr is open source, so why not visit me on github: 
[https://github.com/Darunada/namechangr](https://github.com/Darunada/namechangr)

