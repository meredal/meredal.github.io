---
layout: post
title: "Lesson 32 | CSS Standards	"
excerpt: "BEM | OOCSS | SMACSS | Atomic"
modified: 
tags: [standards, css, bem, github, pages, gitup, learning, front end]
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

## Types of CSS Standards

*In all of my building of small one-page sites, I have not been using any specific type of standards for my CSS. I know that standards are important though, I was not ignoring them on purpose. My goal was to be as much of a clean slate as possible when I entered into a position somewhere, and be able to use whatever type of standards were necessary (or not necessary) on my new projects.*

*Now, I am an operations and logistics girl at heart, so I looooooove standards, SOPs, KPIs, and the like. I used to write them, soooo DUH. But it was also nice to be able to write Sass & CSS the way I thought it made sense to me. Regardless, I wanted to take some time to dig into the different types of CSS Standards, what they are, and what I think about them. Here we go.* 

### BEM

BEM is one of the most common standards I have seen out there. I have also read that it pairs very well with React. And with a rising need for that, it sounded even better to learn about. After reading through a couple articles, this seems to be the methodology quite a few people are using and I am most excited to try.

Here are a couple of the pages I used for information:

- [BEM - Frontend Development Methodology](https://en.bem.info/)
- [Get BEM](http://getbem.com/)

Now BEM stands for Block, Element, Modifier. **Blocks** are meant to be new components, maybe a button or a div. And they are parents for other things on the site. And hopefully are reused over and over. A button is a pretty simple example as buttons often look very similar throughout a site. I really like this because it means only writing most of the CSS for your buttons once.. glorious. I also like that it is intended for you to be able to use this block of CSS on other projects or pages. Anything to keep me from writing the same thing over and over sounds like a great idea.

The second part is the **Element**. The element is a child of the block, and it depends on the block to have meaning. Perhaps a `<ul>`, `<li>`, or a `<p>` inside the button mentioned in the first section. There is a long list of things that could go here, but the important part is that it is directly related to the block and in a way, depends on the block to exist.

The last part is the **Modifier**. The modifier is a bit like the fun iterations you do to the block. Mostly, it is meant for theming, styling, or a specific behavior. This could be the change the colors, adjust the font sizing, or any number of things as long as it is not creating an entirely new block.

### OOCSS

**Object Oriented CSS** is another popular method for standardizing CSS across multiple pages and projects.

Here are a couple of the pages I used for information:

- [OOCSS Wiki](https://github.com/stubbornella/oocss/wiki)
- [OOCSS Wiki FAQ](https://github.com/stubbornella/oocss/wiki/faq)

Using this method means that you separate repeating visual patterns out into "objects" and then reuse them across the site. Umm. what? I had to read more to try and understand what that actually meant in practice. According to Stubbornella, there are two main principles of OOCSS:

- **Separate structure and skin**

For this, you should separate repeating styles out into something they call "skins". They used backgrounds and border styles as examples, which helped me to understand what they meant there. If multiple buttons have the same borders or if I have a repeating background throughout my site, it should be it's own "skin". That way I can use it as a class and continue to use it elsewhere on my site, or in new sites. And since HTML elements can have multiple classes, I can use as many as I need to use for an element without having to repeat the CSS over and over again. 

- **Separate container and content**

Again using Stubbornella's words: "rarely use location-dependent styles". Which I took to mean you should have some standard stylings that work across your site. They used the example of an `<h2>`. But I think you can apply it to all of your different text tags, setting the style for each across the site, so they look the same everywhere. Then, if you need a couple to change, you can class it differently and cut down on the amount of CSS you're writing. 

___

*Now, a couple more methods that I've heard once or twice..*

### SMACSS

Here are a couple of the pages I used for information:

- [Scalable and Modular Architecture for CSS](https://smacss.com/)
- [Video: Introduction to SMACSS](http://tv.adobe.com/watch/adc-presents-smacss/smacss-introduction-to-a-scalable-and-modular-architecture-for-css/)

SMACSS works with categorizing and using a specific naming convention so the same thing is used across multiple pages or projects. 

So there are categories. And then there are rules to go with each category. I'm borrowing the following section straight from the SMACSS website to explain the categories and their rules:

>1. **Base** rules are the defaults. They are almost exclusively single element selectors but it could include attribute selectors, pseudo-class selectors, child selectors or sibling selectors. Essentially, a base style says that wherever this element is on the page, it should look like this.
>
>2. **Layout** rules divide the page into sections. Layouts hold one or more modules together.
>
>3. **Modules** are the reusable, modular parts of our design. They are the callouts, the sidebar sections, the product lists and so on.
>
>4. **State** rules are ways to describe how our modules or layouts will look when in a particular state. Is it hidden or expanded? Is it active or inactive? They are about describing how a module or layout looks on screens that are smaller or bigger. They are also about describing how a module might look in different views like the home page or the inside page.
>
>5. Finally, **Theme** rules are similar to state rules in that they describe how modules or layouts might look. Most sites don’t require a layer of theming but it is good to be aware of it.

Now after each set of rules, there are naming conventions to go along with each. 

Wow. That is a lot of rules. And it seems like a lot of the way things can be named are still really up to the developer. Plus, the rules overlap a bit, which seems like it could be a bit confusing. I'm not opposed to using this one, but I like the simplicity of the first two a lot better. 

### Atomic CSS

Here are a couple of the pages I used for information:

- [Atomic CSS](http://acss.io/)
- [Pattern Lab](http://patternlab.io/)

Atomic CSS allows you to have smaller stylesheets and aims to cut down issues with specificity and repetitive code. To use it, you create very specific classes in your HTML code, and then are able to reuse that class throughout your site. Each class is used for one CSS property, which is how it is easily reusable.

This one sounds pretty interesting. Plus it has some very strict rules about syntax, which would make it easily transferrable between developers. That sounds intruiging, too. There isn't much to explain further as I think learning and applying it would really mean understanding and using the syntax as it's written on their site. Plus they have some tools that you can use to help you use Atomic CSS. Pretty Cool.

___

### My Thoughts

Since these are the two I see mentioned most often, they are the two I was most interested in learning about. And what was even more exciting to me is that I think I have used bits and pieces of both without even realizing I was doing it. I used OOCSS on some of my buildouts when I was styling my text for the entire page. When I had to override some of them later in the page I didn't use a class though, and now that I've read this it makes a lot more sense to be able to use a class and then have it available for re-use rather than writing the new CSS multiple times. I think I used BEM when I styled my buttons on a couple of my sites, too. One of the sites had the same buttons throughout the page, and one was slightly different. I used the style for the overall button throughout and then just changed the one button when needed.

Now, my use of both of these was guaranteed not perfect. I didn't even know I was using some type of standard. But it's cool to think I was moving in that direction without realizing it. And I'm excited to possibly use some type of standards in my future projects. I can really see the benefit to having multiple people using the same standards. It makes it easier to read someone else's code and be able to make adjustments to it. Or to go back and make changes to your own code. 

SMACSS does not interest me as much, it seems a little involved and much more interpretation is available. Which is great in a lot of circumstances, but it also is not entirely the point of applying standards in my opinion.

Atomic seems really interesting, too. I could see that taking a bit of time in the initial phases of using it. But it would be great on really large projects with multiple people working on them. 

Overall, learning a little bit about standards has been great. I've spent a few days learning about each and feel like I have at least a basic understanding of each. I can see the benefits of using, or not using standards and I'm excited to be able to adapt to new surroundings depending on the situtation I'm working with. 
