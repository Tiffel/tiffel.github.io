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
* mark pictures on google photos as favorites
* selecting multiple folders from favorites, download as zip.
* create folder /img/$date according to post date
* move zip in there, run `unzip Photos.zip`
* run the following per image to create thumbnails

<!-- -->

    export img=2022-05-30/PXL_20220528_144504881.jpg
    convert  -resize 20% $img ../thumbs/$img

* insert stuff to post
