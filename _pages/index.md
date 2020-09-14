---
layout: defaults/page
permalink: index.html
narrow: true
title: Hello!
---

## I'm Tejas Rane.

{% include components/intro.md %}

Follow this [link]({{ site.baseurl}}{% link _pages/about.md %}) to read more about me.

### Areas of Research Interest

- Modular Robotics
- Legged Robotics
- Robotic Manipulators
- Reinforcement Learning
- Bio-inspired Robotics
- Mechanism Designing
- Mechanical Manufacturing

Visit the [Projects & Articles]({{ site.baseurl }}{% link list/posts.html %}) tab to read more about the projects that I have contributed in, as well as some of the articles I have written thus far. 

Some of the projects that I am currently working on are listed below.

### Current Projects

<hr />
{% for post in site.posts limit:3 %}
{% include components/post-card.html %}
{% endfor %}

<hr />

### Contact me

Feel free to contact or DM me on the following platforms- 

<p class="d-flex align-items-center">
    <span class="icon grey mr-2" markdown="0">
        {% include entypo/mail.svg %}
    </span>
    <a href="mailto:f20170918@goa.bits-pilani.ac.in">f20170918@goa.bits-pilani.ac.in</a>
</p>

<p class="d-flex align-items-center">
    <span class="icon grey mr-2" markdown="0">
        {% include entypo/twitter.svg %}
    </span>
    <a href="https://www.twitter.com/desi_irodov">@desi_irodov</a>
</p>

<p class="d-flex align-items-center">
    <span class="icon grey mr-2" markdown="0">
        {% include entypo/linkedin.svg %}
    </span>
    <a href="https://www.linkedin.com/in/tejas-rane-359590149">Connect on LinkedIn</a>
</p>