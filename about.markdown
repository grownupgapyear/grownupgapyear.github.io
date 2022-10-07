---
layout: page
title: About
permalink: /about/
---

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll

---
Blag updates:

2022-09-27 - a 40 image post without populated alt text was still a bit of a manual slog. New
workflow has alt text added to filenames and parsed out during markdown generation script. 

2022-09-26 - K is kind enough to offer proofreading/editorial help; new QC workflow established for
posts which should make things look more polished. This started with the post on
2022-09-11 and will be used moving forward ( as well as retroactively reviewing existing posts once
I get around to cleaning them up ).

Big productivity gains related to generating the markdown for images. Scripted up a simple infinite bash loop
to read in the alt text / resized image link / original size image link, which then spit the final
markdown version out to paste into the post. While it still required a fair amount of clicking
around, it was still leaps and bounds better than the original workflow. Using this for the 9/11
post and looking over the output, I realized I incorrectly assumed that the base URL for each link
was unique. This led to an even better loop which can piggy back on the resizer script, generating
the markdown for an entire post directory of images automagically. (The alt text still needs to be
manually populated, but I'm not too worried about that at the moment).

Also realized directory listing is enabled for my cloud cloud storage solution, which is not the
most desirable. Resolved by throwing up a blank index.html file in each folder. 

---

2022-09-20 - the markdown format for resized images which link to the original res versions has been
established; today I created a script to resize all images in a particular post directory. This
workflow allows me to stage files locally for a particular post, create resized versions of the
images, then upload them to my cloud storage solution where they can be linked from.
