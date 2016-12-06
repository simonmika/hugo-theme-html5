# HTML 5 Theme for Hugo (dn3s Fork)

This is a fork of [simonmika](https://github.com/simonmika)'s [hugo-theme-html5](https://github.com/simonmika/hugo-theme-html5).
It's got a bunch of feature branches that I am hoping will be merged upstream. The master branch is simply a combination of all the feature branches.
You probably don't want to install this theme; **use the upstream version instead!**
This one may at any point be out of date or have bugs. 

HTML5 theme for the static site generator [Hugo](http://http://hugo.spf13.com).
It is not a complete theme but rather a set of templates that generates the necessary HTML. It also contains some sensible CSS reset.
It requires the end user to provide their custom design through CSS files.

## Getting started
### Clone
Clone this repository into your `themes` folder of your site. Issue the following command from within your Hugo sites root directory:

	git clone https://github.com/simonmika/hugo-theme-html5 themes/html5

### Add stylesheets
Add CSS for your site into the css folder. For example:

```
static/css/layout.css
static/css/colors.css
```

And add it to your config under `.params.css`:

#### TOML example:

```
[params]
	...
	css = ["layout.css", "colors.css"]
	...
```

#### YAML example:

```
params:
	...
	css: ["layout.css", "colors.css"]
	...
```

#### JSON example:

```
{
	...
	"params": {
		...
		"css": ["layout.css", "colors.css"],
		...
	}
	...
}
```

### Add Favicon
Add your sites favicon here:

```
	static/favicon.ico
```

### Create Menu
Add pages to the `main` menu.

## Features
 * CSS only designing
 * Menu with infinitive levels
 * Uses HTML 5 structural elements

## Configuring

### Table Of Contents

By default, every article is preceded by a table of contents.
To diable this globally, set `Params.toc` to `false` in your site config.
To override the global setting, set `toc` in the front matter of an individual article.

### Word Counts

By default, every article is preceded by a word count and estimated reading time.
To disable this globally, set `Params.showWordCount` to `false` in your site config.

## Contributing

Please clone this repository and create pull-requests for any features that could have a more general use and that fit within the vision of this theme.
