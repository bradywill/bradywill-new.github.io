---
title: 'GitHub Pages'
date: 2024-04-28
permalink: /posts/2024/04/github_pages/
excerpt: 'My process for getting this site set up.'
---

To get myself in the habit of posting here, I thought I'd retroactively document my process for getting this website set up.

I'm using [GitHub Pages](https://pages.github.com/).

<!--
 GitHub pages is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository.
-->

You *can* start from scratch with a barebones site via a handful of terminal commands (after creating a new repository). This is how I created the [old version](/files/old.html) of this website.

```
git clone https://github.com/bradywill/bradywill.github.io

cd bradywill.github.io

echo "Hello." > index.html

git add .

git commit -m "initial commit"

git push -u origin main
```

But what I found most useful was the [Academic Pages](https://academicpages.github.io/) template. I forked [academicpages.github.io](https://github.com/academicpages/academicpages.github.io), renamed it and modified the content to suit me. This [diff](https://archive.is/3TPas) was helpful in showing the most important files to edit, at least to start with.

I highly recommend [running locally](https://github.com/academicpages/academicpages.github.io?tab=readme-ov-file#running-locally) to preview changes before pushing them. I'm mostly a Windows user, Academic Pages is a [Jekyll](https://jekyllrb.com/) theme and [Jekyll is not officially supported on Windows](https://jekyllrb.com/docs/installation/windows/); so I used a virtual machine with Ubuntu instead. After installing some bits and pieces, I could run this command from a terminal window to generate the website HTML and serve it via localhost.

```
jekyll serve -l -H localhost
```

Then I could open a browser window, and navigate to localhost:4000/ to preview the site. The only catch was that any changes to [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) required a server restart, but that took less than ten seconds.

Once I was happy with the changes reflected in the local preview, I could commit and push, and release it to the world. The [repo](https://github.com/bradywill/bradywill.github.io) includes an automatic deployment from the github-pages environment to get the site up and running.

The end result is this new version of the site, and new posts (like this one) are a Markdown doc and git push away from being live. Neat.

