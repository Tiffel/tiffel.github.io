bundle exec jekyll serve --drafts

export img=2022-05-30/PXL_20220528_144504881.jpg
convert  -resize 20% $img ../thumbs/$img
