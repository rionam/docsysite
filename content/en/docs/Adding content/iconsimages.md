---
title: "Logos and Images"
linkTitle: "Logos and Images"
date: 2017-01-05
weight: 6
description: >
  Add and customize logos, icons, and images in your project.
---

## Add your logo

Add your project logo as `assets/icons/logo.svg` in your project. This overrides the default Docsy logo in the theme.

## Add your favicons

The easiest way to do this is to create a set of favicons via http://cthedot.de/icongen (which lets you create a huge range of icon sizes and options from a single image) and/or https://favicon.io/, and put them in your site project's `static/favicons` directory. This will override the default favicons from the theme.

Note that https://favicon.io/  doesn't create as wide a range of sizes as Icongen but *does* let you quickly create favicons from text: if you want to create text favicons you can use this site to generate them, then use Icongen to create more sizes (if necessary) from your generated `.png` file.

If you have special favicon requirements, you can create your own `layouts/partials/favicons.html` with your links.

## Add images

### Landing pages

Docsy's [`blocks/cover` shortcode](/docs/adding-content/shortcodes/#blocks-cover) make it easy to add large cover images to your landing pages. The shortcode looks for an image with the word "background" in the name inside the landing page's [Page Bundle](https://gohugo.io/content-management/page-bundles/) - so, for example, if you've copied the example site, the landing page image in `content/en/_index.html` is `content/en/featured-background.jpg`.

You specify the preferred display height of a cover block container (and hence its image) using the block's `height` parameter.  For a full viewport height, use `full`: 

```html
{{</* blocks/cover title="Welcome to the Docsy Example Project!" image_anchor="top" height="full" color="orange" */>}}
...
{{</* /blocks/cover */>}}
```

For a shorter image, as in the example site's About page, use one of `min`, `med`, `max` or `auto` (the actual height of the image):

```html
{{</* blocks/cover title="About the Docsy Example" image_anchor="bottom" height="min" */>}}
...
{{</* /blocks/cover */>}}
```

### Other pages

To add inline images to other pages, use the [`imgproc` shortcode](/docs/adding-content/shortcodes/#imgproc).

## Images used on this site

Images used as background images in this and the example site are in the [public domain](https://commons.wikimedia.org/wiki/User:Bep/gallery#Wed_Aug_01_16:16:51_CEST_2018) and can be used freely.
