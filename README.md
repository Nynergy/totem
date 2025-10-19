# totem

A script for building a one-file static website

-------------------------------------------------------------------------------

## What is it?

_totem_ is a bash script that reads files from a set of local directories and
uses them to construct a single HTML file that serves as your entire website.

## Why is it?

I stumbled across [this site](https://john-doe.neocities.org/) and thought,
"hey, I want to do that." But I'm a weirdo who programs for fun, so I'm gonna do
it _my_ way.

Which how I ended up with yet another over-engineered bash script to do
something that should probably be done by hand anyway.

## How is it?

Basically, I take advantage of the fact that when you have a
[fragment](https://developer.mozilla.org/en-US/docs/Web/URI/Reference/Fragment)
in your URL, the associated HTML element gains the `:target` CSS
pseudo-selector. With this, we can show and hide different elements based on
where the user has "navigated".

This allows us to stuff everything into one file, and gives the user the
impression that they are actually viewing a
[single-page application](https://en.wikipedia.org/wiki/Single-page_application)
that doesn't reload the page whenever you click on an internal link.

## Can I?

Yes.

```shell
$ git clone https://github.com/Nynergy/totem
$ cd totem
$ ./totem
```

You may need to add execute permissions to the script first: `$ chmod +x totem`

When you run it, it will tell you to create an environment file and add some
required variables to it. These will be some site-specific things like title,
description, url, etc. You can also use this file to override the default values
for a bunch of configuration options in the script. See all the global variable
initializations at the top of the script to see what the defaults are. This will
also tell you what folders _totem_ expects to find.

Feel free to comment out or modify anything that your site doesn't need, or add
stuff that you want. Then, start filling your folders with content.

## Cool

cool.
