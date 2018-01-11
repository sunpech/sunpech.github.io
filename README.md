# sunpech.github.io

This is my website/blog that is run using [Jekyll](http://jekyllrb.com/) and is hosted on [Github Pages](https://pages.github.com/). The posts were converted from [Blogger](http://www.blogger.com). See: [Blogger migration](http://jekyllrb.com/docs/migrations/).

The website is at: [sunpech.com](http://sunpech.com)

The theme is based off of [Clean Blog Jekyll](https://github.com/IronSummitMedia/startbootstrap-clean-blog-jekyll).

## Creating a Post

Here are some helpful tips in creating a post, particularly in [front matter](http://jekyllrb.com/docs/frontmatter/) variables such as thumbnail, image, and description. Also see draft example.

* Name post files with YEAR-MM-DD-TITLE.md format.
* Use Markdown in new posts, but HTML is acceptable (not encouraged).

### Variables
* `thumbnail` - width should be 300px.
* `image` - width should be 600px or wider. Recommended: 1080px. Dimension of 1080x720.
* `description` - should be filled out for better Twitter Cards and Facebook Graph posts (optional).
* `header-img` - can be set for custom header image. Should be 1900px wide. Also dim the photo, maybe 1-3 exposure stops.

### Embedding a YouTube video

You can embed an iframe into a post, but to get it so it's responsive, use the following div and class around the iframe:

```
<div class="video-container">
<iframe... </iframe>
</div>
```

### Drafts

Drafts for future posts can be found in folder: `_drafts`. When testing locally, just run the following to see what it looks like:

```bash
jekyll s --drafts --watch
```

### Posts

Posts that are used to generate the site are found in folder: `_posts`. After a draft is made, just move it to this folder and git push to origin.

### Tags

For any new tag that doesn't already exist, create a folder of that name in the folder tag. Then copy `index.md` from another tag folder into the created folder.

## Creating a Page

There is a folder called `best`, which contains pages regarding recommendations of best products etc. Other pages can be created at the root folder.

### Variables

* `navigation` - set to true or false, as to should be shown as navigation link.
* `permalink` - path to page
* `best` - set to true or false, to be used as part of index of best pages. Optional, only required if to be displayed.
* `header-img` can be set for custom header image. Should be 1900px wide. Also dim the photo, maybe 1-3 exposure stops.


### Testing

I use [HTML::Proofer](https://github.com/gjtorikian/html-proofer) to help check my HTML. The Rakefile is set to ignore alt tags and check only external links.

```shell
bundle exec rake test
```

## TODO:

* Move all images to be local, instead of hosted on blogspot.
* Add Search feature (possible on Github Pages?)
* Consider Heroku. See: [How to deploy jekyll site to heroku](http://blog.bigbinary.com/2014/04/27/deploy-jekyll-to-heroku.html)
