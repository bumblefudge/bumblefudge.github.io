---
layout: archive
author_profile: true
title: "blogs"
category: blog
permalink: "/blog/"
description: "Personal writings varied and sundry."
og_image: "/assets/images/banner1.jpg"
---

&nbsp;
{% include figure image_path="/assets/images/banner1.jpg" alt="my puppy making puppy dog eyes" %}

As a lifelong writer across varies veins (academic, professional, literary, critical, political) I have always felt it important to do a little writing just for me.  When I was a literature professor, I advised any student that wanted to some day make a living writing to *always*, without fail, write (or carefully, lovingly translate) at least one thing every week for themself, lest the writing-muscle deep in them should atrophy from too much coursework, or term-paper-ing, or vacationing, livelihood-earning, or what have you.  As a professor, I ate that dogfood, but didn't keep receipts or records.

Now, in a different phase of my life altogether, I finally feel I am rooted enough to get back to taking my own advice.  I will be doing so here, over the coming weeks, and as time allows digging up old writings from [past](http://caballerojuan.tumblr.com) [lives](http://tortaface.com).


{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% capture label %}{{ collection.label }}{% endcapture %}
    {% if label != written_label %}
      <h2 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h2>
      {% capture written_label %}{{ label }}{% endcapture %}
    {% endif %}
  {% endunless %}
  {% for post in collection.docs %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
{% endfor %}
