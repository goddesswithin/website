# Goddess Within site

This is a demonstration of using [GitHub Pages](https://pages.github.com/) to host the Goddess Within site.

It is a copy of http://goddesswithin.us, to show how a similar site could be maintained this way, and how it is different.

## WordPress vs GitHub Pages

The original site was created with **WordPress**. WordPress manages the content, as well as an interface to modify the content--which makes it more costly and difficult to host, and can lead to lost content.

The [GitHub Pages](https://pages.github.com/) approach is a little different. It requires a bit more technical knowledge to maintain the content, but it comes with these benefits:

- GitHub Pages is free to host for public repositories, significantly reducing cost.
- The overall codebase is significantly less overwhelming then WordPress's and easier to maintain.
- The history of the site is totally transparent (which is the nature of `git`)
- Anyone can request to contribute (but the actual site can only be modified by contributors).
- If the domain goes down, the content is still on GitHub. Someone can pick up the mantle by "forking" the site and making their own version.
- Because of how git works, if GitHub goes down, there are likely copies distributed on multiple computers of the website.

## Where is the content?

GitHub stores code in "repositories". A repository is like a folder on your computer that is marked to contain files for a specific project. The repository contains all of the files needed to generate the website on any platform that can run code.

The **content** of the homepage, for example, is in [index.md](https://github.com/goddesswithin/website/blob/main/index.md).

When GitHub goes to publish a new version of the site, it uses a program called [Jekyll](https://jekyllrb.com/) to generate the site. Jekyll separates all of the code that contains the design, layout, and structure from the files that contain the content. It can also generate pages from multiple formats. `index.md` is written in [Markdown](https://daringfireball.net/projects/markdown/basics), which is much easier to read *and* learn than HTML.

If you want to create a new page, you can just create a new file ending in `.md` and start writing. You don't need to worry about including navigation headers, stylesheets, or other advanced website stuff, because Jekyll handles all of that for you.

I plan on writing documentation for common maintenance tasks. 

## Who can make changes?

Anyone with **edit permission** on this repository can make changes. They will need a GitHub account, and to have the rights granted by an admin.

However, anyone with a GitHub account can **request** to make changes, and discuss those requests. It is up to someone with edit permissions to review the changes, make sure they are acceptable, and merge them into the site.

I created [an example request](https://github.com/goddesswithin/website/pull/1) to show what it looks like when someone wants to make changes to the code.

This README is on the front of the repository. Later on, it can be updated to explain how to contribute (including tutorials), what kinds of contributions will be accepted, a code of conduct, etc.

## What *can't* GitHub Pages do?

GitHub pages hosts "static" content. The sites hosted by it are read-only by end users.

While GitHub Pages uses Jekyll to generate content, the end result is still "static"--you cannot create interactive content without the help of third party libraries.

For example, there isn't a native way to add comments to pages, or to add in a shop.

However, there are resources that help you to do this. For example, [Discus](https://disqus.com/) is a platform that lets you add comments to pages, and it stores comments on its own servers based on the page's permalink. Site search can be implemented through plugins like [Elastic Site Search](http://elastic.co/products/site-search/service?ultron=resources&blade=jekyll&hulk=referral).
