---
layout: post
title: Column Ordering in Bootstrap
tags:
- Bootstrap
- Column-Ordering
---

When attempting to use the column ordering features in Bootstrap 3, I found that it was pretty confusing at first. Normally the [Bootstrap Documentation](http://getbootstrap.com/css/) is stellar, but the section on [Column Ordering](http://getbootstrap.com/css/#grid-column-ordering) is really lacking some important details. 

> Easily change the order of our built-in grid columns with `.col-md-push-*` and `.col-md-pull-*` modifier classes.

And that's about it. So this article is my attempt at shedding some light on this feature, hopefully it helps you understand column ordering.

## Misconception

My misconception with column ordering was that I should (or could) do the pushing and pulling on mobile devices, and that the desktop views should render in the natural order of the markup. Once I realized how wrong this was, I started to see things clearly.

## Reality

Bootstrap is a mobile first framework. This means that the order of the columns in your HTML markup should represent the order in which you want them displayed on mobile devices. This would also mean that the pushing and pulling is done on the larger desktop views.

Lets take a look at an example. Below we have two columns of equal width which will be pushed and pulled on `sm` or larger viewports.  

{% highlight HTML %}
<div class="row">
  <div class="col-sm-6 col-sm-push-6">
    <!-- Column A -->
  </div>
  <div class="col-sm-6 col-sm-pull-6">
    <!-- Column B -->
  </div>
</div>
{% endhighlight %}

- On the larger desktop views (`sm` or larger) the columns are pushed and pulled.
- On the mobile view (`xs`) the columns are rendered in the natural order of the markup.

![Column Ordering Example](/img/posts/column-ordering-example.png)

I think most people would (at first) assume that the desktop views would be rendered in normal order and that the pushing and pulling are done on the mobile views. Once you realize that the complete opposite is true, you begin to understand how to layout your columns in the correct order, and the correct classes that need to be used.

## Conclusion 

The two statements below summarize the functionality of the push and pull classes and should give you the full understanding of how they work, and how they should be used.

- `col-vp-push-x` = push the column to the right by `x` number of columns, starting from where the column would normally render (`position: relative`), on a `vp` or larger view-port.
- `col-vp-pull-x` = pull the column to the left by `x` number of columns, starting from where the column would normally render (`position: relative`), on a `vp` or larger view-port.
- `vp` = *xs, sm, md, or lg (minimum viewport)*
- `x` = *1 thru 12 (number of columns)*
