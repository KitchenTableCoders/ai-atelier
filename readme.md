# Kitchen Table Coders' Workshop

## Introduction

This repo holds the code for Kitchen Table Coder's **AI Atelier** website. The site is written in Jekyll and hosted on Github Pages.

You'll need [ruby](https://github.com/postmodern/chruby) configured on your system to build the site locally. Run `bin/server` to install dependencies and start an incremental build server. Navigate to [localhost:4000](http://127.0.0.1:4000) to view the site.

Available to preview here: <http://kitchentablecoders.com/ai-atelier/>.

## CSS

The site reads from `assets/css/main.scss`. Jekyll will take a look at the file name and render css from the Sass source.

## Templates and Content

Someday we'll clean this up. Until then, the templates in use are:

- Templates (Layout)
    - [http://ai-atelier.com/](http://ai-atelier.com/): `_layouts/home.html` > `_layouts/default`
    - [About](http://ai-atelier.com/about/): `_layouts/page.html` > `_layouts/default`
    - [Past Workshops](http://ai-atelier.com/previous/): `pages/previous.html` > `_layouts/default`
- Content
    - [http://ai-atelier.com/](http://ai-atelier.com/): `_posts/2018-01-15-machine-learning.md`
    - [About](http://ai-atelier.com/about/): `/pages/about.md`
    - [Past Workshops](http://ai-atelier.com/previous/): `_posts/*.md`

## Theme Stuffs

- Customize the theme
    - `_config.yml`
    - If a variable in this document is marked as "optional", disable the feature by removing all text from the variable.
- Run the Jekyll server: `jekyll serve`

---

# Official Docs: Type on Strap

A free and open-source [Jekyll](https://jekyllrb.com) theme. Based on Rohan Chandra [type-theme](https://github.com/rohanchandra/type-theme) with a few new features:

* Responsive design
* Portfolio page for your projects
* Tags compability
* Bootstrap : [Get Bootstrap](http://getbootstrap.com/)
* Search feature : [Simple-Jekyll-Search](https://github.com/christian-fei/Simple-Jekyll-Search)
* Math Rendering : [KateX](https://github.com/Khan/KaTeX)
* Seo Tags : [Jekyll-seo-tag](https://help.github.com/articles/search-engine-optimization-for-github-pages/)
* Free of rights images from [pexels](https://www.pexels.com/)

## Structure

Here are the main files of the template

```bash
jekyll-theme-basically-basic
├── _draft	               # To store your drafts, they won't be published on your site
├── _includes	               # theme includes
├── _layouts                   # theme layouts (see below for details)
├── _portofolio	               # collection of article to be populated in the portfolio page
├── _posts                     # Blog posts
├── _sass                      # Sass partials
├── assets
|  ├── js	               # theme javascript, Katex, jquery, bootstrap, jekyll search,
|  ├── css                     # isolated Bootstrap, font-awesome, katex and main css
|  ├── fonts		       # Font-Awesome, Glyphicon, and other fonts
|  └── img		       # Images used for the template
├── pages
|   ├── 404.md		       # To be displayed when url is wrong
|   ├── about.md               # About example page
|   ├── portfolio.html	       # Portfolio bootstrapped page
|   ├── search.html	       # Search page
|   └── search.json            # Specify the search target (page, post, collection)
├── _config.yml                # sample configuration
└── index.html                 # sample home page (blog page paginated)
```

### Site configuration

Configure Jekyll as your own blog or with a subpath in in `_config.yml`:

Jekyll website *without* a subpath (such as a GitHub Pages website for a given username):

```yml
  baseurl: ""
  url: "https://username.github.io"
```

Jekyll website *with* subpath (like the Type on Strap [demo](https://sylhare.github.io/Type-on-Strap/) page):

```yml
  baseurl: "/sub-directory"
  url: "https://username.github.io/"
```

Please configure this  before using the theme.

### Meta and Branding

Meta variables hold basic information about your Jekyll site which will be used throughout the site and as meta properties for search engines, browsers, and the site's RSS feed.

Change these variables in `_config.yml`:

```yml
  theme_settings:
    title: My Jekyll Blog                 # Name of website
    avatar: assets/img/triangular.svg     # Path of avatar image, to be displayed in the theme's header
    gravatar: f98....6bfc                 # MD5 hash of your email address
    description: My blog posts            # Short description, primarily used by search engines
```

### Customizing text

#### Footer and Header's text

Customize your site header/footer with these variables in `_config.yml`:

```yml
  theme_settings:
    header_text: Welcome to my Jekyll blog
    header_text_feature_image: assets/img/sample3.png
    footer_text: Copyright 2017
```

#### Localisation string

Change localization string variables in `_config.yml`.

English text used in the theme has been grouped  so you can quickly translate the theme or change labels to suit your needs.

```yml
  theme_settings:
     str_follow_on: "Follow on"
     str_rss_follow: "Follow RSS feed"
     str_email: "Email"
     str_next_post: "Next post"
     str_previous_post: "Previous post"
     str_next_page: "Next"
     str_previous_page: "Prev"
     str_continue_reading: "Continue reading"
     str_javascript_required_disqus: "Please enable JavaScript to view comments."
```
### Other features

Jekyll works with [liquid](https://shopify.github.io/liquid/) tags usually represented by:

```
{{ liquid.tag | filter }}
```
These are useful to render your jekyll files. You can learn more about them on [shopify's doc](https://help.shopify.com/themes/liquid/basics)

### Footer's icons

Display the site's icon from [Font Awesome](https://fortawesome.github.io/Font-Awesome/) in the footer. All icon variables should be your username enclosed in quotes (e.g. "username") in `_config.yml`, except for the following variables:

```yml
  theme_settings:
     rss: true
     email_address: type@example.com
     linkedin: ttps://www.linkedin.com/in/FirstLast
     stack_exchange: https://stackoverflow.com/users/0000/first-last
```

### Comments (via Disqus)

Optionally, if you have a [Disqus](https://disqus.com/) account, you can show a
comments section below each post.

To enable Disqus comments, add your [Disqus shortname](https://help.disqus.com/customer/portal/articles/466208) to your project's `_config.yml` file:

```yml
  theme_settings:
     disqus_shortname: my_disqus_shortname
```

### Google Analytics

To enable Google Analytics, add your [tracking ID](https://support.google.com/analytics/answer/1032385)
to `_config.yml` like so:

```yml
  theme_settings:
     google_analytics: UA-NNNNNNNN-N
```

### Math typesetting

When KateX is set in `_config.yml`:

```yml
  theme_settings:
     katex: true # to Enable it
```

You can then wrap math expressions with `$$` signs in your posts and make sure you have set the `katex` variable in `_config.yml` to `true` for math typesetting.

For inline math typesetting, type your math expression on the *same line* as your content. For example:

```latex
Type math within a sentence $$2x^2 + x + c$$ to display inline
```

For display math typesetting, type your math expression on a *new line*. For example:

```latex
$$
  \bar{y} = {1 \over n} \sum_{i = 1}^{n}y_i
$$
```

## Layout

Please refer to the [Jekyll docs for writing posts](https://jekyllrb.com/docs/posts/). Non-standard features are documented below.

### Layout: Post

This are the basic features you can use with the  `post` layout.

```yml
---
layout: post
title: Hello World                                # Title of the page
subtitle: "This is a subtitle"                    # A subtitle can be displayed below your title
feature-img: "assets/img/sample.png"              # Add a feature-image to the post
thumbnail: "assets/img/thumbnail/sample-th.png"   # Add a thumbnail image on blog view
tags: [sample, markdown, html]
---
```

With `thumbnail`, you can add a smaller image than the `feature-img`. If you don't want/have a thumbnail you can still use the same image as the feature one.

### Layout: Page

The page layout have a bit more features explained here.

```yml
---
layout: page
title: "About"
subtitle: "This is a subtitle"
feature-img: "assets/img/sample.png"
permalink: /about.html               # Set a permalink your your page
hide: true                           # Prevent the page title to appear in the navbar
tags: [sample, markdown, html]
---
```

The hide only hides your page from the navigation bar, it is however still generated and can be access through its link. Use the `_draft` folder to keep files from being generated on your site.

### Layout: Bootstrap

This is the page layout modified to have bootstrap activated to format your content accordingly with the theme.

```yml
---
layout: bootstrap
---
```

### Layout: Default

This layout includes the head, navigation bar and footer around your content.

## Feature pages

All feature pages besides the "home" one are stored in the `page` folder, they will appear in the navigation bar unless you set `Hide: true` in the front matter.

Here are the documentation for the other feature pages that can be added through `_config.yml`.

### Home

This page is the used as the home page of the template (in the `index.html`). It displays the list of article in `_posts`.
You can use this layout in another page (adding a title to it will make it appear in the navigation bar).

### Portfolio

Portfolio is a feature bootstrapped page that will take all the markdown/html files in the `_portfolio` folder to create a 3x3 image portfolio matrix.

The portfolio page can be enable/disable in the navigation bar through the `_config.yml` via:
```yml
# Scripts / Feature
  portfolio: true
```

### Search

The search feature is based on [Simple-Jekyll-search](https://github.com/christian-fei/Simple-Jekyll-Search) there is a `search.json` file that will create a list of all of the site posts, pages and portfolios.

Then there's a `search.js` displaying the formated results entered in the `search.html` page.


The search page can be enable/disable in the navigation bar through the `_config.yml` via:
```yml
# Scripts / Feature
  search: true
```

### Tags

Tags should be placed between `[]` in your post metadata. Seperate each tag with a comma. Tags are recommended for posts and portfolio items.

For example:

```yml
---
layout: post
title: Markdown and HTML
tags: [sample, markdown, html]
---
```

> Tags are case sensitive `Tag_nAme` ≠ `tag_name`

All the tags will be listed in `tags.html` with a link toward the pages or posts.
The tags page can be enable/disable in the navigation bar through the `_config.yml` via:

```yml
# Scripts / Feature
  tags: true
```

## Template as a Gem

You can use Type-on-strap as a [gem](https://rubygems.org/gems/type-on-strap). Checkout an example in the [gem-demo branch](https://github.com/Sylhare/Type-on-Strap/tree/gem-demo).

To make the feature pages available in from the gem I created them as layouts that can be invoked in the pages folder.

So if you're using the template as a theme, Make sure you have:
  - A `index.html` file
  - The right `_config.yml` with the theme setting such as `theme: type-on-strap` uncommented
  - The feature page included. (ex: as it is already in `pages`)
  - Some content ready in `_posts` and `_portfolio` to be displayed

Now you can use any theme gem with github pages : [29/11/2017 Github Pages Broadcast](https://github.com/blog/2464-use-any-theme-with-github-pages)

## License

[The MIT License (MIT)](https://raw.githubusercontent.com/Sylhare/Type-on-Strap/master/LICENSE)
