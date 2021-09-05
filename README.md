# Cupper-hugo-dfd-x

[![Netlify Status](https://api.netlify.com/api/v1/badges/75ddecc5-089c-4ec5-a587-1c2d6a194c93/deploy-status)](https://app.netlify.com/sites/cupper-hugo-dfd-x/deploys)

A Hugo theme, ported from the [zwbetz-gh/cupper-hugo-theme](https://github.com/zwbetz-gh/cupper-hugo-theme), which is an accessibility-friendly
Hugo theme, ported from the [original Cupper](https://github.com/ThePacielloGroup/cupper) project.

We try to remain accessibility-friendly while still having nice features like cover images and thumbnails for those able to appreciate them.

For production use we recommend the upstream [zwbetz-gh/cupper-hugo-theme](https://github.com/zwbetz-gh/cupper-hugo-theme) rather than experimental theme.

## Table of contents

- [Demo](#demo)
- [Minimum Hugo version](#minimum-hugo-version)
- [Installation](#installation)
- [Updating](#updating)
- [Run example site](#run-example-site)
- [Configuration](#configuration)
- [Logo](#logo)
- [Favicons](#favicons)
- [Shortcodes](#shortcodes)
- [Syntax highlighting](#syntax-highlighting)
- [Disable toc for a blog post](#disable-toc-for-a-blog-post)
- [Localization](#localization)
- [Custom CSS and JS](#custom-css-and-js)
- [Default to Dark Theme](#default-to-dark-theme)
- [Non-Git Repo](#non-git-repo)
- [Getting help](#getting-help)
- [Credits](#credits)

## Demo

https://cupper-hugo-dfd-x.wildtechgarden.ca/

## Minimum Hugo version

Hugo version `0.87.0` or higher is required. View the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

## Installation

From the root of your site:

```
git submodule add https://github.com/danielfdickinson/cupper-hugo-dfd-x.git themes/cupper-hugo-dfd-x.
```

## Updating

From the root of your site:

```
git submodule update --remote --merge
```

## Run example site

From the root of `themes/cupper-hugo-dfd-x/exampleSite`:

```
hugo server --themesDir ../..
```

## Configuration

Copy `config.yaml` from the [`exampleSite`](https://github.com/danielfdickinson/cupper-hugo-dfd-x/tree/main/exampleSite), then edit as desired. 

## Logo

Place your SVG logo at `static/images/logo.svg`. If you don't provide a logo, then the default theme logo will be used. 

## Favicons

Upload your image to [RealFaviconGenerator](https://realfavicongenerator.net/) then copy-paste the generated favicon files under `static`. 

## Shortcodes

See the [full list of supported shortcodes](https://cupper-hugo-dfd-x.wildtechgarden.ca/cupper-shortcodes/).

## Syntax highlighting

Syntax highlighting is provided by [Prism](https://prismjs.com/). See this [markdown code fences example](https://cupper-hugo-theme.netlify.com/cupper-shortcodes/#syntax-highlighting).

By default, only a few languages are supported. If you want to add more, follow these steps:

1. Select the languages you want from <https://prismjs.com/download.html>
1. Download the JS file, then copy it to `static/js/prism.js`
1. Download the CSS file, then copy it to `static/css/prism.css`

## Disable toc for a blog post

Blog posts that have two or more subheadings (`<h2>`s) automatically get a table of contents. To disable this set `toc` to `false`. For example:

```
---
title: "My page with a few headings"
toc: false
---
```

## Localization

The strings in the templates of this theme can be localized. Make a copy of `<THEME_BASE_FOLDER>/i18n/en.yaml` to `<YOUR_SITE_FOLDER>/i18n/<YOUR_SITE_LANGUAGE>.yaml`, and translate one by one, changing the `translation` field.

[Here is a tutorial that goes more in depth about this.](https://regisphilibert.com/blog/2018/08/hugo-multilingual-part-2-i18n-string-localization/)

## Custom CSS and JS

You can provide an optional list of custom CSS files, which must be placed inside the `static` dir. These will load after the theme CSS loads. So, `static/css/custom_01.css` translates to `css/custom_01.css`.

You can provide an optional list of custom JS files, which must be placed inside the `static` dir. These will load after the theme JS loads. So, `static/js/custom_01.js` translates to `js/custom_01.js`.

See the [example site config file](https://github.com/danielfdickinson/cupper-hugo-dfd-x/blob/main/exampleSite/config.yaml) for sample usage.

## Default to Dark Theme

In the site config file set the param `defaultDarkTheme` to true.

E.g. for `config.yaml`
```yaml
params:
  defaultDarkTheme: true
```

Note that the default of light or dark theme only applies to the first visit to a site using this theme. Once the site is visited the choice of dark or light theme is stored in 'local storage' in the browser.

To reset to a 'first visit' scenario (e.g. for testing), one needs to either browse in private mode (aka Incognito/InPrivate/etc) or delete 'local storage' for this site. The easiest way to do that, but which affects other sites as well, is to use the 'Clear History' feature of the browser.

Check your browser's help or documentation for details.

## Non-Git Repo

If your site is **not** a git repo, then set `enableGitInfo` to `false` in your config file.

## Getting help

If you run into an issue that isn't answered by this documentation or the [`exampleSite`](https://github.com/danielfdickinson/cupper-hugo-dfd-x/tree/main/exampleSite), then visit the [Hugo forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132).

## Credits

Thank you to [Zachary Betz](https://zwbetz.com/) for creating the Cupper-hugo-theme, and thank you to [Heydon Pickering](http://www.heydonworks.com) and [The Paciello Group](https://www.paciellogroup.com/) for creating the original Cupper project. 
