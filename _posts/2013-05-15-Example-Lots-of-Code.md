---
layout: post
title: Example With Lots of Code
tags:
- Example-Post
---

### Inline Code

Some code right in the middle `<img src="meme.gif">` of a sentence.

### Non-highlighted Code

	html {
	  font-family: $font-family-copy;
	  font-size: $font-size-mobile;
	  line-height: 1.5;
	  padding: 0;

	  @media (min-width: $break-point-mobile) {
	    font-size: $font-size-desktop;
	  }
	} 

### Highlighted Code

{% highlight HTML %}
<!-- Highlight that shit! -->
<header class="masthead">
  <a href="/">
    <img class="logo" src="/img/me.png" alt="Brandon Schmalz">
  </a>
  <ul class="nav">
    <li><a href="/career/">Career</a></li>
    <li><a href="/personal/">Personal</a></li>
    <li><a href="/posts/">Posts</a></li>
    <li><a href="/contact/">Contact</a></li>
  </ul>
</header>
{% endhighlight %}

### Add Some Line Numbers

{% highlight ruby linenos %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}

### Embed It

<script src="https://gist.github.com/Schmalzy/f2f998978808f75fa53f.js"></script>
