---
title: Docs
layout: page
published: false
---

## docs

* <https://jekyllrb.com/docs/>
* <https://www.markdownguide.org/basic-syntax>

Gallery stuff
* <https://dmnfarrell.github.io/software/jekyll-galleries>
* <https://github.com/Kirlovon/Zoomtastic>
* <https://fengyuanchen.github.io/viewerjs/>

## start site locally
drafts for blogposts in _drafts, unpublished for this page, future for upcoming posts.

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
    for img in $(ls); do convert -resize 10% "$img" "$thumbsdir/$img"; done;

### single way
* insert into to post

<!-- -->
    {% raw %}{% include gallery.html fnstring="2022-05-30/IMG-20220529-WA0017.jpg,2022-05-30/PXL_20220528_085128752.MP.jpg" %}{% endraw %}

### folder way
* insert into post

<!-- -->
    {% raw %}{% include foldergallery.html folder="2022-06-07/2" %}{% endraw %}

## videos
todo: build an include

until now manully done for teamchallenge

### encode h265 from phone for web
    ffmpeg -i aerzte_westerland.mp4 -vcodec libx264 -vf scale=1280:720 -acodec copy -preset slow -crf 23 aerzte_westerland-out.mp4



https://stackoverflow.com/a/69316283
