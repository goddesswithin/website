# Goddess Within site

This is a demonstration of the site hosted using [GitHub Pages](https://pages.github.com/).

It is a copy of http://goddesswithin.us, to show how a similar site could be controlled, and how it is different.

## WordPress vs GitHub Pages

The original site was created with WordPress. WordPress provides a "WYSIWYG" (what you see is what you get) editor that abstract away the code, but they are harder to host. This means that it can be costly to host, which can lead to content being lost entirely.

The [GitHub Pages](https://pages.github.com/) approach is a little different. It requires a bit more technical knowledge to maintain, but it comes with these benefits:

- GitHub Pages is free to host for public repositories. When setting up a website, hosting is usually the costliest piece.
- The overall codebase is significantly less overwhelming then WordPress's and easier to maintain.
- The history of the site is totally transparent (which is the nature of `git`)
- Anyone can request to contribute (but the actual site can only be modified by contributors).
- If the domain goes down, the content is still on GitHub. Someone can pick up the mantle by "forking" the site and making their own version.
- Because of how git works, if GitHub goes down, there are likely copies distributed on multiple computers of the website.

## Where is the content?

When GitHub goes to publish a new version of the site, it uses a program called [Jekyll](https://jekyllrb.com/) to generate the site. Jekyll allows you to separate a page's content from the layout and structure of the website, and write the content in different formats. The most common format you will see pages written in is [Markdown](https://daringfireball.net/projects/markdown/basics), which is much easier to read *and* learn than HTML.

In other words, if you want to change the content of the homepage, for example, you only need to change the text in [index.md]().

If you want to create a new page, you can just create a new file ending in `.md` and start writing. You don't need to worry about including navigation headers, stylesheets, or other advanced website stuff, because Jekyll handles all of that for you.

## Who can make changes?

Anyone with edit permission on this repository can make changes. 

However, anyone with a GitHub account can **request** to make changes, and discuss those requests. It is up to someone with edit permissions to review the changes, make sure they are acceptable, and merge them into the site.

As an example, you can review #1.

## What *can't* GitHub Pages do?

While GitHub Pages uses Jekyll to generate content, the end result is still "static"--you cannot create interactive content without the help of third party libraries.

For example, there isn't a native way to add comments to pages, or to add in a shop.

However, there are resources that help you to do this. For example, [Discus](https://disqus.com/) is a platform that lets you add comments to pages, and it stores comments based on the page's permalink. Site search can be implemented through plugins like [Elastic Site Search](http://elastic.co/products/site-search/service?ultron=resources&blade=jekyll&hulk=referral).