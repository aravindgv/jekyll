---
layout: docs
title: Assets
prev_section: datafiles
next_section: migrations
permalink: /docs/assets/
---

<div class="note unreleased">
  <h5>Sass and CoffeeScript support is currently unreleased.</h5>
  <p>
  In order to use this feature, <a href="/docs/installation/#pre-releases">
  install the latest development version of Jekyll</a>.
  </p>
</div>

Jekyll provides built-in support for Sass and CoffeeScript. In order to use
them, create a file with the proper extension name (one of `.sass`, `.scss`,
or `.coffee`) and start the file with two lines of triple dashes, like this:

{% highlight sass %}
---
---

// start content
.my-definition
  font-size: 1.2em
{% endhighlight %}

## Sass/SCSS

Jekyll allows you to customize your Sass conversion in certain ways.

If you are using Sass `@import` statements, you'll need to ensure that your
`sass_dir` is set to the base directory that contains your Sass files. You
can do that thusly:

{% highlight yaml %}
sass:
    sass_dir: _sass
{% endhighlight %}

The Sass converter will default to `_sass`.

You may also specify the output style with the `style` option in your
`_config.yml` file:

{% highlight yaml %}
sass:
    style: :compressed
{% endhighlight %}

These are passed to Sass, so any output style options Sass supports are valid
here, too.
