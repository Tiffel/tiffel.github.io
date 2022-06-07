---
title: Docs
layout: page
published: false
---

## docs

* <https://jekyllrb.com/docs/>
* <https://www.markdownguide.org/basic-syntax>

## start site locally
drafts for blogposts in _drafts, unpublished for this page.

    bundle exec jekyll serve --drafts --unpublished

## image processing
Prequisite: `sudo apt-get install imagemagick`
* mark pictures on google photos as favorites
* selecting multiple folders from favorites, download as zip.
* create folder /img/$date according to post date and changedir into it
* move zip in there, run `unzip Photos.zip`
* create thumbnail dir

<!-- -->
    thumbsdir=$(pwd | sed 's/img/thumbs/')
    mkdir -p $thumbsdir

* convert images

<!-- -->
    for img in $(ls); do convert -resize 20% "$img" "$thumbsdir/$img"; done;

### current way
* insert into to post

<!-- -->
    {% raw %}{% include gallery.html fnstring="2022-05-30/IMG-20220529-WA0017.jpg,2022-05-30/PXL_20220528_085128752.MP.jpg" %}{% endraw %}

### better way
adapt include to use folder instead of a list of filenames
