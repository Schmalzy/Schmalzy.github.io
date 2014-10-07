---
layout: post
title: Column Ordering in Bootstrap
tags:
- Bootstrap
- Column-Ordering
---

When attempting to use the column ordering features in Bootstrap 3, I found that it was pretty confusing at first. Normally the [Bootstrap Documentation]( http://getbootstrap.com/css/) is stellar, but the section on [Column Ordering](http://getbootstrap.com/css/#grid-column-ordering) is really lacking some important details. 

> Easily change the order of our built-in grid columns with .col-md-push-* and .col-md-pull-* modifier classes.
>
>    {% highlight HTML %}
>    <div class="row">
>      <div class="col-md-9 col-md-push-3">.col-md-9 .col-md-push-3</div>
>      <div class="col-md-3 col-md-pull-9">.col-md-3 .col-md-pull-9</div>
>    </div>
>    {% endhighlight %}

And that's about it. So this article is my attempt at shedding some light on this feature, hopefully it helps you understand column ordering.

## Mobile First

Bootstrap is a mobile fisrt framework, which means that the order of the columns in your HTML markup should represnt the order in which you want them displayed on a mobile device.



- `col-vp-push-x` = push the column to the right by *x* number of columns, starting from where the column would normally render -> `position: relative`, on a *vp* or larger view-port.
- `col-vp-pull-x` = pull the column to the left by *x* number of columns, starting from where the column would normally render -> `position: relative`, on a *vp* or larger view-port.

vp = xs, sm, md, or lg

x = 1 thru 12
