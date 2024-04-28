---
title: 'GitHub Pages'
date: 2024-05-01
permalink: /posts/2024/05/github_pages/
---

I thought I'd retroactively document my process for getting this website set up.

I'm using [GitHub Pages](https://pages.github.com/).

You *can* start from scratch with a barebones site via a handful of terminal commands (after creating a new repository).

```
git clone https://github.com/username/username.github.io

cd username.github.io

echo "Hello." > index.html

git add .

git commit -m "initial commit"

git push -u origin main
```

But what I found most useful was the [Academic Pages](https://academicpages.github.io/) template, thanks to [Stuart Geiger](http://stuartgeiger.com/). I forked [academicpages.github.io](https://github.com/academicpages/academicpages.github.io) and modified the content to suit. This [diff](https://archive.is/3TPas) was helpful, showing the most important files to edit.

```
git clone https://github.com/username/username.github.io

cd username.github.io

[insert changes here]

git add .

git commit -m "some really amazing changes like wow"

git push -u origin main
```

I highly recommend [running locally](https://github.com/academicpages/academicpages.github.io?tab=readme-ov-file#running-locally) to preview changes before pushing them. Under the hood, Academic Pages is a [Jekyll](https://jekyllrb.com/) theme. I'm typically a Windows user and [Jekyll is not officially supported on Windows](https://jekyllrb.com/docs/installation/windows/), so I used a virtual machine with [Ubuntu 22.04](https://releases.ubuntu.com/jammy/). After installing Ruby, I was able to run a command to generate the website HTML and serve it via localhost. 

```
jekyll serve -l -H localhost
```

The only catch was that any changes to [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) required a server restart (but that took less than ten seconds). 

Once I was happy with my changes reflected in the local preview, I could commit and push, and release it to the world. The end result is this site, and new posts (like this one) are a markdown document and git push away from being live. Neat.

