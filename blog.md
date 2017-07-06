
# 96boards Blog

1. [Adding a blog post](#adding-a-blog-post)

96boards blog posts are now written in markdown for a Jekyll based static site. These markdown posts are pulled in by Jekyll and displayed just like your typical 96boards blog post. The following tips will help you get on track and start writing blog posts for the new static site.

## Markdown
This Jekyll site is using Kramdown flavour markdown and also uses the rouge highlighter and a custom scss file in the \_assets/css folder.

## Images
Images are included through Jekyll assets and the use of asset_path and the typical image include for markdown. Below are a couple of examples of image includes.

[![Image alt caption]({% asset_path "name-of-image.jpg" %}){:class="img-responsive"}](/assets/name-of-image.jpg)

The above example will create a hyperlinked image that links to the original image file and also displays the image as a bootstrap responsive image.

![Image alt caption]({% asset_path "name-of-image.jpg" %}){:class="img-responsive"}

The above is a basic example of a responsive image that is not linked.

## Media
Media items are include using the media.html file will will generate a bootstrap responsive media element and include the supplied media_url as a source.

_media.html_

<div class="embed-responsive embed-responsive-16by9">
  <iframe class="lazyload embed-responsive-item" src="{{include.media_url}}"></iframe>
</div>
