
# 96boards Blog

1. [Adding a blog post](#adding-a-blog-post)

96boards blog posts are now written in markdown for a Jekyll based static site. These markdown posts are pulled in by Jekyll and displayed just like your typical 96boards blog post. The following tips will help you get on track and start writing blog posts for the new static site.

## Markdown
This Jekyll site is using Kramdown flavour markdown and also uses the rouge highlighter and a custom scss file in the \_assets/css folder.

## Images
Images are included using the image.html file. This is located in the \_includes folder. This file will generate the necessary markdown for an image that opens in a lightbox and is lazy loaded as users scroll down the blog post. Below is an example of how to include an image in your post.

```
{% include image.html name="name-of-your-specific-image.png" alt="This is the image alt tag which is also the lightbox caption." %}
```

The above is a basic example of a responsive lightbox image include for use in your blog posts when you include an image.

## Media
Media items are included using the media.html file will will generate a bootstrap responsive media element and include the supplied media_url as a source. This can be used for Slideshare includes and youtube video includes; both of which will be displayed as a repsonsive full width element which is lazy loaded using the Lazy Sizes plugin.
```
{% include media.html media_url="https://www.youtube.com/embed/bbMp3puXkVg" %}
```

## Code Highlighting
In order to highlight your source code in blog posts you should use the shorthand in markdown. Below is an example of this:

```
    ```python
        def newFunction(firstname, surname):
            name = firstname + surname
            return name
    ```
```
Once rendered the above will look similiar to this:
```python
    def newFunction(firstname, surname):
        name = firstname + surname
        return name
```
