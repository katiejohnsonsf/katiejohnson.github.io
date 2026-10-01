My blog, dedicated to Machine Learning tutorials, code, and insights.

Base Design
===========
My blog is built on top of [Poole][poole_repo]. I took inspiration and a lot of direction from Joshua Lande and his blog post [here][jl_poole].

Because my blog is my GitHub user page (and not just a project page), I worked from the master branch of Poole.

Page Links in Header
====================
Following instructions in [Joshua Lande's post][jl_poole], I modified the masthead of the 'default.html' layout and added his code for displaying links to the top level pages. Also, the list of top level pages is defined in _config.yml.

Google Analytics
================
Google Analytics is enabled by simply setting the variable `analytics_id` in `_config.yml`.

Time Zone
=========
Initially, I didn't have a timezone set for the site. This actually caused a problem at one point, because the site builder generated my post with a different date than what I put in the post, after converting the time. This was fixed by setting the `timezone: America/Los_Angeles` in `_config.yml`.

Math & Equations
================
Adding support for equations with MathJax was a cinch. I just put the following line in `_includes/head.html`

<code>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
</code>

{% highlight html %}
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
{% endhighlight %}

WordPress Migration
===================
Since I work in Python, I used the [exitwp](https://github.com/thomasf/exitwp) tool to convert all of my wordpress posts to Jekyll posts in markdown. Wordpress has an option for exporting your entire site as one big XML file, and exitwp is able to take this in and spit out all the images and posts. 

One thing I had to consider was "categories". I wanted to setup redirects from my Wordpress site to my Jekyll one, and the Wordpress redirect feature isn't customizeable. The issue this created is that Jekyll uses categories as part of the URL, but Wordpress does not. I opted to simply strip the categories from my posts to simplify things.

Another issue I faced was with the timezones. The funny thing about timezones is that if there are any inconsistencies, it's possible that your blog post will end up published on a different calendar date because of the time difference. I had just this issue, and it caused some of my redirect links to break. I just had to go through the posts and fix the timezones using some find/replace all magic.

Lastly, all of my images in my wordpress site were specifically set in the URL to be displayed at 470px wide. I just used some find/replace all to strip out all instances of this.

Google Adsense
==============
I put the Google Adsense code in `_includes/advertising.html` and then inserted in my `_layouts/posts.html` just above the comments.

It took a good day and a half or more before I saw any ads on my site. Until then, the Javascript Adsense Javascript was actually throwing an error! I could see the exception in the Chrome developer tools. Wish they handled that better--getting an exception on your code is unsettling! 


Licensing
=========
This repository is dual-licensed:

- **Code** (Jekyll templates, layouts, includes, and stylesheets) is licensed
  under the [MIT License](LICENSE), derived from the original
  [Poole](https://github.com/poole/poole) / Lanyon theme by Mark Otto.
- **Content** (research write-ups, project descriptions, and the original
  figures I created for them) is licensed under
  [CC BY 4.0](LICENSE-CONTENT).

My headshot and any photographs or third-party images are excluded from the
content license. See `LICENSE-CONTENT` for the full terms, including a note
on project write-ups that describe work performed as a U.S. federal employee.

AI assistance
=============
This site's code (Jekyll templates, layouts, includes, and stylesheets) was
developed with Claude (Anthropic) as a coding assistant. Project page content
also notes where Claude assisted with drafting/editing — see each page's
Stack & Methods section, or the About page's AI Use section for the full
disclosure.

[poole_repo]: https://github.com/poole/poole "Poole repository on GitHub"
[jl_poole]: http://joshualande.com/jekyll-github-pages-poole/ "Joshua Lande's blog post on Jekyll with Poole"
