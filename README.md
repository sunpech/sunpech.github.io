# sunpech.github.io

This is my website/blog that is run using [Jekyll](http://jekyllrb.com/) and is hosted on [Github Pages](https://pages.github.com/). The posts were converted from [Blogger](http://www.blogger.com). See: [Blogger migration](http://jekyllrb.com/docs/migrations/).

The theme is based off of [Pool Hyde](https://github.com/poole/hyde).

## Creating a Post

Here are some helpful tips in creating a post, particularly in [front matter](http://jekyllrb.com/docs/frontmatter/) variables such as thumbnail, image, and description. Also see draft example.

* Name post files with YEAR-MM-DD-TITLE.md format.
* thumbnail width should be 300px. 
* image width should be 600px or wider. Recommended: 800px.
* description should be filled out for better Twitter Cards and Facebook Graph posts (optional).
* Use Markdown in new posts, but HTML is acceptable (not encouraged).

### Drafts

Drafts for future posts can be found in folder: _drafts. When testing locally, just run the following to see what it looks like:

{% highlight bash %}
	jekyll s --drafts
{% endhighlight %}

### Posts

Posts that are used to generate the site are found in folder: _posts. After a draft is made, just copy it to this folder and git push to origin.

### Tags

For any new tag that doesn't alredy exist, create a folder of that name in the folder tag. Then copy index.md from another tag folder into this newly created tag folder.

## Creating a Page

There is a folder called best/, which contains pages regarding recommendations of best products etc. 

### Variables

* navigation - set to true or false, as to should be shown as navigation link.
* permalink - path to page
* best - set to true or false, to be used as part of index of best pages. Optional, only required if to be displayed.

## TODO:

* Move all images to be local, instead of hosted on blogspot.
* Add Search feature
