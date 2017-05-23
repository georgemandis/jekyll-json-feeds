Jekyll JSON Feed Templates
=========================

A few Liquid templates to use for rendering JSON feeds for your Jekyll blog in keeping with the [JSONFeed spec](https://jsonfeed.org/).  Like it's sister project [jekyll-rss-feeds](https://github.com/snaptortoise/jekyll-rss-feeds), it features a number of kinds of feeds:

- **feed.json** &mdash; Renders the 10 most recent posts.
- **feed.category.json** &mdash; Only renders posts for a specific category. This example renders posts for a "miscellaneous" category.
- **feed.tag.json** &mdash; Only renders posts for a specific tag. This example renders posts for a "jekyll" category.
- **feed.links.json** &mdash; Only contains posts that link to external websites noted by a <code>link</code> variable in the [YAML Front Matter](https://github.com/mojombo/jekyll/wiki/YAML-Front-Matter).  Not a common Jekyll convention, but a good way to generating a linked list.
- **feed.articles.json** &mdash; Only showing articles that don't link to external sites; The opposite of <code>feed.links.json</code>

How to use
----------
- Update \_config.yml as noted below, or manually replace the variables.
- Copy one of the JSON (ie, <code>feed.json</code>) files to the root directory of your Jekyll blog.
- Run <code>jekyll</code>.

In your generated <code>\_site</code> folder you should find a properly formatted feed at <code>feed.json</code>.

Customizing \_config.yml
------
These templates rely on a customized version of <code>\_config.yml</code>.  The following lines have been added:

	name: Your Blog's Name
	description: A description for your blog
	url: http://your-blog-url.example.com
  author: Your Name (optional)

This makes it easy to reference the title, description and URL for your site in the feed templates using <code>{{ site.name }}</code>, <code>{{ site.description }}</code> and <code>{{ site.url }}</code>.  Even if you're not using these feed templates, you might find these variables useful when you're designing your layouts.

## Looking for the RSS version?

If you missed the link at the top please also checkout the original incarnation of this project: 

[github.com/snaptortoise/jekyll-rss-feeds](https://github.com/snaptortoise/jekyll-rss-feeds)
