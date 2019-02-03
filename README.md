```
This theme is no longer maintained.
```

# What is this.

This is the theme for Hugo that supports the [Accelerated Mobile Pages Project](https://www.ampproject.org/).

[Hugo :: A fast and modern static website engine](https://gohugo.io/)

## PC View

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_tropic/master/images/screenshot.png)

## SP View(Responsive)

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_tropic/master/images/responsive.png)

## Article footer

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_tropic/master/images/taxonomy.png)

## AMP supported

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_tropic/master/images/amp-valid.png)

# Features

* [Accelerated Mobile Pages Project](https://www.ampproject.org/) a.k.a AMP supported
* Responsive design
* Google Analytics
* High score by Google Page Speed Insight.
* Share button
* Structured data(Article and Breadcrumb)
* Twitter cards
* OGP
* Specializing in SEO

## Installation

```
$ cd themes
$ git clone https://github.com/dim0627/hugo_theme_tropic.git
```

[Hugo \- Installing Hugo](http://gohugo.io/overview/installing/)

# `config.toml` example

```
baseurl = "https://example.com/"
title = "SiteTitle"

googleAnalytics = "UA-XXXXXXXX-XX" # Optional

[params]
  contact = "contact@example.com" # Optional
  dateformat = "Jan 2, 2006" # Optional
  themecolor = "#00bcd4" # Optional, <meta name="theme-color" content="{{ . }}">
  # Fonts settings.
  googlefonts = "https://fonts.googleapis.com/css?family=Lobster|Lato:400,700" # Optional, Include google fonts.
  fontfamily = "Lato,YuGothic,'Hiragino Kaku Gothic Pro',Meiryo,sans-serif" # Optional, Override body font family.
  logofontfamily = "Lobster, cursive" # Optional, Override logo font.
  ampscripts = """ # Optional, scripts for AMP.
<script async custom-element="amp-twitter" src="https://cdn.ampproject.org/v0/amp-twitter-0.1.js"></script>
<script async custom-element="amp-iframe" src="https://cdn.ampproject.org/v0/amp-iframe-0.1.js"></script>
<script async custom-element="amp-ad" src="https://cdn.ampproject.org/v0/amp-ad-0.1.js"></script>
"""
```

# Frontmatter example

```
+++
date = "2016-09-28T17:00:00+09:00"
title = "Article title here"
+++
```

# Recommended directory structure

This themes `Header Menu` is using `Section`.
Recommend that you use the section than taxonomy.

```
.
├── config.toml
├── content
│   ├── section1         # Separated by Section.
│   │   └── article1.md
│   └── section2
│       └── article2.md
├── layouts
└── static
    └── favicon.ico
```

# Shortcodes

## Iframe

```
{{% iframe src="https://www.youtube.com/embed/XXXXXXX" w="560" h="315" %}}
```

## Image

```
{{% img src="images/image.jpg" w="600" h="400" %}}
{{% img src="images/image.jpg" w="600" h="400" class="right" %}}
{{% img src="images/image.jpg" w="600" h="400" class="left" %}}
{{% img src="images/image.jpg" w="600" h="400" caption="Referenced from wikipedia." href="https://en.wikipedia.org/wiki/Lorem_ipsum" %}}
```

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_tropic/master/images/include-images.png)

## Clear

Break float.

```
{{% img src="images/image.jpg" w="600" h="400" class="right" %}}

brabrabra # Displayed left of the image.

{{% clear %}}

brabrabra # Displayed below of the image.
```

## Twitter

```
{{% twitter tweetid="780599416621297xxx" %}}
```

# Development mode

Supported development mode.

```
env HUGO_ENV="DEV" hugo server --watch --buildDrafts=true --buildFuture=true -t tropic
```

This mode is

* Not show Google Analytics tags.
* Show `IsDraft`.
* Show `WordCount`.

And set `{{ if ne (getenv "HUGO_ENV") "DEV" }} Set elements here. {{ end }}` if you want to place only in a production environment.

# Using iconset

* [Font Awesome, the iconic font and CSS toolkit](http://fontawesome.io/)

# Colorscheme

* [Material Design Colors, Material Colors, Color Palette \| Material UI](https://www.materialui.co/colors)

