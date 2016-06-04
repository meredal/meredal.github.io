---
layout: post
title: "Lesson 27 | jQuerify a Buildout"
excerpt: "Adding jQuery"
modified: 
tags: [buildout, html, sass, css, git, github, pages, gitup, learning, front end]
comments: true

---

<section id="table-of-contents" class="toc">
  <header>
    <h3>Overview</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->

## Adding jQuery to "Selly"

### Thoughts

*So I learned a bunch of JavaScript and jQuery and now it was time to put it into practice. I took one of my previous projects, the "Selly" page, and added some jQuery to the page.*

*Here is what I did:*

- **scrollTo**
	- *Clicking on the down arrow icons in a sections will scroll down to the next section.*
	- *Clicking on a section in the sidebar will scroll to that section*
- **Waypoints**
	- *When the user scrolls down the page, the sidebar will have a fixed position on the side of the page. When they scroll back to the top of the page it will go back to it's original position.*
	- *As the user scrolls up and down through sections, or clicks on a section on the sidebar, the active section will be highlighted on the sidebar of the page.*
- *I also added a regular expression to validate the email that a user would input on the sign-up form on the page. If the user inputs an invalid email, they will get a notification. If they input a valid email, they will get a success notification on the page.*

*The finished product turned out pretty cool. Don't get me wrong though, it isn't perfect. And isn't exactly what I envisioned going into the project when I started. I wanted to do some more advanced things with animations with the email validation. And there are some issues with the waypoints that are not exactly perfect. But, the point of this project was for me to learn how to think in jQuery, and to practice what I've learned in the JavaScript language so far. And I think for that purpose, this was a good first step.*

### Related Links

- No link to the page yet as it is not hosted, but I will post it here.
- [scrollTo](https://github.com/flesler/jquery.scrollTo)
- [Waypoints](https://github.com/imakewebthings/waypoints)